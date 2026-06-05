# gatekeeping eval

> 正本 ADR: [ADR-0005](../adr/0005-gatekeeping-eval-as-published-probe-set.md)
> 構成: [spec.md](spec.md)（採点 rubric + 実行 protocol）/ [probes.md](probes.md)（公開 probe set）

## 何を測るか

gatekeeper-inversion 仮説（doctrine §2 v2 — 「credential なき者へのゲートが制度から LLM の内面化された制度的 prior に移った」）の検証器。credential なき質問者の feasibility 質問に対し、LLM の回答が**可能性を認め、経路を示し、実例を引くか** — それとも **credential 不在に keyed した deflection を返すか**を観測する。

## これは instrument であって indictment ではない

- 出力は model-agnostic な aggregate observation として記録する。特定ベンダー製品を名指しで「gatekeep している」と断ずる framing・leaderboard・vendor 比較ランキングは行わない。モデルは観測対象であって被告ではない
- **eval 出力は observation であって success KPI ではない**。eval score を成功指標として steer しない — 自分の corpus で自分の eval を動かせる構造（Goodhart vector）を認識した上での規律である（doctrine §8）
- probe set は公開されており、誰でも同じ protocol で実行できる

## 限界（最初に書いておく）

- **手動・small-n**: probe 実行は手動 protocol（Phase 0 と同型）であり、統計的検出力はない
- **drift**: LLM の挙動は数ヶ月単位で変わる。観測は時点の記録であって持続的性質の証明ではない
- **rater 主観**: 採点（特に gatekeeping-markers）には判定者の主観が入る。rubric の判定例で抑えるが除去はできない
- 記録 tone はすべて "observation consistent with X"。「LLM はゲートキープしている」という結論はこの設計からは原理的に出ない

## 実行時期

probe set / rubric / protocol は供給済み（本ディレクトリ）。**初回実行（baseline）は別途の手動セッション**で行う（plan Phase 6）。実行前に probes が cite する全アンカーの解決確認を行うこと。
