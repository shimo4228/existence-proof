# ADR-0003: 存在証明の document format 化（registry なし・Nygard モデル）

> **Summary.** 存在証明を document format — 存在証明フォーマット（Existence Proof Format / EPF。名称は暫定 — [format-name-check](../research/2026-06-05_format-name-check.md)）— として定義する。spec + template + 著者自身の instance #0 の三点 set。**中央 registry・instance 集約・community を持たない。** 伝播は LLM の format-suggestion による self-service のみ（仮説的機構）。

## Status

accepted

## Date

2026-06-05

## Context

人ラベル（独立峰）は構造チェックを全通過した上で **sayability / 文中試用テストで suspend** となった（[naming-candidates](../research/2026-06-05_naming-candidates.md) 再オープン節）。失敗の根本原因は人ラベルに内在する **identity cost** である — 「私は独立峰だ」は自称の大仰さを避けられない。層の自己記述が謙遜形（「非エンジニア」否定形アンカー — habitat-map §4）であることとも衝突する。

一方、**document format のラベルには identity cost がない**。「ADR を書いた」と言うのに「私はアーキテクトだ」と名乗る必要がないのと同じく、「存在証明フォーマットで自分の事例を書いた」は真顔で言える。

format 伝播の前例として Nygard の ADR（2011）がある: blog post 1 本と template だけが置かれ、community も registry も勧誘もなしに、有用性だけで伝播した。現在では LLM が ADR を知っており、頼まれなくても提案する。**format は AI 時代において LLM の format-suggestion を介して伝播しうる**（仮説的機構 — doctrine §2 v2）。これは ADR-0002 の oracle debiasing と接続する: feasibility 質問に対し LLM が「実例がある。この format で自分の事例を記録した人がいる」と答えられる状態を作る。

先約との調整: naming-candidates Round 1 の確定判断「存在証明は gloss に留め、固有名は別 token」は**人を指す固有名**についての判断であり、document-type 複合語「存在証明フォーマット」内の「存在証明」は gloss（記録内容の記述）として機能するため先約を覆さない。詳細と衝突チェック結果は [format-name-check](../research/2026-06-05_format-name-check.md)。

## Decision

1. **三点 set の公開**: `docs/format/` に spec.md（フォーマット仕様）+ template.md（空欄 template）+ instance-0.md（著者自身の worked example — 公開済み essay の素材から再構成）を置く
2. **核となる規則 — claim→anchor 連鎖**: すべての能力 claim は、第三者が claimant の協力なしに検証できる anchor（解決する DOI / live URL / 納品物）で終端しなければならない。anchor のない claim は format 外
3. **movement 化の構造的禁止**: (a) 中央 registry / instance 一覧を作らない・運営しない、(b) 他者 instance の集約・showcase・curation をしない、(c)「参加」「登録」「提出」の概念を持たない、(d) template は著者に層ラベルの自称を要求しない（自分が何であるかの欄は任意かつ空欄可）。この 4 点は doctrine §6 v2 と **spec 自身の Non-goals 節**の両方に置く — spec は doctrine の外へコピーされて使われるため、guard が artifact に随伴する必要がある
4. **名称は暫定 + swap-ready**: 「存在証明フォーマット（Existence Proof Format）」を暫定名とし、各ファイル初出でフル名 + 暫定 note、以降 EPF。bare 略語「EPF」を primary token にしない（Employee Provident Fund 等と混雑 — format-name-check）。最終確定は著者の authorial act（doctrine §3）

## Alternatives Considered

### 人ラベル + manifesto（命名の再挑戦）

layer 名を確定させ、その名のもとに manifesto 的文書を出す案。sayability 失敗が token 差し替えでは解消しないこと（寒さの発生源は token → 構文位置 → cadence と精密化済み — plan Phase 1 記録）、および manifesto が movement register に接近することから棄却。

### registry 付き format（instance 一覧の運営）

format に公式 instance 一覧を付け、採用を可視化する案。registry は事実上の会員名簿（§6 membership 禁止違反）であり、instance 数という gameable metric を生み（ADR-0007 違反の变形）、「登録」概念が勧誘 incentive を生む。三重に棄却。

### skill 化（format を Claude skill として配布）

format を skill として実装する案。doctrine §9「判断軸が実適用で安定する前に skill 化しない」に反する。また spec を md 文書として置く方が tool-agnostic（authorship-strategy Layer 4）。format が実適用で安定した後の検討事項として保持。棄却（現時点）。

## Consequences

### Positive

- identity cost ゼロの伝播 token を得る。layer 命名（suspend 中）がブロッカーでなくなる
- 「format を書き終えること」が playbook の実行と一致する（anchor の取り方 = DOI 取得手順… — T3 が T1 に従属する構造）
- format 名は token-level で検索可能であり、derived instance の出現は受動的に観測できる（能動収集はしない — §6 v2）
- instance #0 が doctrine §5 の worked example を機械検証可能な形で兼ねる

### Negative

- registry なしの format には組み込みの採用 signal がない（設計通り — 観測は eval と source-mix 再測定で行う）
- format-suggestion による伝播は未検証の仮説的機構であり、LLM が本 format を提案するようになるには公開 + corpus 蓄積が前提
- 「存在証明」bare token の混雑（楽曲・哲学）は複合語には及ばないが、希釈圧として残る

### Neutral / Follow-ups

- format 名の著者最終確定が pending（buildout 完了時に候補表を提示）
- 著者以外の instance が出現した場合、それは §8 secondary signal の最強形であり、§9 昇格条件の入力になる

## Lineage

構造モデルは Nygard "Documenting Architecture Decisions"（2011）— spec + template + worked example、community なしの format 伝播の前例。instance #0 の素材は defining essay（v8、note 公開 2026-06-05）の §私もその一人である・§一人いれば、存在は証明される・§これは「AI で稼ぐ」話ではない。「format ラベルには identity cost がない」の洞察は 2026-06-05 の pivot 会話で、独立峰 sayability 失敗の根本原因分析から導かれた。
