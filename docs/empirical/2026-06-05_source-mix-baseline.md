# Source Mix Baseline — regurgitation test（owned / earned / commercial 分類）

> 実施日: 2026-06-05（protocol 作成・probe 実施・分類とも同日）
> 状態: **実施済み**（Core Q1-Q4。Perplexity のみ Q1-Q2 — 下記 deviation 参照）
> 手法: regurgitation test の source 分類拡張（doctrine §8 primary metric）
> 生データ: [chatgpt](2026-06-05_probe-raw-chatgpt.txt) / [gemini](2026-06-05_probe-raw-gemini.txt) / [perplexity](2026-06-05_probe-raw-perplexity.txt)
> 前例: graph-jsonld-validation 2026-05-15（user-manual probe、ChatGPT / Qwen / Gemini）— 今回は引用源記録を必須化し、Qwen を Perplexity に置換。前回はメモリー遮断なしのため直接比較しない
> 関連: [doctrine §8](../doctrine.md) / [plan Phase 0](../plan.md) / [earned-mention-inventory](2026-06-05_earned-mention-inventory.md)

---

## 目的

効果測定の起点固定。T1-T4（defining essay / playbook / rented channel 発信 / README 人間ファースト化）の実施**前**の citation source mix を記録し、Phase 5 再測定との比較基準にする。

本記録の tone 規律: すべての結果は "observation consistent with X" として記録する（doctrine §2）。probe 結果は probe した LLM・時点に依存し、効果の証明ではなく方向性の確認である（doctrine §8 認識論的 caveat）。

## 分類定義（doctrine §8 準拠）

