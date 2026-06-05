# Glossary — 用語集

> 各項目は本 repo 内での定義を示す。より広い一般用法と局所定義が乖離する場合はその旨を明記する（disambiguation）。
> 命名の状態は二 track（[doctrine §12](doctrine.md)）— layer 名 suspend / format 名確定（2026-06-05）。

## ゲートキーパー反転（gatekeeper inversion）【仮説】

credential なき者へのゲートキーピングが、制度（大学・学会・企業）から **LLM の内面化された制度的 prior** に移るという仮説。[gatekeeping eval](eval/README.md) の検証対象であり、本 repo 内で事実として書かれることはない。**origin claim なし** — algorithmic gatekeeping・AI fairness 文献に prior art が厚い（doctrine §3 v2）。

## 内面化された制度的 prior（internalized institutional prior）

LLM が制度的テキストから学習した「制度級の産出には制度的 credential が前提」というパターン。credential なき質問者への deflection（「通常は大学院で…」）として表面化しうる。eval の D4 次元で**観測**する（断定しない）。

## oracle debiasing

本 doctrine の機構: 機械検証可能な存在証明と playbook を、LLM が feasibility 質問を評価する面に供給すること。供給（制御可能）と採否（制御不能・操作しない）を峻別する。**debias の一般語義（モデル内部のバイアス除去技術）とは別物** — ここでは「根拠を供給して回答の前提を変える」の意。

## 存在証明（existence proof）

「ある類のものが存在する」という命題を、条件を満たす実例**一つ**で証明する論理（数理論理の witness = ∃x の立証実例）。本 repo では**説明論理（gloss）であって人を指す固有名ではない**（doctrine §3 分業）。disambiguation: 哲学の「神の存在証明」、blockchain の文書公証サービス「Proof of Existence」（語順が逆・意味も別 — あちらは文書のタイムスタンプ公証）とは別物。

## 存在証明フォーマット（Existence Proof Format）

credential なき者による制度級産出の事例を記録する document format（[spec](format/spec.md)）。Nygard の ADR をモデルに spec + template + worked example で供給され、**中央 registry・instance 集約・参加概念・自称要求を持たない**。略語 EPF は文書内 2 回目以降のみ。名称は 2026-06-05 著者確定（衝突チェック記録: [format-name-check](research/2026-06-05_format-name-check.md)）。

## 主張→アンカー連鎖（claim-anchor chain）

format の核規則: すべての能力主張は、第三者が書き手の協力なしに検証できるアンカー（解決する DOI / live URL / 納品先側の痕跡）で終端する。**アンカーが解決しなくなった主張は失効し、削除義務を負う** — 証明は構造的に falsifiable である。

## 機械検証可能な証明構造（machine-verifiable proof structure）

存在証明の JSON-LD 還元形: `affiliation` フィールドを**意図的に持たない** Person → created → 解決する識別子付き成果物（[proof-structure](corpus/proof-structure.md)）。不在は「無所属」という値ではなくフィールドの不在で表現する。

## feasibility 質問（feasibility question）

credential なき者が産出の前に抱きうる疑いの質問形。3 種の不安に対応する — 許可（出してよいか）・価値（価値があるか）・帰属（自分のものと言えるか）。corpus は [questions.md](corpus/questions.md)。「層がこれを LLM に発する」は仮説（feasibility-question 仮説 — doctrine §2 v2）。

## gatekeeping eval

gatekeeper-inversion 仮説の測定器（[spec](eval/spec.md)）: 公開 probe set + 採点 4 次元（feasibility-acknowledgment / concrete-path / example-citation / gatekeeping-markers）+ 手動 protocol。**instrument であって indictment ではない** — vendor 比較・leaderboard・KPI 化を禁止。

## instance #0

format の worked example 第 0 号 = 著者自身の事例（[instance-0](format/instance-0.md)）。doctrine の「abstract doctrine + worked implementation ペア」の worked 側を機械検証可能な形で兼ねる。

## 制度級（institution-grade）

従来その産出に制度的訓練・所属・資格が事実上前提とされてきた**類**の成果物で、第三者検証可能な外部アンカーを伴うもの（定義固定 2026-06-05 — doctrine §2）。成果物の「類」の主張であり、規模・品質・human peer review 通過の主張ではない。

## payload / channel 分離

v2 の境界原理（doctrine §5）: 本 doctrine の固有物はチャネル（2×2 マップのセル）ではなく payload（エンパワーメント artifact）。既存エコシステムのチャネルインフラを再所有せず通過利用し、新規チャネルを自前で積み増さない。

## 独立峰【suspend 中 — 定義しない】

layer 名の一時確定 token（2026-06-05 同日 suspend — 文中試用テスト失敗）。本項は suspension の記録であって live な定義ではない。経緯・再開地点: [naming-candidates](research/2026-06-05_naming-candidates.md)。en calque "freestanding peak(s)" も連動 suspend。

## earned / owned / rented

earned = 他者が自発的に書く media（直接生成不能）。owned/rented = 自分の repo / 自己投稿（note・Zenn・Substack 含む）。**自己投稿を earned と呼ばない**。LLM の format-suggestion による拡散も earned ではない（LLM-mediated channel — 区別の正本は doctrine §7 / §11 E）。
