# format 名衝突チェック — 「存在証明フォーマット」(暫定)

> 実施日: 2026-06-05
> 文脈: gatekeeper-inversion pivot（[ADR-0002](../adr/0002-gatekeeper-inversion-strategic-reframe.md)）の F1 工程。document format（[ADR-0003](../adr/0003-existence-proof-as-document-format.md)）の暫定名チェック
> 関連: [naming-candidates](2026-06-05_naming-candidates.md)（layer 名の経緯 — **本チェックとは別 object**）

---

## 前提: format 名は人ラベルとは別の命名問題

layer 名（独立峰 — suspend 中）と format 名は別 object である。人ラベルは identity cost（自称の大仰さ・sayability）で失格したが、**document-type label には identity cost がない** — 「ADR を書いた」と言うのに「私はアーキテクトだ」と名乗る必要がないのと同じ。「存在証明フォーマットで書いた」は真顔で言える。

### 4 点チェックの format 名向け読み替え

| 検査 | 人ラベル版 | format 名版 |
|---|---|---|
| ①衝突チェック | near-empty token（ja/en 個別） | **不変（binding）** |
| ②sayability | 当事者が謙遜文化で自称可能か | 「『〈format〉を書いた』と言えるか」 |
| ③文中試用 | 命名文・自称・結びの 3 形 | spec / prose 内試用（自称形は不適用） |
| ④グリフター register | 不変 | **不変** |

## 先約との調整: 「存在証明は gloss に留める」(naming-candidates Round 1 学び 4)

先約の内容: **人を指す固有名**を「存在証明（者）」にしない — bare token は数学イディオム + 楽曲群で paraphrase-prone / 混雑のため。固有名は別 token（→ 独立峰系へ）、存在証明は説明論理として保持。

**本 format 名はこの先約を覆さない**: 複合語「存在証明フォーマット」内の「存在証明」は gloss（このフォーマットが記録する内容の記述）として機能しており、人を指す固有名への昇格ではない。ADR が "Architecture Decision Record" という純記述名から使用を通じて固有名化した前例と同型。ただし先約の運用に隣接するため、**著者の最終確定を要する**（暫定 + swap-ready で建造）。

## 衝突チェック結果（2026-06-05 実施）

### ja「存在証明フォーマット」— 複合語の直接占有なし ✅

検索 hit はすべて bare「存在証明」: 神の存在証明（哲学）/ 辞書義 / 劇団俳優座公演『存在証明』/ note 哲学記事。**複合語としての先住者ゼロ**。bare token の混雑（楽曲群含む）は複合語には及ばない — 「決定」が混雑していても "Architecture Decision Record" が機能するのと同じ構造。

### en "Existence Proof Format" — 固有名占有なし ✅

hit は数学教育の一般記述のみ（「existence proof の書き方・format」— Tricki / Whitman / Study.com 等）。固有 format 名・製品・ブランドとしての使用ゼロ。**数学の existence proof（witness / ∃x）隣接はむしろ意味的補強** — doctrine の説明論理（一人でも実例があれば類は証明される）と同根。

### 略語 "EPF" — 混雑 ⚠️（運用規約で対応）

Employee Provident Fund（印・馬の年金制度 — en-Asia 圏で巨大 token）/ Encapsulated PostScript File / Eclipse Process Framework（dev 隣接）/ Engineering, Procurement and Fabrication。**bare 略語を primary token にしない**:

- 初出は必ずフル名（ja「存在証明フォーマット」/ en "Existence Proof Format"）
- 略語は同一文書内の 2 回目以降のみ。文書冒頭で gloss 必須
- 検索・retrieval の semantic signature はフル complex に持たせる（略語に依存しない）

### 隣接 token "Proof of Existence" — 語順逆の別物 ⚠️（glossary で disambiguation）

blockchain 公証サービス（proofofexistence.com / poex.io / bloxberg、2013-）が「Proof of Existence」を占有。**意味も別物**: あちらは「この文書がこの時刻に存在した」のハッシュ公証、こちらは「この類の人が存在する」の witness 記録。語順（"Existence Proof" vs "Proof of Existence"）が token を分離するが、glossary に disambiguation 項目を置く。

### ②sayability / ③文中試用 / ④グリフター register

- 「存在証明フォーマットで自分の事例を書いた」— 真顔で言える（identity cost なし）✅
- spec 内試用: 「存在証明フォーマット（EPF）の必須フィールドは…」「これは EPF instance である」— 機能する ✅
- グリフター register: 数学・論理の register はハッスル語彙から最遠。reject 済み候補（permissionless 等）のような empowerment 一般形容詞の植民地帯に入らない ✅

## 代替候補トリアージ（著者確定用）

| 候補 | 判定 | 根拠 |
|---|---|---|
| **存在証明フォーマット / Existence Proof Format**（暫定採用） | ✅ viable | 上記の通り。複合語 near-empty、記述的で ADR 前例と同型、gloss 先約と整合 |
| 存在証明レコード / Existence Proof Record (EPR) | △ | "Record" register は ADR 家族と最も近い。ただし略語 EPR が Electronic Patient Record（医療で巨大）+ EPR パラドックス（物理）に占有され、略語衝突がフル名の想起にまで干渉する懸念 |
| 存在記録 / Existence Record | ✗ | 「証明」（claim→anchor の検証可能性）が落ちる。format の核心が名前から消える |
| witness record / ウィットネスレコード | ✗ | ja で不可読 loanword。著者 taste signal（proof/witness 系は「むずい」）にも反する |

## 判定

**暫定名「存在証明フォーマット（Existence Proof Format）」で建造続行** — binding の①を通過、②③④も format 名版で通過。全 artifact に swap-ready 規律（初出フル名 + 暫定 note、以降 EPF）を敷く。**著者の最終確定は buildout 完了時の候補表提示で行う**（命名は authorial act — doctrine §3）。
