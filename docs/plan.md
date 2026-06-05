# plan — existence-proof 実行計画

> doctrine: [doctrine.md](doctrine.md)（判断の正本。本 plan は手順のみ）
> research: [research/2026-06-05_field-map.md](research/2026-06-05_field-map.md)
> 更新頻度: 高（Phase 完了ごとに状態列を更新）

## Phase 一覧

| Phase | 内容 | doctrine 参照 | 状態 |
|---|---|---|:---:|
| 0 | baseline 測定 + segment 生息地検証 | §2, §8 | ✅ 完了 (2026-06-05) |
| 1 | 命名確定 + defining essay | §3, §7 T1 | 🔄 命名確定済（独立峰）・essay 残 |
| 2 | Positioning 確定 + semantic signature 点検 | §4, §7 T5 | ⏳ 未着手 |
| 3 | README 人間ファースト化（Part B 吸収） | §7 T4 | ⏳ 未着手 |
| 4 | playbook artifact 整備 + 発信継続 | §7 T2, T3 | ⏳ 未着手 |
| 5 | 再測定 + 昇格判断 | §8, §9 | ⏳ 未着手 |

依存: 0 → 1 → 2 は順序必須（baseline なしの効果測定は不能、term なしの positioning は不完全）。3 は 1 完了後いつでも可。4 は 1-2 完了後。5 は 3-4 の実施から十分な観測期間（目安: 1-2 ヶ月）を置いて実行。

## Phase 0: baseline 測定 + segment 生息地検証

**目的**: 効果測定の起点固定と、層の実在仮説の最初の検証。

1. **source mix baseline**: regurgitation test を owned/earned/commercial 分類で実行・記録
   - probe 対象: ChatGPT / Perplexity / Gemini（graph-jsonld-validation で使った構成を踏襲）
   - probe query: 既存固有用語（AKC / Contemplative Agent / Authorship Strategy 等）+ 著者名
   - 記録先: `docs/empirical/`（新設）。tone は "observation consistent with"（doctrine §2 規律）
2. **earned mention 棚卸し**: 第三者による言及（blog / forum / SNS）を検索し、現状 ≈ 0 を確認・記録
3. **生息地検証**: AI-powered humans（仮称）がどこに集まるかの実在証拠収集
   - 探索先候補: HN / Reddit (r/ChatGPT, r/LocalLLaMA 等) / X / Discord / Zenn / note
   - 観測するもの: 「AI で初めて〜が作れた」型の一人称報告、credential なし作者の制度級成果物、自己同定的な語り
   - 成果物: 生息地マップ（どこに・どんな密度で・どんな語彙で存在するか）。**層が見つからない場合も結果として記録する**（仮説棄却は失敗ではない）

**完了記録（2026-06-05）**:

1. source mix baseline → [empirical/2026-06-05_source-mix-baseline.md](empirical/2026-06-05_source-mix-baseline.md)。owned 100% / earned 0（probe 条件: メモリー遮断、Perplexity は 2 query 上限の deviation あり）。AKC が最強 term、"Authorship Strategy" は単独 retrieval 不可（著者名 anchor で解決）
2. earned mention 棚卸し → [empirical/2026-06-05_earned-mention-inventory.md](empirical/2026-06-05_earned-mention-inventory.md)。observation consistent with ≈ 0。Attention-Not-Self の用語衝突（Ganeri 2017）を記録
3. 生息地検証 → [research/2026-06-05_habitat-map.md](../docs/research/2026-06-05_habitat-map.md)。**層の実在仮説を支持する観測**（ja 圏が最も厚い、外部アンカー付き 6+ 事例）。規模は依然仮説。自己記述語彙: ja は「非エンジニア」否定形アンカー（= 肯定形の名前が空いている）→ Phase 1 の造語候補生成への入力

## Phase 1: 命名確定 + defining essay

**目的**: recognition 軸の起点を作る。

1. 造語候補の生成（Phase 0 の生息地マップで観測された自己記述語彙を入力にする）
2. 隣接語差分表（doctrine §3 の表を候補ごとに拡張）で defensible scope を確認
3. **著者が確定**（命名は著者の authorial act。エージェントは候補と差分表まで）
4. defining essay 執筆: `writing-ecosystem`（essay-reviewer / fact-checker / AI-slop 検査）
   - 内容要件: 層の定義（3条件の交点）/ 仮説である旨 / グリフター境界 / 存在証明の論理 / 著者自身の一人称
   - ガード: 勧誘で終わらない。income claim ゼロ（doctrine §7 T1）
