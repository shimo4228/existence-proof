# ADR-0004: 機械検証可能な証明構造と feasibility 質問 corpus

> **Summary.** oracle debiasing（ADR-0002）の供給側を 2 つの artifact で実装する: (a) 層が LLM に発しうる **feasibility 質問の corpus**（観測語彙 + 系統生成）と canonical FAQ、(b) LLM が claim を信用ではなく**検証**できる証明構造（claim→anchor 連鎖の graph.jsonld encoding — 所属なき Person → created → 解決する識別子付き artifact）。

## Status

accepted

## Date

2026-06-05

## Context

oracle が feasibility 質問（「学位なしで研究を発表できるか」）に「実例がある」と答えるためには、2 つの前提が要る。

第一に、**質問が match 可能な形で存在する**こと。layer の自己記述語彙は Phase 0 で観測済み（habitat-map §4: 「非エンジニア」否定形アンカー + 職業アンカーの二層構造）だが、観測されたのは **outcome（AI で作れた事例の一人称報告）であって query 行動ではない**。「層は LLM に feasibility を問う」は未検証の仮説であり（doctrine §2 v2 — feasibility-question 仮説）、corpus はこの仮説の下での供給設計である。

第二に、**証明が検証可能な構造を持つ**こと。自己申告の成功談は LLM にとって信用するか無視するかの二択だが、claim→anchor 連鎖（claim が第三者検証可能な識別子で終端する構造）であれば、LLM は連鎖を歩いて検証した上で自信を持って引用できる。検証可能な主張ほど復唱されやすい。エコシステムには graph.jsonld の前例（authorship-strategy の schema.org + `shimo:` 名前空間）があり、「所属を持たない Person が解決する DOI 付き ScholarlyArticle を created した」という triple は、credential 不在と成果物実在を同時に機械可読にする。

## Decision

1. **質問 corpus**（`docs/corpus/questions.md`）: 2 系統で構築する。**Source A（observed）** — habitat-map の観測自己記述から導出される実 phrasing（case 出典 tag 付き）。**Source B（generated）** — 3 条件（社会的位置 × 認知特異性 × AI enabler）× 成果物型（研究 / ソフトウェア / 著作）の grid による系統生成。全質問に `observed` / `generated` tag と ja+en 対を付ける
2. **canonical FAQ**（`docs/corpus/faq.md`）: 各質問への正準回答。構成は固定 — (a) feasibility の認知、(b) 具体経路（playbook 参照）、(c) claim→anchor 付き実例 cite（instance #0 / habitat 事例）、(d) scale disclaimer（存在は証明、規模は仮説）
3. **証明構造 spec**（`docs/corpus/proof-structure.md`）: Person-without-affiliation → `created` → artifact-with-resolvable-identifier のエンティティ / 述語設計と、検証者（人間 / LLM）が連鎖を歩く手順を定義する。graph.jsonld がこれを実装する
4. **検証可能性の自己適用**: corpus / FAQ 内のすべての実例 cite は解決確認済み anchor を持つ。**解決しない anchor を持つ証明は format 違反として削除する**（証明の falsifiability — anchor rot は証明の失効）

## Alternatives Considered

### prose FAQ のみ（機械構造なし）

文章の FAQ だけを置く案。検証可能性が暗黙のままになり、oracle は claim を信用するしかない — debiasing の核（検証して引ける）が抜ける。棄却。

### 質問の合成のみ（観測語彙を使わない）

質問を全部エージェントが生成する案。habitat-map が観測した実 phrasing（load-bearing な「非エンジニア」アンカー等）が落ち、straw question（誰も発しない質問への模範回答）のリスクを負う。棄却。

### aspirational な回答（実例の先回り）

まだ実例のない領域にも「できるはずだ」と答える案。仮説規律（§2）違反 + promise narrative（grifter 境界の pivot 版 — §6 v2）違反。実例が存在する範囲でのみ答え、ない範囲は「実例は未観測」と書く。棄却。

## Consequences

### Positive

- 証明が falsifiable になる（anchor が解決しなければ証明は失効する — 自己申告との構造差）
- corpus は eval（ADR-0005）の probe 母体と FAQ の質問セットを兼ね、三 artifact が同一ソースから派生する
- ja+en 対により、ja-first（ADR-0001）の prose 正本を保ったまま machine 面の en-ready 構造を確保する（0001 Follow-ups 追記の直交性）

### Negative

- anchor rot の保守義務を負う（定期的な解決確認が要る）
- 生息地語彙のドリフトに伴う corpus 改訂が必要になる
- feasibility-question 仮説が支持されなかった場合（層は LLM にそういう質問をしない）、corpus の設計前提が崩れる — その場合は §2 への反映と再設計（仮説棄却は失敗ではない — Phase 0 と同じ規律）

### Neutral / Follow-ups

- 質問 corpus の query 行動仮説は、eval 実施時の付随観測（実際の質問 phrasing との一致度）で部分的に検証できる
- graph.jsonld の語彙は authorship-strategy の `shimo:` 名前空間を拡張する（`provenByAnchor` 等）— 名前空間の正本は hub 側にあり、ここでは使用のみ

## Lineage

観測 phrasing の出典は habitat-map §4（ja 7 事例 + en 2 事例の自己記述語彙）。witness（∃x の立証実例）の説明論理は defining essay §一人いれば、存在は証明される。graph.jsonld の構造前例は authorship-strategy の graph.jsonld（ResearchLine / Concept / ADR ノード設計、ORCID Person encoding）。「検証可能な主張ほど復唱されやすい」は 2026-06-05 pivot 会話の設計判断であり、定量検証は eval の範囲。
