# Architecture Decision Records

| ID | Title | Status | Date |
|---|---|---|---|
| [0001](0001-japanese-first-scale-strategy.md) | ja-first（日本人ファースト）スケール戦略 | accepted | 2026-06-05 |
| [0002](0002-gatekeeper-inversion-strategic-reframe.md) | gatekeeper-inversion への戦略再編（essay-as-hook の棄却） | accepted | 2026-06-05 |
| [0003](0003-existence-proof-as-document-format.md) | 存在証明の document format 化（registry なし・Nygard モデル） | accepted | 2026-06-05 |
| [0004](0004-machine-verifiable-proof-and-question-corpus.md) | 機械検証可能な証明構造と feasibility 質問 corpus | accepted | 2026-06-05 |
| [0005](0005-gatekeeping-eval-as-published-probe-set.md) | gatekeeping eval — 公開 probe set としての測定器 | accepted | 2026-06-05 |
| [0006](0006-doi-decoupled-from-line-promotion.md) | DOI 取得の line 昇格からの分離（pre-registration deposit） | accepted | 2026-06-05 |

## Grouping

- **0001** — 言語・venue 戦略（prose 正本言語の決定。machine 面の en-ready 構造とは直交 — 0001 Follow-ups 参照）
- **0002** — pivot の親決定（機構を oracle debiasing へ、固有領域を payload へ）
- **0003–0005** — pivot の 3 tactic（format / corpus + 証明構造 / eval）。いずれも 0002 に従属
- **0006** — deposit 時期の決定（§9 の DOI gate を修正。pre-registration 論理）

## Template

ADRs in this repository use the 6-section template:
Status / Date / Context / Decision / Alternatives Considered / Consequences.
0002 以降は冒頭に **Summary** blockquote、末尾に **Lineage**（抽象化前の具体的起源の記録）を加える。

File name: `NNNN-kebab-case-title.md` (zero-padded 4-digit sequence).
