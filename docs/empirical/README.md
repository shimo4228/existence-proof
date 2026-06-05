# empirical — 観測記録の index

> 規律: すべての記録は "observation consistent with X" tone（doctrine §2）。測定は方向性の確認であって効果の証明ではない（doctrine §8 caveat）

## 記録一覧

| 日付 | 記録 | 内容 |
|---|---|---|
| 2026-06-05 | [source-mix-baseline](2026-06-05_source-mix-baseline.md) | regurgitation test の owned / earned / commercial 分類 baseline。結果: owned 100% / earned ≈ 0。raw: probe-raw-{chatgpt,gemini,perplexity}.txt |
| 2026-06-05 | [earned-mention-inventory](2026-06-05_earned-mention-inventory.md) | 第三者言及の棚卸し。observation consistent with ≈ 0 |

## 測定系の対応関係（doctrine §8）

| 測定 | method 正本 | baseline | 再測定 |
|---|---|---|---|
| citation source mix（primary） | [source-mix-baseline](2026-06-05_source-mix-baseline.md) の protocol | 2026-06-05 | plan Phase 6 |
| gatekeeping 観測（parallel primary, v2） | [eval/spec.md](../eval/spec.md) | **未実施**（probe set 供給済み、初回実行は plan Phase 6 の手動セッション） | 同左 |
| self-identification / format 利用（secondary） | 受動観測（検索で見つかったものの記録のみ — 能動収集・registry 化は doctrine §6 禁止） | ≈ 0（2026-06-05） | 随時記録 |

## 記録の置き方

- 新しい run は `YYYY-MM-DD_<name>.md` + raw ファイルで追加する。既存記録は frozen（追記のみ、書き換えない）
- probe protocol の deviation（engine の仕様変更等）は必ず記録する — deviation の記録が時系列比較の前提になる
