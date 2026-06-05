# Earned Mention 棚卸し — 2026-06-05

> 実施日: 2026-06-05
> 手法: web 検索 12 query（固有用語群 + 著者名 + coined sub-term + DOI、site 指定含む）。ヒットした候補は一次ソースを直接 fetch して引用有無を検証
> 目的: doctrine §8 baseline「earned mention ≈ 0」の実地確認（plan Phase 0 タスク 2）
> 関連: [doctrine §8](../doctrine.md) / [source-mix-baseline](2026-06-05_source-mix-baseline.md)

---

## 結論

**Observation consistent with earned mention ≈ 0**（2026-06-05 時点）。固有用語群（Agent Knowledge Cycle / Contemplative Agent / AAP / Authorship Strategy / Attention-Not-Self / Security by Absence）と著者名（shimo4228 / Tatsuya Shimomoto）のいずれでも、第三者が自発的に書いた言及（blog / forum / SNS / 学術引用）は発見されなかった。発見されたものはすべて owned surface（自 repo / 自己投稿記事）だった。

## 検索クエリと結果

| # | query | 結果 |
|---|---|---|
| 1 | `"Agent Knowledge Cycle" shimo4228` | own GitHub repo + Zenn 自己投稿 + arXiv 2 件（→ 下記「検証済み・棄却」） |
| 2 | `"Contemplative Agent" shimo4228 OR Shimomoto` | own GitHub repo のみ（他は同姓の無関係人物） |
| 3 | `"Attention-Not-Self" research` | **全件 Jonardon Ganeri の同名著書（2017, OUP）**（→ 下記「用語衝突」） |
| 4 | `shimo4228`（単独） | own GitHub profile / repos + dev.to 自己投稿群 |
| 5 | `shimo4228 site:news.ycombinator.com OR site:reddit.com` | **0 件** |
| 6 | `"agent-knowledge-cycle" -site:github.com -site:zenn.dev -site:dev.to` | own repo（除外漏れ）+ 無関係の一般概念記事のみ |
| 7 | `shimo4228 site:zenn.dev OR site:note.com OR site:qiita.com` | Zenn / Qiita 自己投稿のみ（第三者言及なし） |
| 8 | `"Contemplative Constitutional AI" agent implementation` | own dev.to 自己投稿 + Laukkonen et al. 2025（**引用元** — 本プログラムが引用する側）+ 無関係 |
| 9 | `"Authorship Strategy" + AI attribution 系` | 無関係の学術論文・特許のみ |
| 10 | `"Security by Absence" AI agent` | **0 件**（一般的 AI security 記事のみ。第三者使用なし） |
| 11 | `"Agent Knowledge Cycle" 日本語 記事 解説` | 無関係（Zendesk / Google Cloud の一般記事、arXiv 同上） |
| 12 | `zenodo.20263316 OR "agent attribution practice"` | 無関係の attribution 研究のみ。DOI 直接言及 0 件 |

## 検証済み・棄却（誤認防止）

検索 #1 / #11 で arXiv 2 論文がヒットしたが、**PDF 本文 + References を直接確認し、いずれも引用・言及なしを確認**（検索エンジンの意味的マッチによる偽陽性）:

- arXiv:2603.10808 "Nurture-First Agent Development"（Zhang）— "Knowledge Crystallization Cycle" という類似概念を含むが AKC への言及なし
- arXiv:2603.14805 "Knowledge Activation"（AKU 概念）— 言及なし

将来の棚卸しで同じ 2 論文がヒットしても earned に数えないこと。なお、隣接概念（agent の知識ライフサイクル管理）が独立に学術文献化しつつあることは Phase 1 の隣接語差分表の入力になりうる。

## 用語衝突の記録

- **Attention-Not-Self**: Jonardon Ganeri *Attention, Not Self*（2017, Oxford University Press）が検索結果を占有する。この term は web 検索上は一意に owned ではない。source mix probe（Q6）でこの term を使う場合、応答が Ganeri を指すか本プログラムの research line を指すかを区別して記録すること

## 観測された owned footprint（参考）

検索で到達可能だった自己 surface（earned ではない）: github.com/shimo4228/*（repos + profile）/ zenn.dev/shimo4228（ja + en locale）/ qiita.com/shimo4228 / dev.to/shimo4228。dev.to の en 記事群が検索面で比較的目立つ。

## Caveats

- 検索 index は US 中心（使用した検索ツールの制約）。日本語圏（note / はてな / 個人 blog）のカバレッジは不完全であり、「ja 圏で 0」の確度は en 圏より低い
- X / Discord は login 壁のため検索不能。これらのプラットフォーム上の言及は本棚卸しでは観測できない
- 本記録は 2026-06-05 時点のスナップショット。検索エンジンの index 遅延により、直近の言及は写らない可能性がある
- 「発見されなかった」は「存在しない」の証明ではない（doctrine §8 認識論的 caveat と同じ規律）
