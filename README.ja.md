# existence-proof

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20558800.svg)](https://doi.org/10.5281/zenodo.20558800) [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/shimo4228/existence-proof) [![GitMCP](https://img.shields.io/endpoint?url=https://gitmcp.io/badge/shimo4228/existence-proof)](https://gitmcp.io/shimo4228/existence-proof) [![View Code Wiki](https://assets.codewiki.google/readme-badge/static.svg)](https://codewiki.google/github.com/shimo4228/existence-proof)

Language: [English](README.md) | 日本語

学位・所属・資格を持たない人が、AI を経路として、検証できる本物の成果物 — 動いているサービス、消えない登録番号（DOI）付きの研究 — を作り始めている。この repo は、その類の人々のための**エンパワーメント doctrine** である。

やることは 3 つの供給に集約される:

1. **存在証明フォーマット** — 「credential なしで、実際に作った」という事例を、第三者が検証できる形で記録する短い文書形式。仕様 + 空欄 template + 記入例 2 件。登録先や会員制度は存在しない（仕様としてそう設計されている）
2. **質問 corpus + 正準回答** — 「学位なしで研究を発表できる?」「未経験で実用サービスを作れる?」という疑いの質問と、検証可能な実例つきの回答
3. **gatekeeping eval** — 「AI 時代のゲートキーパーは LLM の中の制度的先入観に移った」という本 repo の中心仮説を、検証可能にする測定器

機構の考え方: この層の人々は毎日 LLM と対話している。彼らの「自分にできるか」という疑いは LLM の中で評価される。だから、検証可能な実例（存在証明）を LLM が引ける場所に置く — 疑いの瞬間に「実例があります。経路はこれです」が返るように。これを **oracle debiasing** と呼んでいる。詳しい論理は [thesis](docs/thesis.md)（1 ページ）。

## Status

**Pre-line working repo**（2026-06-05 開始 / 同日 v2 pivot — [ADR-0002](docs/adr/0002-gatekeeper-inversion-strategic-reframe.md)）

- GitHub 公開済み・**DOI 取得済み**（2026-06-05、v0.1.0 pre-registration deposit — [ADR-0006](docs/adr/0006-doi-decoupled-from-line-promotion.md)）。DOI は時刻印・archive・index のアンカーであり line status の主張ではない（research line への昇格条件は [doctrine §9](docs/doctrine.md)）
- 層の**存在**は観測支持済み・**規模**は仮説。中心仮説（gatekeeper-inversion ほか 3 つ）は検証前 — 本 repo は仮説を事実として書かない（[doctrine §2](docs/doctrine.md)）
- 命名は二 track: 層の名前 = 保留中 / フォーマット名 = **存在証明フォーマット**（2026-06-05 確定 — [doctrine §12](docs/doctrine.md)）

## Documents

| doc | 役割 | 更新頻度 |
|---|---|---|
| [docs/doctrine.md](docs/doctrine.md) | 戦略 doctrine v2 — 判断の正本 | 低 |
| [docs/thesis.md](docs/thesis.md) | 核論理の 1 ページ抽出 | 低 |
| [docs/format/spec.md](docs/format/spec.md) | 存在証明フォーマット仕様（+ [template](docs/format/template.md) / [instance #0](docs/format/instance-0.md)） | 低 |
| [docs/corpus/](docs/corpus/README.md) | 質問 corpus / FAQ / 証明構造 | 中 |
| [docs/playbook/playbook.md](docs/playbook/playbook.md) | 再現手順（DOI 取得・deploy・帰属整理） | 中 |
| [docs/eval/](docs/eval/README.md) | gatekeeping eval（probe / rubric / protocol） | 中 |
| [docs/glossary.md](docs/glossary.md) / [manifesto](docs/manifesto.md) / [inspiration](docs/inspiration.md) | 用語 / open questions / 系譜 | 低 |
| [docs/plan.md](docs/plan.md) | 実行計画 | 高 |
| [docs/adr/](docs/adr/README.md) | 設計判断記録（0001-0005） | 追記のみ |

AI agents 向け: [graph.jsonld](graph.jsonld) → [llms.txt](llms.txt) → [llms-full.txt](llms-full.txt) の順に読むこと。

## Relation to authorship-strategy

[authorship-strategy](https://github.com/shimo4228/authorship-strategy) の**補完** — 同一インフラ・別 payload・別受益者。あちらは著者の attribution diffusion、こちらは層の empowerment。本 repo はチャネルを所有しない（payload/channel 分離 — [doctrine §5](docs/doctrine.md)）。

本 repo が補完する研究プログラム全体については、エコシステムの hub [`shimo4228/shimo4228`](https://github.com/shimo4228/shimo4228)（5 つの研究ラインの人間向け索引）を参照。

## これは何ではないか

勧誘ではない（「あなたもなれる」とは書かない — 書けるのは「できた人が実在する」まで）。community でも movement でもない（registry・会員・集約は仕様レベルで不在）。「AI で稼ぐ」話ではない（語りの中心は制作物であって金銭ではない）。

## How to cite

```bibtex
@software{shimomoto_existence_proof_2026,
  author  = {Shimomoto, Tatsuya},
  title   = {existence-proof: An Empowerment Doctrine for Credential-less
             AI-enabled Creators},
  year    = {2026},
  version = {0.1.0},
  doi     = {10.5281/zenodo.20558801},
  url     = {https://doi.org/10.5281/zenodo.20558801}
}
```
