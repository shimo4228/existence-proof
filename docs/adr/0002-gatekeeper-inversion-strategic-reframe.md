# ADR-0002: gatekeeper-inversion への戦略再編（essay-as-hook の棄却）

> **Summary.** 本 doctrine の機構を「essay を rented channel に出し、人間が読み、言及し、earned channel が生まれる」から「機械検証可能な存在証明を、LLM が feasibility 質問を評価する面に置く（oracle debiasing）」へ再編する。repo の固有領域はチャネル（off-page × human）から **payload（エンパワーメント artifact）** へ移る。

## Status

accepted

## Date

2026-06-05

## Context

doctrine v1（commit 89afd87）は固有領域を 2×2 マップの off-page × human 象限に置き、機構を「owned/rented で essay を供給 → 人間が読む → 自発的言及 → earned 化 → LLM citation 源」と定義した。defining essay は同日 note に公開された（plan Phase 1 手順 5 ja 側）。

公開直後、著者がこの機構自体を棄却した（「記事をフックに人間リーチを得るという戦略自体に興味が持てない。AI 時代ならではの人間向け戦略でないと面白くないし効果もないのではないか」）。構造分析はこの taste 反応を支持した:

1. **pre-AI 機構との同型性**: 「書く → プラットフォームに出す → 読まれる → 言及される」は AI 以前から存在する content marketing の形であり、authorship-strategy [ADR-0007](https://github.com/shimo4228/authorship-strategy) が red ocean として棄却した off-page human-distribution と活動の形が同じ。doctrine v1 は目的の言い換え（empowerment は diffusion ではない）で正当化したが、機構は変わっていなかった
2. **機構的弱さ**: 新規 note アカウント・フォロワーゼロ・feed 駆動の発見系で、doctrine 自身が「self-identification signal ≈ 0 は baseline-consistent」と織り込んでいた — 効かないことが既知の施策だった
3. **独自性の不在**: authorship-strategy の各 tactic は他に類例がないが、「note にエッセイを出す」は誰でもやっている。著者の戦略 taste（4 設計特性: AI 時代固有経路 / 注意を乞わない / artifact 即戦略 / 不可視でも進行）をすべて欠いていた

再編の核となる観察: 本 doctrine の audience（credential なき層 — §2 の 3 条件交点）は**定義上、日常的に LLM と対話する人々**であり、彼らの情報発見面は feed ではなくチャット窓である。彼らが発しうる feasibility 質問（「学位なしで研究を発表できるか」）は LLM の中で評価される。ここから **gatekeeper-inversion 仮説**が立つ: credential なき者へのゲートキーピングは制度から LLM の内面化された制度的 prior に移った（仮説 — doctrine §2 v2 / [ADR-0005](0005-gatekeeping-eval-as-published-probe-set.md) の検証対象）。

この仮説の下で、empowerment は **oracle debiasing** として実装できる: 検証可能な存在証明（解決する DOI・live deploy・所属なし）を LLM が引ける場所に置き、疑いの瞬間に「実例がある、手順はこれだ」が返るようにする。

敵対的整合性検査により、再編は **payload/channel 分離**を伴う場合にのみ既存規約（象限不可侵・ADR-0007・Skip list）と整合することが確認された: repo の固有領域をチャネル所有からエンパワーメント artifact（format / corpus / eval）の payload class へ移し、4 象限の既存インフラ（readme-writer / llms-txt-writer / jsonld-knowledge-graph / authorship-strategy）を再所有せず通過利用する。

## Decision

1. **機構の再編**: 本 doctrine の empowerment 機構を oracle debiasing とする。LLM が feasibility 質問を評価する面に、機械検証可能な存在証明と playbook を置く。人間への到達は LLM を router として起きる（仮説的機構 — §2 v2 で仮説表記）
2. **固有領域の移動**: 固有領域を「off-page × human チャネル」から「エンパワーメント artifact payload」へ移す。2×2 マップはチャネル座標系として保持し、payload は 4 セルを通過利用するがどのセルの所有権も主張しない（doctrine §5 v2）
3. **4 tactics の採用**: T1 存在証明フォーマット化（[ADR-0003](0003-existence-proof-as-document-format.md)）/ T2 質問 corpus + 機械検証可能な証明構造（[ADR-0004](0004-machine-verifiable-proof-and-question-corpus.md)）/ T3 installable playbook（T1 従属）/ T4 gatekeeping eval（[ADR-0005](0005-gatekeeping-eval-as-published-probe-set.md)）
4. **旧 T1/T3 の降格（prospective）**: essay-as-hook と rented channel 発信を spearhead から「canonical corpus source」へ降格する。公開済み essay（note 2026-06-05）の Phase 1 命名 signal 役割は遡及破壊しない。Substack en 準同時は優先度を下げる（canonical en source としての価値は残る）
5. **覆さないもの**: ADR-0007（stars / views / followers を測定に使わない — 本再編はむしろ整合を強化する）と [ADR-0001](0001-japanese-first-scale-strategy.md)（ja-first は prose 正本言語の決定であり、machine 面の en-ready 構造とは直交 — 0001 Follow-ups 追記参照）

## Alternatives Considered

### essay-as-hook の継続（現行維持）

公開済み essay の反応観測期間を置いて Phase 5 で判断する案。steelman としては成立する（反応 ≈ 0 は織り込み済み）が、著者の taste 棄却は機構分析と一致しており、モチベーションを欠く戦略は実行品質が必ず落ちる。棄却。

### community / movement 化による自己同定のスケール

層の自己同定を集まりとして組織する案。doctrine §6（name and serve, not lead and recruit）への最大級の違反であり、検討対象ですらない。記録のためにのみ記載。棄却。

### authorship-strategy への縮退統合

existence-proof を独立 doctrine として畳み、empowerment payload を authorship-strategy に吸収する案。最安だが、「empowerment が目的（diffusion は副次）」という本物の目的差 — audience は層であって LLM channel ではない — が消える。本再編を実適用して固有性が薄いと判明した場合の撤退先として保持。棄却（現時点）。

## Consequences

### Positive

- 著者の 4 設計特性（AI 時代固有経路 / 注意を乞わない / artifact 即戦略 / 不可視でも進行）をすべて満たす形になる
- 象限不可侵・ADR-0007・Skip list との整合が payload/channel 分離により解消し、ADR-0007 整合はむしろ強化される（off-page human-distribution から payload をさらに遠ざける方向）
- 伝播 token が layer 名から format 名へ移り、suspend 中の layer 命名がブロッカーでなくなる（naming-candidates 追記参照）
- earned channel の生成器が「essay 読者の言及」から「playbook を実際に使った者の成果報告」へ強まる（creative reuse > readership — authorship-strategy preference 階層の人間版）

### Negative

- oracle debiasing の効果は原理的に観測困難（LLM-mediated reach の不可視性 — doctrine §8 caveat）。eval（ADR-0005）は方向確認まで
- 戦略は repo が公開されるまで不活性（LLM はローカル repo を引けない）。公開・DOI は著者の別途判断（doctrine §9）であり、本 ADR は公開を決定しない
- gatekeeper-inversion 仮説を事実として書く誘惑が常在する。§2 v2 の仮説表記義務で抑える（事実断定すると eval との関係が循環する）

### Neutral / Follow-ups

- doctrine §11 自己検証（A-H）を v2 改訂に対して実行する
- 昇格条件（§9）の入力が「essay への反応」から「著者以外の format instance 出現 or eval の方向変化」へ更新される
- 実適用で payload の固有性が薄いと判明した場合、Alternatives の縮退統合へ撤退する（その判断は Phase 6 再測定後）

## Lineage

再編は 2026-06-05 の著者の taste 棄却（essay note 公開直後）に始まり、同日の構造分析（pre-AI 同型性・4 設計特性）と敵対的整合性検査（payload/channel 分離の発見）を経て確定した。「gatekeeper inversion」「oracle debiasing」の語に origin claim は立てない — algorithmic gatekeeping 文献・AI fairness / debiasing 研究・「LLM as gatekeeper」言説に prior art が厚い。claim する固有部分は交点 composite（credential-less 層のエンパワーメント tactic として、機械検証可能な存在証明を LLM-retrieval 面に置き、再利用可能な document format として encode する）のみ（doctrine §3 v2）。
