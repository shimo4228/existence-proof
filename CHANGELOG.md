# Changelog

All notable changes to this repository are documented here. Format: [Keep a Changelog](https://keepachangelog.com/). 本 repo は pre-line（バージョン tag・DOI 未採番 — line 昇格時に v0.1.0 を起点とする予定）。

## [Unreleased]

### Added — gatekeeper-inversion pivot 小宇宙 buildout（2026-06-05）

- **ADR-0002〜0005**: pivot の親決定（oracle debiasing / payload-channel 分離）+ 3 tactic（document format 化 / 証明構造 + corpus / gatekeeping eval）
- **doctrine v2**: §1 機構再編 / §2 pivot 3 仮説の明示 / §3 origin-claim scope + format 名チェック読み替え / §5 payload-channel 分離 + ADR-0007 整合強化 / §6 format movement 化禁止 + promise narrative 禁止 / §7 新 T1-T4 + bright line / §8 gatekeeping 観測 + eval-not-KPI / §9 昇格条件更新 / §11 H 追加 / §12 命名二 track
- **存在証明フォーマット**（暫定名）: spec / template / instance #0（全アンカー解決確認済み）
- **corpus**: feasibility 質問（observed 7 + generated 9、ja+en 対）/ 正準回答 FAQ 7 問 / 証明構造 spec
- **playbook**: format フィールド対応の再現手順（DOI 取得 / live deploy / 納品痕跡 / 帰属整理）
- **gatekeeping eval**: probe set 9 本 v0.1 / 採点 4 次元 rubric / Phase 0 同型 protocol（初回実行は未実施）
- **machine 層**: graph.jsonld（20 ノード、shimo: vocab 拡張 — provenByAnchor / isComplementOf / epistemicStatus）/ llms.txt / llms-full.txt
- **entry docs**: thesis / glossary / manifesto / inspiration / README.ja.md（正本）+ README.md（en 縮約）
- **staged citation メタデータ**: CITATION.cff / .zenodo.json（DOI は line 昇格時に採番 — placeholder 明記）

### Changed

- 旧 T1/T3（essay-as-hook / rented channel 発信）を canonical corpus source へ降格（prospective — 公開済み essay の命名 signal 役割は維持）
- README.md を en 縮約 mirror 化（正本は README.ja.md）

### 経緯メモ

- 2026-06-05: Phase 0（baseline + 生息地検証）完了 → Phase 1（命名 + defining essay note 公開）→ 同日、著者の essay-as-hook 棄却を起点に v2 pivot（ADR-0002 Lineage 参照）
