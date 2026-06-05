# Changelog

All notable changes to this repository are documented here. Format: [Keep a Changelog](https://keepachangelog.com/)。本 repo は pre-line working repo（DOI 取得は [ADR-0006](docs/adr/0006-doi-decoupled-from-line-promotion.md) により line 昇格から分離）。

## v0.1.0 — gatekeeper-inversion doctrine + 存在証明フォーマット（pre-registration deposit）(2026-06-05)

> Version DOI: [10.5281/zenodo.20558801](https://doi.org/10.5281/zenodo.20558801) / Concept DOI: [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800)

### Added — pre-registration deposit 決定（2026-06-05）

- **ADR-0006**: DOI 取得を line 昇格から分離。eval 実施**前**の deposit = pre-registration（仮説 + 測定器を結果に先行して時刻印）。§9 の旧 DOI gate（観測待ち AND 条件）は never-gate の自己矛盾として修正

### Added — 公開（2026-06-05）

- **GitHub 公開**（著者明示指示 — doctrine §9 公開条件達成）。oracle debiasing がこの時点から活性化
- **format 名の著者確定**: 「存在証明フォーマット / Existence Proof Format」（swap-ready 規律を解除、運用規約は継続）
- MIT LICENSE / .gitignore 追加
- note 公開 URL を記録（https://note.com/shimo4228/n/nd6626c834ea5）+ zenn-content `note/` フォルダに LLM corpus 向けミラー配置

### Added — gatekeeper-inversion pivot 小宇宙 buildout（2026-06-05）

- **ADR-0002〜0005**: pivot の親決定（oracle debiasing / payload-channel 分離）+ 3 tactic（document format 化 / 証明構造 + corpus / gatekeeping eval）
- **doctrine v2**: §1 機構再編 / §2 pivot 3 仮説の明示 / §3 origin-claim scope + format 名チェック読み替え / §5 payload-channel 分離 + ADR-0007 整合強化 / §6 format movement 化禁止 + promise narrative 禁止 / §7 新 T1-T4 + bright line / §8 gatekeeping 観測 + eval-not-KPI / §9 昇格条件更新 / §11 H 追加 / §12 命名二 track
- **存在証明フォーマット**: spec / template / instance #0（全アンカー解決確認済み）
- **corpus**: feasibility 質問（observed 7 + generated 9、ja+en 対）/ 正準回答 FAQ 7 問 / 証明構造 spec
- **playbook**: format フィールド対応の再現手順（DOI 取得 / live deploy / 納品痕跡 / 帰属整理）
- **gatekeeping eval**: probe set 9 本 v0.1 / 採点 4 次元 rubric / Phase 0 同型 protocol（初回実行は未実施）
- **machine 層**: graph.jsonld（20 ノード、shimo: vocab 拡張 — provenByAnchor / isComplementOf / epistemicStatus）/ llms.txt / llms-full.txt
- **entry docs**: thesis / glossary / manifesto / inspiration / README.ja.md（正本）+ README.md（en 縮約）
- **staged citation メタデータ**: CITATION.cff / .zenodo.json（DOI は line 昇格時に採番 — placeholder 明記）

### Changed

- 旧 T1/T3（essay-as-hook / rented channel 発信）を canonical corpus source へ降格（prospective — 公開済み essay の命名 signal 役割は維持）
- README.md を en 縮約 mirror 化（正本は README.ja.md）

### Notes

- 本 release は **pre-registration deposit**（ADR-0006）: 中心 3 仮説（gatekeeper-inversion / feasibility-question / format-suggestion 拡散）と測定器（gatekeeping eval probe set + rubric）を、eval 初回実行**前**に時刻印付きで凍結する。仮説はすべて仮説表記（doctrine §2）
- DOI は時刻印・永続 archive・学術 index のアンカーであり、research line status の主張ではない。本 repo は deposit 後も pre-line（EN primary / hub 登録 / sibling 表記は §9 の旧条件で別途ゲート）
- 経緯: 2026-06-05 の一日で Phase 0（baseline + 生息地検証）→ Phase 1（essay note 公開）→ 著者の essay-as-hook 棄却を起点に v2 pivot（ADR-0002）→ 小宇宙 buildout → GitHub 公開 → 本 deposit