5. 公開（2026-06-05 改訂 — 旧: Zenn → 観測 → Substack）: **note（ja・新規アカウント）初出 + Substack（en, `ja-to-en-translation`）準同時**。Zenn は後続記事からの参照 hub。en term は衝突チェック → 著者確定を公開前に前倒し。スケール戦略は ja-first（[ADR-0001](adr/0001-japanese-first-scale-strategy.md)）。観測期待値: 観測期間の self-identification signal ≈ 0 は baseline-consistent（人間到達ほぼゼロからの開始 — doctrine §8）であり failure ではない
6. doctrine §3 の仮称を確定 term に置換、repo rename の要否を §9 条件に照らして記録

**進捗記録（2026-06-05）**: 手順 1-3 と 6 完了。(a) 前提整理として doctrine §2 を解像度上げ（条件1の成果物領域相対化 + 「制度級」定義固定 + Phase 0 結果反映）。(b) 候補 13 件 × 2 round 衝突チェック + 同 register 追加生成 6 案を経て、著者が**独立峰**を確定 — 全経緯は [research/2026-06-05_naming-candidates.md](research/2026-06-05_naming-candidates.md)。運用: 層・現象のカテゴリ名（自称を要求しない）。(c) doctrine 仮称置換 + §9 rename 判断（term 確定済・rename は line 昇格時）+ CLAUDE.md 同期済み。**残: 命名の再確定（再オープン — naming-candidates 引き継ぎ節が再開地点）→ essay の term 差し替え → 手順 5（note + Substack 準同時公開）**。essay 本文 v3 はレビュー 2 巡 + fact-check + textlint 通過済みで、term 差し替えのみで公開判定に進める状態

## Phase 2: Positioning 確定 + semantic signature 点検

**目的**: PBE 3次元の実体化と既存資産の branding 観点レビュー。

1. 5 line 各々の recognition 軸（何で思い出されるか）を1行で固定
2. プログラム全体の differentiation 文を確定（origin claim は固有用語の disciplinary scope に限定 — doctrine §3）
3. appeal の検証: Phase 1 essay への反応から「存在証明 + playbook」仮説を点検
4. semantic signature 点検（T5）: 固有用語が各 repo の llms.txt / graph.jsonld に載っているか確認。欠落のみ修正、新規生成はしない

## Phase 3: README 人間ファースト化（Part B 吸収）

**目的**: earned 言及から辿ってきた人間の着地点整備。

> 出自: human-channel SEO direction（memory: `human-channel-seo-direction-2026-05`）の Part B を本 plan が吸収（2026-06-05 決定）。事実の正本は memory 側、ここは手順のみ。

1. 対象: hub（shimo4228）+ 5 line repo の README.md / README.ja.md
2. `readme-writer` で人間ファースト化（構造 lint + ホリスティック review。audience = 独立峰の層を review の lens に渡す）
3. repo メタ整備: `gh repo edit` で description / topics。social preview は手動 checklist
4. 各 repo で `context-sync`（fact 一致検査 — cloaking 規約の機械的保証）
5. 制約: 「README は hygiene であり growth lever ではない」（ADR-0007）。ドラスチックに書き換えない。hub の No-volatile-state 規約遵守

## Phase 4: playbook artifact 整備 + 発信継続

**目的**: 再現可能性の供給（T2）と rented channel の継続運用（T3）。

1. playbook 第1号: 「どうやって学位なしで DOI-registered 研究プログラムを作ったか」の再現手順（既存 repo / skill / ADR が原料。新規制作は梱包のみ）
2. 以降の記事は `collect-context` → `writing-ecosystem` → Zenn / Substack の既存 pipeline
3. ガード: 投稿時刻最適化・ハッシュタグ戦略・バズ狙いタイトルはしない（doctrine §7 T3）

## Phase 5: 再測定 + 昇格判断

**目的**: 効果の方向確認と、skill 化 / line 化 / rename の go/no-go。

1. source mix 再測定（Phase 0 と同一手順・同一 probe 構成）
2. self-identification signal の棚卸し（コメント / 引用 / 派生 / 「これは自分だ」反応）
3. doctrine §9 の昇格条件に逐条照合し、go/no-go を記録
4. no-go の場合: どの仮説が支持されなかったかを doctrine §2 / §4 に反映（証拠で原則を改訂する流れを断たない — authorship-strategy empirical 規約の継承）

## 本 plan が参照する外部正本

- `~/.claude/skills/authorship-strategy/SKILL.md` — 禁止事項
- memory `authorship-strategy-judgments-shimo4228-2026-05` — Skip 確定 list
- memory `human-channel-seo-direction-2026-05` — Part B 詳細・cloaking 規約・clone:view baseline
- authorship-strategy ADR-0007 — metric 規約の正本
