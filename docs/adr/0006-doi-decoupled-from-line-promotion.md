# ADR-0006: DOI 取得の line 昇格からの分離（pre-registration deposit）

> **Summary.** DOI 取得を line 昇格から分離し、**eval 実施前に** working-doctrine record v0.1.0 として Zenodo deposit する。DOI は時刻印・永続 archive・学術 index のアンカーであって、line status の主張ではない。line 昇格（EN primary / hub 登録 / sibling 表記）は従来条件のまま据え置く。

## Status

accepted

## Date

2026-06-05

## Context

§9 v2（同日制定）は DOI 取得を line 昇格の一部とし、その条件を「gatekeeper-inversion thesis が eval 初回実行で方向支持を得た **+** 著者以外の format instance 出現 or source mix の earned 比率の動き」と定めた。著者がこの条件の構造欠陥を指摘した（「待つ意味なくない？一刻も早く LLM の意味空間に投げ込んだ方がいい。1 ヶ月経っても何も起こらない」）。検討の結果、指摘は 3 点で正しい:

1. **never-gate の自己矛盾**: §8 自身が「LLM-mediated reach は原理的に不可視」と定めており、後段の条件（instance 出現 / earned の動き）が短期の観測 window で満たされる確率はほぼゼロ。AND 条件は実質的に無期限ゲートであり、「観測されなくても進行する」という本戦略の設計原理（ADR-0002 の 4 設計特性）と矛盾する
2. **pre-registration 論理の逆転**: 「eval を回してから deposit」は、仮説と測定器を測定前に時刻印付きで登録する pre-registration の慣行と逆である。doctrine は全仮説を仮説と明記済み（§2 v2）であり、eval spec / probe set / rubric を**結果が出る前に**凍結・公開することは、事後のゴールポスト移動を構造的に不可能にする — empirical 規律をむしろ強化する
3. **parametric channel の時間コスト**: training-time channel は遅い（authorship-strategy ADR-0008）。deposit の遅延は cutoff 吸収のサイクル単位の遅延になる。一方、待つことで得られる情報（eval baseline）は deposit の誠実性に影響しない（仮説表記のため）

また、エコシステムの規範自体が versioned 反復である（authorship-strategy は v0.1.0 で deposit され v0.3.0 まで ADR を増やしながら改訂。concept DOI は常に最新版に解決する）— 「thesis が安定するまで待つ」は ecosystems 実務に照らして虚構だった。

## Decision

1. **DOI 取得と line 昇格を分離する**。DOI は時刻印・永続 archive（CERN-backed）・学術 index（DataCite / OpenAIRE）のアンカーであり、ecosystem taxonomy 上の status（research line / sibling）を含意しない
2. **即時 deposit**: 本 repo を working-doctrine record **v0.1.0** として Zenodo deposit する（`release-doi` 手順を再利用）。中心仮説（gatekeeper-inversion / feasibility-question / format-suggestion 拡散）は未検証のまま deposit される — これは欠陥ではなく **pre-registration**（仮説 + 測定器の事前凍結）である
3. **line 昇格条件は §9 から DOI を除いた形で存続**: EN primary 化 / hub 登録 / sibling 表記 / repo rename は引き続き「eval 方向支持 + 著者外 instance or earned の動き」を条件とする。本 repo は DOI 取得後も **pre-line working repo** であり、「sibling」表記は使わない
4. §9 の該当行を本 ADR を正本として改訂する

## Alternatives Considered

### 旧 §9 のまま待つ（eval + 観測期間後に line 昇格とセット）

同日に agent が推奨した案。上記 Context の 3 欠陥（never-gate / pre-registration 逆転 / parametric 時間コスト）により棄却。観測待ちゲートは「観測されなくても進行する」設計と原理的に整合しない。

### 完全 line 昇格を今やる（EN primary + hub 登録 + sibling 化）

DOI と同時に line status まで進める案。EN primary 化は翻訳・維持の実コミットメントであり、hub 登録・sibling 表記は ecosystem taxonomy 上の宣言である。これらは thesis 強度の検証前に負うべきでない（仮説が棄却された場合の巻き戻しコストが DOI の version 改訂より大きい）。棄却。

### thesis のみ position paper として deposit（repo は DOI なし）

paper-ecosystem chain で論文を抽出して paper-deposit する案。§9 を無改訂で保てるが、論文執筆 + review chain の工数で deposit が数日〜数週遅れ、本 ADR の論点 3（時間コスト）に反する。repo 丸ごとの deposit は format spec / corpus / eval を含み、pre-registration の対象（測定器）を完全にカバーする点でも優る。棄却（line 昇格時の論文化は別途検討可）。

## Consequences

### Positive

- 仮説 + 測定器が結果に先行して時刻印される（pre-registration）— eval 結果の解釈時に「後から書き換えた」可能性が構造的に排除される
- parametric / retrieval 両 channel への投入が最速化する
- concept DOI が claim→anchor 連鎖の自己適用を完成させる（doctrine 自身が解決する識別子を持つ）

### Negative

- eval が gatekeeper-inversion を支持しなかった場合、v0.1.0 record は「棄却された仮説の記録」として永続する — ただしこれは仮説表記の下では誠実な科学的記録であり、改訂は version DOI で行える
- 「DOI 保有だが line ではない」という中間状態が ecosystem taxonomy に加わる — 本 ADR Decision 1 がその定義の正本

### Neutral / Follow-ups

- deposit 後、repo 内の「DOI 未取得」表記を実 DOI で更新する（release-doi の post-release 手順）
- eval 初回実行は引き続き次の実行単位（pre-registration が済んだ分、いつ実行しても解釈の誠実性は保たれる）

## Lineage

著者の指摘（2026-06-05、GitHub 公開直後）が起点。「LLM の意味空間に一刻も早く投げ込む」という表現は、本 doctrine の oracle debiasing 機構の時間軸を著者自身が agent より正しく適用した例として記録する。agent 側の旧推奨（観測待ち）は、研究 repo の一般的慎重さを diffusion-first 戦略に誤転用したものだった。