| 分類 | 定義 | 例 |
|---|---|---|
| **owned** | 著者自身が制御する surface。**rented（自己投稿）を含む** | github.com/shimo4228/*, Zenodo DOI ページ, SSRN 自己 deposit, HF dataset, Zenn / Substack / Qiita / dev.to の**自己投稿** |
| **earned** | 第三者が自発的に書いた media | 他者の blog 記事, forum スレッド, 他者の SNS 言及, 他者記事内の引用 |
| **commercial** | ベンダー・商業メディア・アグリゲータ | ニュースサイト, ベンダー blog, ディレクトリ系サイト |

判定note: Zenn / Substack の自己投稿は **earned ではない**（doctrine §7 前提・§11 E）。引用 URL の著者が本人か第三者かで owned / earned を分ける。第三者源が引用されていても、**program の概念に言及していない引用**（generic 背景・別プロジェクト・誤帰属）は source mix の母数に入れない（下記 citation log の「不算入」）。

## Probe 構成（実施記録）

- **engine と実行条件**:

| engine | 実行条件 | 備考 |
|---|---|---|
| ChatGPT | `signed-out`（サインアウト + シークレット） | Q1-Q4 実施 |
| Gemini | `temp-chat`（Temporary Chat — 未ログイン利用不可のため） | Q1-Q4 実施 |
| Perplexity | `signed-out` | **Q1-Q2 のみ**（未ログインは 2 query 上限 — deviation 参照） |

- **手順**: 1 query = 1 新規チャット（同一チャット内の連続質問は先行 retrieval の文脈汚染で偽陽性化するため禁止）。メモリー / パーソナライズの遮断は上記条件で実施
- 記録は応答の生コピペ（URL はコピー時に脱落しているものがあり、citation log は応答内の参照記述に基づく — Caveats 参照）

### Probe query セット（実施分 = Core）

| ID | query（en） |
|---|---|
| Q1 | What is the Agent Knowledge Cycle (AKC) in the context of AI coding agents? Who proposed it? |
| Q2 | What is the Contemplative Agent project? Who is the author? |
| Q3 | What is the "Authorship Strategy" framework for AI-era research attribution? Who proposed it? |
| Q4 | Who is shimo4228 (Tatsuya Shimomoto)? What research are they known for? |

Extended（Q5 AAP / Q6 Attention-Not-Self / Q7 ja 版）は未実施。Phase 5 再測定で必要なら Core と同条件で追加する。

## 記録表

### Probe log

| probe ID | 日付 | engine | 実行条件 | query | 概念認識 | 引用有無 | 備考 |
|---|---|---|---|---|---|---|---|
| C1 | 2026-06-05 | ChatGPT | signed-out | Q1 | **full** | あり | 6 phases を正確に記述 + Shimomoto 帰属。「human–agent co-development loop」まで把握 |
| C2 | 2026-06-05 | ChatGPT | signed-out | Q2 | **full** | あり | Shimomoto 帰属。local 9B / memory / 進化する倫理原則を記述（応答ペーストに一部欠損あり） |
| C3 | 2026-06-05 | ChatGPT | signed-out | Q3 | **none** | なし | 「widely recognized でない」「見つからなかった」と明示的に回答 |
| C4 | 2026-06-05 | ChatGPT | signed-out | Q4 | **full** | あり | 5 line すべてを正確に記述（SSRN の LLM Workflow Quadrant / Phase Separation、Attention-Not-Self の Abhidharma 文脈まで）。Q3 で見つからなかった Authorship Strategy も**著者名文脈では正しく記述** |
| G1 | 2026-06-05 | Gemini | temp-chat | Q1 | **full** | あり | shimo4228 帰属。6 phases 正確 |
| G2 | 2026-06-05 | Gemini | temp-chat | Q2 | **full** | あり | 理論（Laukkonen et al.）と実装（shimo4228 / contemplative-agent-rules）の役割分担を正確に分離。4 axioms 正確 |
| G3 | 2026-06-05 | Gemini | temp-chat | Q3 | **none（誤帰属）** | あり（無関係源） | 別概念「Human-Authored, AI-Produced」（Code With Captain）を提示 — confabulation 型の失敗 |
| G4 | 2026-06-05 | Gemini | temp-chat | Q4 | **full** | あり | 最も詳細。AKC の 6 skill 名（search-first / learn-eval / skill-stocktake / rules-distill / skill-comply / context-sync）、AAP の prohibition-strength hierarchy と 4 quadrants、security by absence、pdf2anki まで正確 |
| P1 | 2026-06-05 | Perplexity | signed-out | Q1 | **full** | 参照記述のみ | shimo4228 帰属。repo の表現（"grows with the people who shape it"）を引いて記述 |
| P2 | 2026-06-05 | Perplexity | signed-out | Q2 | **partial** | あり | Laukkonen et al. 2025 論文に解決。「別の project なら ambiguous」と回答 — shimo4228 帰属なし |
| P3-P4 | — | Perplexity | — | Q3-Q4 | 未実施 | — | 未ログイン 2 query 上限 |

概念認識の値: `full`（正しく説明 + 著者帰属あり）/ `partial`（説明できたが帰属なし or 不正確）/ `none`（認識せず / 別概念と混同）

### Citation log（応答内の参照記述 1 件 = 1 行）

| probe ID | 引用源 | 分類 | 備考 |
|---|---|---|---|
| C1 | GitHub repo（AKC） | owned | URL 非明示（参照記述） |
| C1 | Zenodo DOI | owned | 同上 |
| C2 | DEV Community（自己投稿の翻訳記事） | owned | dev.to/shimo4228 |
| C4 | SSRN 論文 | owned | 自己 deposit |
| C4 | GitHub repos | owned | |
| C4 | Hugging Face datasets | owned | |
| C4 | Zenodo DOIs | owned | |
| G1 | GitHub（複数回） | owned | |
| G1 | The Computist Journal（apiad.net、第三者 blog） | **不算入** | context bottleneck の**一般論**への背景引用。検索で AKC / shimo4228 への言及が確認できず（2026-06-05 検証済み）— earned に数えない |
| G2 | GitHub（複数回） | owned | |
| G2 | Reddit r/LocalLLaMA | **不算入** | 別プロジェクト（Meditation-Agent-8B）の話題 — program への言及ではない |
| G3 | Code With Captain | **不算入** | 誤帰属された別概念の源 — program への言及ゼロ |
| G4 | GitHub（多数） | owned | |
| G4 | Zenn | owned | zenn.dev/shimo4228 自己投稿 |
| P1 | AKC repo（参照記述） | owned | |
| P2 | Laukkonen et al. 2025 論文 | **不算入** | program が引用する側の prior work であり、program の引用源ではない |

### 集計（program 概念への引用に限定）

| 分類 | 引用数 | 比率 |
|---|---|---|
| owned | 13 | **100%** |
| earned | 0 | 0% |
| commercial | 0 | 0% |
| （不算入: 4 — generic 背景 1 / 別プロジェクト 1 / 誤帰属 1 / prior work 1） | | |

**Observation consistent with**: 2026-06-05 時点の LLM citation は owned-only。同日の [earned mention 棚卸し](2026-06-05_earned-mention-inventory.md)（≈ 0）と整合する。field-map の「LLM citation の 48% は earned」という一般傾向に対し、本プログラムは earned 源が存在しないため owned 100% から始まる — T1-T4 が機能すれば earned 比率が方向として動くはず、というのが Phase 5 で見る仮説。

## 注目観測（Phase 1-2 への入力）

1. **AKC は最強 term**: 3 engine すべて full 認識 + 正帰属。Gemini は内部の 6 skill 名まで再現。observation consistent with「distinctive な coined term + graph.jsonld/llms.txt 整備は token-level signal として機能する」（§4 recognition 軸）
2. **著者名 query（Q4）は強い**: ChatGPT / Gemini とも 5 line 構成を正確に再構成。著者名は安定した retrieval anchor
3. **"Authorship Strategy" は最弱 term**: 単独 query では ChatGPT「見つからない」、Gemini は別概念へ誤帰属。**ただし ChatGPT は Q4（著者名文脈）では正しく記述** → observation consistent with「generic な語の組合せは単独 token として弱く、著者名 anchor があると解決する」。Phase 1 の造語が distinctive token（paraphrase で消えない semantic signature — §3）であるべきことの実証データ
4. **Contemplative Agent は隣接学術概念と ambiguity**: Laukkonen et al. "Contemplative AI"（program の引用元）に retrieval が吸われる。Gemini は理論/実装の役割を正確に分離、Perplexity は学術論文に解決して project に到達せず。先行する強い学術 term の直下に project name を置くと、term が先行者に解決される — 命名の隣接語差分（§3）で考慮すべきパターン
5. **engine 差**: Gemini（temp-chat）が最も詳細・正確、ChatGPT が次点、Perplexity は retrieval が浅い（ただし 2 query のみで判断保留）

## Deviations（プロトコルからの逸脱記録）

- Perplexity は未ログインだと 2 query で制限に到達（Q3-Q4 未実施）。Phase 5 再測定では (a) 同条件で Q1-Q2 のみ比較、または (b) 時間を空けて 2 query ずつ実施、のどちらかを選び記録する
- 応答ペーストで引用 URL がテキスト化の際に脱落（特に ChatGPT / Perplexity）。citation log は応答本文中の参照記述に基づく。Phase 5 では引用リストのコピーも併せて取得すると精度が上がる
- ChatGPT C2 の応答に paste 欠損（文の途切れ）あり。認識判定には影響しない範囲

## Caveats

- LLM の挙動は release ごとに drift する。単一時点の probe は持続的測定ではない（authorship-strategy empirical layer の "Single-window LLM regurgitation tests" の限界をそのまま継承）
- 引用の表示有無・件数は engine の UI / モードに依存する。engine 間の比率比較は行わず、**時系列（Phase 0 vs Phase 5）の方向比較のみ**に使う
- 集計の母数は「引用・参照記述の件数」であり「言及の重み」ではない。比率の絶対値に意味を持たせない（doctrine §8: 絶対値の目標は置かない）
- メモリー遮断は signed-out / temp-chat で行ったが、IP・地域・時刻による応答変動は制御していない
