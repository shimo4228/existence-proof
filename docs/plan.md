# plan — existence-proof 実行計画 v2

> doctrine: [doctrine.md](doctrine.md)（判断の正本。本 plan は手順のみ）
> v2（2026-06-05）: gatekeeper-inversion pivot（[ADR-0002](adr/0002-gatekeeper-inversion-strategic-reframe.md)〜[0005](adr/0005-gatekeeping-eval-as-published-probe-set.md)）により Phase 2 以降を再編。旧 plan の Phase 0-1 記録は下に凍結保持
> 更新頻度: 高（Phase 完了ごとに状態列を更新）

## Phase 一覧（v2）

| Phase | 内容 | doctrine 参照 | 状態 |
|---|---|---|:---:|
| 0 | baseline 測定 + segment 生息地検証 | §2, §8 | ✅ 完了 (2026-06-05) |
| 1 | 命名 + defining essay（v1 時代） | §3, §12 | 🔄 essay ja 公開済・**役割は corpus source へ prospective 降格**（ADR-0002）・layer 命名 suspend 継続 |
| 2 | pivot doctrine（ADR-0002〜0005 + doctrine v2 + §11 A-H） | §1-§12 | ✅ 完了 (2026-06-05) |
| 3 | 存在証明フォーマット（spec / template / instance #0） | §7 T1 | ✅ 完了 (2026-06-05) |
| 4 | corpus + 証明構造 + playbook + eval spec | §7 T2-T4 | ✅ 完了 (2026-06-05) |
| 5 | machine 層 + entry docs（graph.jsonld / llms / thesis / README / staged citation） | §5, §7 | ✅ 完了 (2026-06-05) |
| 6 | 再測定 + 昇格判断（著者ゲート） | §8, §9 | ⏳ 未着手 |

## Phase 6: 再測定 + 昇格判断（次の実行単位）

**著者の判断・手動作業を要する項目のみが残っている**:

1. ~~format 名の著者最終確定~~ → ✅ **確定（2026-06-05）: 存在証明フォーマット**（[format-name-check 確定記録](research/2026-06-05_format-name-check.md)）
2. ~~GitHub 公開の go/no-go~~ → ✅ **公開済み（2026-06-05、著者明示指示）**。MIT LICENSE 追加・README Status 更新・rename は不要（§9 — rename は line 昇格と同時）
3. **gatekeeping eval 初回実行（baseline）**: [eval/spec.md](eval/spec.md) の手動 protocol（Phase 0 と同じ実施形態 — 著者がブラウザで probe 実行、raw を `docs/empirical/` に保存）。実行前に probes の cite anchor 解決確認
4. **source-mix 再測定**: Phase 0 と同一手順・同一 probe 構成。公開から十分な観測期間（目安 1-2 ヶ月）を置く
5. **昇格判断**: §9 の条件に逐条照合（line 化 = EN primary / hub / sibling、skill 化、rename — DOI は取得済み 2026-06-05、ADR-0006 で分離）。no-go の場合はどの仮説が支持されなかったかを §2 に反映（仮説棄却は失敗ではない）

### 記録済み（旧・著者入力待ち）

- **note 公開 URL（記録 2026-06-05）**: https://note.com/shimo4228/n/nd6626c834ea5 。LLM corpus 向けミラー: `~/MyAI_Lab/zenn-content/note/non-engineer-no-name-yet.md`（substack/ と同じ Zenn 規約除外フォルダ）
- Substack en の扱い: pivot で優先度降格（canonical en source としての価値は残る — ADR-0002 Decision 4）。実施は著者判断

### housekeeping backlog（spearhead ではない — §7 v2）

- 旧 T4: hub + 5 line repo の README 人間ファースト化（Part B — 正本: memory `human-channel-seo-direction-2026-05`）
- 旧 T5: 固有用語の semantic signature 点検（各 repo の llms.txt / graph.jsonld）— 本 repo 分は Phase 5 で完了。他 repo 分のみ残

---

## 凍結記録: v1 Phase 0-1（書き換えない）

### Phase 0: baseline 測定 + segment 生息地検証（✅ 2026-06-05）

1. source mix baseline → [empirical/2026-06-05_source-mix-baseline.md](empirical/2026-06-05_source-mix-baseline.md)。owned 100% / earned 0（probe 条件: メモリー遮断、Perplexity は 2 query 上限の deviation あり）。AKC が最強 term、"Authorship Strategy" は単独 retrieval 不可（著者名 anchor で解決）
2. earned mention 棚卸し → [empirical/2026-06-05_earned-mention-inventory.md](empirical/2026-06-05_earned-mention-inventory.md)。observation consistent with ≈ 0。Attention-Not-Self の用語衝突（Ganeri 2017）を記録
3. 生息地検証 → [research/2026-06-05_habitat-map.md](research/2026-06-05_habitat-map.md)。**層の実在仮説を支持する観測**（ja 圏が最も厚い、外部アンカー付き 6+ 事例）。規模は依然仮説。自己記述語彙: ja は「非エンジニア」否定形アンカー

### Phase 1: 命名 + defining essay（v1 時代の記録）

- 候補 13 件 × 4 round の衝突チェック → 著者確定「独立峰」→ **文中試用テストで同日 suspend**。全経緯: [research/2026-06-05_naming-candidates.md](research/2026-06-05_naming-candidates.md)
- essay v8（タイトル: 「非エンジニアの私が」の先に、名前はまだなかった — term 非依存設計）を note に公開（2026-06-05、新規アカウント、タグ: 非エンジニア/生成AI/個人開発/独学/エッセイ、カバー画像設定済み。URL: https://note.com/shimo4228/n/nd6626c834ea5 — 記録 2026-06-05）
- 2026-06-05 公開判定変更（著者決定）: 命名確定を公開のハード依存から外し「あれこれ悩む前に出す」を採用
- **v2 での役割変更**（ADR-0002 — prospective）: essay は spearhead から canonical corpus source へ。命名 signal 観測の役割は維持（遡及破壊しない）。新規 essay の cadence 義務は消滅

---

## 本 plan が参照する外部正本

- `~/.claude/skills/authorship-strategy/SKILL.md` — 禁止事項
- memory `authorship-strategy-judgments-shimo4228-2026-05` — Skip 確定 list
- memory `human-channel-seo-direction-2026-05` — Part B 詳細・cloaking 規約・clone:view baseline
- authorship-strategy ADR-0007 — metric 規約の正本
