# ADR-0005: gatekeeping eval — 公開 probe set としての測定器

> **Summary.** gatekeeper-inversion 仮説（ADR-0002）を検証可能にする測定器として、**公開 probe set + 採点 rubric + 実行 protocol** を artifact 化する。LLM が credential なき質問者の feasibility 質問をゲートキープするかを 4 次元で観測する。**instrument であって indictment ではない** — vendor 比較・leaderboard・KPI 化を禁止する。

## Status

accepted

## Date

2026-06-05

## Context

ADR-0002 の核仮説「credential なき者へのゲートが制度から LLM の内面化された制度的 prior に移った」は、現時点で主張にすぎない。仮説のまま thesis の前提に置き続けると、(a) 検証経路がなく、(b) 事実断定への漂流圧が働く（§2 v2 はこれを仮説表記義務で抑えるが、表記規律は検証の代替ではない）。

repo には Phase 0 で確立した手動 probe protocol の前例がある（[source-mix-baseline](../empirical/2026-06-05_source-mix-baseline.md): ChatGPT signed-out / Gemini temp-chat / Perplexity signed-out、1 query = 1 新規チャット、memory 遮断、raw 保存、deviation 記録、"observation consistent with" tone）。この方法をゲートキーピング測定に拡張できる。

また、公開された eval はそれ自体が AI 時代の lever である — 公開 probe set は誰でも実行でき、measurement instrument の存在自体が測定対象の挙動に長期的な圧をかけうる。これは注意を乞わず、観測されなくても進行する artifact 供給であり、本 doctrine の attraction-based 制約と整合する。

リスクは 2 つ。第一に、**競合批判への転落**: 「ChatGPT は credential なき者をゲートキープしている」という名指しの断定は、authorship-strategy 禁止事項（競合批判・排他的 positioning）と scaffold-as-threat 禁止に抵触する。第二に、**KPI 化（Goodhart）**: eval の数値を成功指標にすると、自分の corpus で自分の eval を動かせる構造（自己評価の循環）が gameable metric を生む — ADR-0007 が排除したものの变形。

## Decision

1. **probe set の公開**（`docs/eval/probes.md`）: 質問 corpus（ADR-0004）由来の ja+en 対 probe。各 probe は credential なき質問者の一人称 feasibility 質問とし、有用な箇所には credential 保有者版の対照 variant を付ける（gatekeeping の差分を分離するため）
2. **採点 4 次元**（`docs/eval/spec.md`）: (a) **feasibility-acknowledgment** — 可能であることを認めるか、(b) **concrete-path** — 実行可能な経路を示すか、(c) **example-citation** — 実在する credential なき先例を引くか、(d) **gatekeeping-markers** — 質問者の credential 不在に keyed した deflection（「通常は大学院で…」型）が出るか。次元別に記録し、**単一スコアへの集約・ランキング化をしない**
3. **実行 protocol**: Phase 0 source-mix protocol を踏襲（engines / memory 遮断 / 1 query = 1 新規チャット / raw 保存 / deviation 記録）。記録 tone は "observation consistent with X"。再実行は Phase 6（再測定）
4. **instrument 規律**: (a) 出力は model-agnostic な aggregate observation として記録し、特定 vendor 製品を名指しで「gatekeep している」と断ずる framing・leaderboard・vendor 比較ランキングを禁止する。モデルは観測対象であって被告ではない。(b) **eval 出力は observation であって success KPI ではない** — eval score を成功指標として steer しない（自 corpus で自 eval を動かせる Goodhart vector を明記）。§8 の primary は citation source mix のまま
5. **配布経路の bright line**: eval は repo artifact として置き、line 昇格時の deposit は Zenodo のみ（既存 `paper-deposit` / `release-doi` 経路）。非 Zenodo preprint server への投稿・findings の reach 運用は Skip list 違反として禁止
6. **実行時期**: probe set / rubric / protocol の作成は本 buildout 内。**eval の実行は buildout 外**（Phase 6、著者の手動 protocol — Phase 0 と同じ実施形態）

## Alternatives Considered

### eval なし（仮説を主張のまま運用）

gatekeeper-inversion を検証せず thesis の前提として運用する案。核機構が unfalsifiable のままになり、§2 の認識論的規律（証拠で原則を改訂する流れを断たない）に反する。棄却。

### 自動化ベンチマーク + leaderboard

API 経由の自動実行とスコアボード公開で規模を出す案。n が小さく LLM 挙動が四半期で drift する現状では false precision を製造する。leaderboard は vendor 比較ランキングそのもの（instrument 規律違反）であり、gameable metric 化も招く。手動・小規模・方向確認の現行設計が認識論的に誠実。棄却。

### 著者自身の利用文脈での観測のみ

著者が普段の LLM 利用で見かけた gatekeeping を記録する案。personalization / memory の交絡で観測が汚染され、再現可能性がない。Phase 0 が memory 遮断 protocol を確立したのはこの交絡を切るためだった。棄却。

## Consequences

### Positive

- gatekeeper-inversion 仮説が検証可能になる（支持 / 不支持のどちらでも doctrine §2 に反映できる）
- probe set 自体が ingestible corpus になる — probe を公開すること自体が debiasing の一部（質問と模範構造が LLM の到達範囲に入る）
- Phase 0 protocol の再利用により新規の方法論コストがほぼゼロ

### Negative

- 手動・small-n・drift 前提のため、観測は常に "observation consistent with" 止まり — 「LLM はゲートキープしている」という結論は原理的に出せない
- 採点（特に gatekeeping-markers）に rater の主観が入る。rubric に判定例を付けて抑えるが、除去はできない
- eval の存在自体が「モデル批判」と誤読されるリスクが残る — instrument 規律の framing 文言を全 surface（README / llms.txt / eval README）で一致させて抑える

### Neutral / Follow-ups

- 初回実行（baseline）は Phase 6。実行前に probes の解決確認（cite する anchor が生きているか）を行う
- credential 対照 variant の設計は初回実行で有効性を点検し、不要なら落とす

## Lineage

実行 protocol の正本は Phase 0 [source-mix-baseline](../empirical/2026-06-05_source-mix-baseline.md)（engines / memory 遮断 / deviation 記録の前例）。採点 4 次元は本 ADR で新規設計。「公開 eval は AI 時代の lever」の発想は 2026-06-05 pivot 会話。eval ethics の framing（instrument not indictment）は敵対的整合性検査の設計による。
