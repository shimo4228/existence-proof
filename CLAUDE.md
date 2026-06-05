# existence-proof (pre-line working repo)

AI-powered humans（仮称 — layer 名は suspend 中、doctrine §12）のエンパワーメント戦略 doctrine v2。機構は **oracle debiasing**（[ADR-0002](docs/adr/0002-gatekeeper-inversion-strategic-reframe.md)）: 機械検証可能な存在証明を LLM が feasibility 質問を評価する面に置く。**research line ではない** — GitHub 公開済み（2026-06-05）だが DOI 未取得の working repo であり、「sibling」表記は使わない（sibling は research line レベル予約語 — authorship-strategy CLAUDE.md の terminology 規約）。昇格条件は [docs/doctrine.md §9](docs/doctrine.md)。

## Scope

- 固有領域: **エンパワーメント artifact payload**（存在証明フォーマット / question corpus / gatekeeping eval — doctrine §5 v2）。2×2 マップはチャネル座標系であり、payload は 4 セルを通過利用するが**どのセルのチャネル所有権も主張しない**（readme-writer / llms-txt-writer / jsonld-knowledge-graph / authorship-strategy の toolchain を再所有しない）。新規 channel infra の自前積み増しは禁止
- 主題は audience の empowerment。diffusion は副次効果（ADR-0007 との整合は doctrine §5 v2 が正本 — pivot は整合を強化する方向）

## 編集時の必須制約（正本ポインタ）

| 制約 | 正本 |
|---|---|
| 禁止事項（マネタイズ / 競合批判 / scope 過拡張 / enclosure） | `~/.claude/skills/authorship-strategy/SKILL.md` |
| Skip 確定 list（awesome-list PR / Wikidata / Pages LP / 非 Zenodo preprint / 被リンク獲得） | memory `authorship-strategy-judgments-shimo4228-2026-05` + doctrine §7 v2 bright line |
| cloaking 禁止・metric 規約（stars / views / eval score 目標を使わない） | memory `human-channel-seo-direction-2026-05` + authorship-strategy ADR-0007 + ADR-0005 |
| 本 repo 固有の禁止（勧誘 / membership / グリフター framing / 仮説の断定 / **format の movement 化 = registry・集約・join 言語・自称要求** / **promise narrative**） | doctrine §6 v2 |

doctrine を改訂したら、必ず doctrine §11 の自己検証チェックリスト **A-H** を実行する（H = registry / format-recruiting 検査、v2 追加）。

## Artifact map（v2）

| artifact | 場所 | ADR |
|---|---|---|
| 存在証明フォーマット（spec / template / instance #0） | [docs/format/](docs/format/spec.md) | [0003](docs/adr/0003-existence-proof-as-document-format.md) |
| 質問 corpus / FAQ / 証明構造 | [docs/corpus/](docs/corpus/README.md) | [0004](docs/adr/0004-machine-verifiable-proof-and-question-corpus.md) |
| playbook（format フィールド対応） | [docs/playbook/playbook.md](docs/playbook/playbook.md) | 0003 従属 |
| gatekeeping eval（probe / rubric / protocol） | [docs/eval/](docs/eval/README.md) | [0005](docs/adr/0005-gatekeeping-eval-as-published-probe-set.md) |
| machine 層（graph.jsonld / llms.txt / llms-full.txt） | repo root | 0004 |

## Writing conventions

- 言語: **ja のみ**（working language）。en 化は line 昇格時に `ja-to-en-translation` で実施。machine 面の en-ready 構造（graph `@language` tag / corpus・eval の ja+en 対）は先行可（[ADR-0001](docs/adr/0001-japanese-first-scale-strategy.md) Follow-ups — 直交 axis）
- 仮説規律: 層の実在は Phase 0 で観測支持済み。**規模・分布 + pivot 3 仮説（feasibility-question / gatekeeper-inversion / format-suggestion 拡散）は検証まで仮説表記**（doctrine §2 v2）。empirical 記録は "observation consistent with X" tone
- 命名は二 track（doctrine §12）: layer 名 = suspend（再オープンしない）/ format 名 = **確定「存在証明フォーマット」**（2026-06-05 著者確定。初出フル名、以降 EPF 可。bare 略語を primary token にしない）
- claim→anchor 規律: corpus / FAQ / instance の実例 cite はすべて解決確認済み anchor を持つ。解決しない anchor の証明は削除（falsifiability の自己適用）
- earned / owned の区別を崩さない: note / Zenn / Substack 自己投稿は owned/rented。LLM format-suggestion 拡散は LLM-mediated channel（earned ではない）
- 公開済み essay（note 2026-06-05）は canonical corpus source（旧 spearhead からの降格は prospective — 命名 signal 役割は維持）
- line 昇格時に適用される規約: EN primary / harness-vendor-framework neutrality / ADR format — authorship-strategy CLAUDE.md を踏襲

## 関連 repo

- `~/MyAI_Lab/authorship-strategy/` — 補完戦略（同一インフラ・別 payload・別受益者 — doctrine §5 v2）。doctrine 書式のモデル
- hub repo `shimo4228/shimo4228` — **本 repo はまだ hub に登録しない**（line 昇格まで hub の編集 trigger に該当しない）
