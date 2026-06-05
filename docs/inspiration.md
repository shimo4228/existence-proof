# Inspiration — 系譜と素材

> 本 doctrine がどこから来たかの記録。prior art の明示は origin-claim scope discipline（doctrine §3）の一部でもある。

## 構造のモデル

- **Nygard, "Documenting Architecture Decisions" (2011)** — document format が community・registry・勧誘なしに有用性だけで伝播した前例。spec + template + worked example の三点 set、および「format ラベルには identity cost がない」という観察の源。存在証明フォーマット（ADR-0003）の直接のモデル
- **authorship-strategy repo** — doctrine 書式（thesis / glossary / manifesto / ADR + Lineage / llms.txt / graph.jsonld / empirical layer）の構造モデルであり、本 doctrine の補完相手（同一インフラ・別 payload・別受益者 — doctrine §5 v2）。`shimo:` vocabulary の正本

## 理論的素材

- **PBE（Personal Brand Equity）**: Gorbatov et al. (2021)、MDPI (2025) — appeal / differentiation / recognition の 3 次元（doctrine §4。研究プログラムへの transfer は仮説）
- **authenticity 緊張**: Gershon (2016)、Pagis (2017) — 戦略的自己呈示と authentic self の本質的緊張（doctrine §6 の設計課題化の根拠）
- **witness（数理論理）** — ∃x の立証実例。存在証明の説明論理の精密版（essay §一人いれば、存在は証明される）
- **earned 48% finding** — LLM citation の plurality は earned media（Omniscient Digital ほか — field-map §3）。v1 の earned-channel 設計の根拠であり、v2 でも「使った者の成果報告が最強の earned 生成器」として残る

## prior art（origin claim を立てない領域）

- **algorithmic gatekeeping** 文献（Napoli 等）/ **AI fairness・debiasing** 研究 / 「LLM as gatekeeper」言説 — gatekeeper-inversion・oracle debiasing の構成要素はすべてここに先行する。claim は交点 composite のみ（doctrine §3 v2）
- **隣接概念**: centaur (Kasparov) / cyborg (Mollick) / vibe coding (Karpathy) / citizen developer / 在野研究者 / 当事者研究（浦河べてるの家） — 差分表は doctrine §3。当事者研究は「非 credential 者による一人称知識生産の確立済み方法論」として最近接の dignified 系譜

## 観測素材（一次資料）

- **habitat-map（2026-06-05）** — ja 圏 7 事例 + en 圏 2 事例の一人称報告（外部アンカー付き）。「非エンジニア」否定形アンカーの発見（= 肯定形の空席）が命名作業全体の起点
- **defining essay（note 公開 2026-06-05）** — 層の 3 条件・グリフター境界・存在証明の論理・著者の一人称を articulate した v1 時代の主 artifact。v2 では canonical corpus source + instance #0 の素材として保持（ADR-0002 — prospective 降格）

## 命名の物語（要約）

人ラベル 13 候補 × 4 round（gateless 系の全滅 → near-empty token 原則 → 独立峰確定 → **文中試用テストで suspend**）の全経緯は [naming-candidates](research/2026-06-05_naming-candidates.md)。この失敗の根本原因分析（identity cost は人ラベルに内在する）が「format に名前を与える」という v2 の転回（ADR-0003）を生んだ — 失敗が設計を進めた例として記録する。

## v2 pivot の経緯（2026-06-05）

essay note 公開の直後、著者が essay-as-hook 機構自体を棄却（「AI 時代ならではの人間向け戦略でないと面白くないし効果もない」）。同日の構造分析が taste を支持し（pre-AI content marketing との同型性・4 設計特性の不在）、「この層の発見面はチャット窓である」という観察から gatekeeper-inversion 仮説と oracle debiasing 機構が導かれた。敵対的整合性検査が payload/channel 分離を発見し、既存規約（象限不可侵・ADR-0007・Skip list）との整合が確定した。全 decision は ADR-0002〜0005。
