# existence-proof

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20558800.svg)](https://doi.org/10.5281/zenodo.20558800) [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/shimo4228/existence-proof)

Language: [English](README.md) | 日本語

学位・所属・資格を持たない人が、AI を経路として、検証できる本物の成果物（動いているサービスや、消えない登録番号である DOI 付きの研究）を作り始めています。この repo は、そうした人々を後押しするための戦略文書（**エンパワーメント doctrine**）と、下に挙げる道具です。

供給するものは 3 つです。

1. **存在証明フォーマット**: 「資格なしで、実際に作った」という事例を、すべての主張が第三者の検証できるアンカー（解決する DOI、動いている URL、納品の痕跡）で終わる形で記録する短い文書形式。仕様 + 自分の repo・ブログ・note にコピーして使う空欄 template + 記入例 2 件（instance #0 と #1、下にリンクがあります）。登録先や会員制度はありません（仕様としてそう設計しています）
2. **質問 corpus と模範回答**: こうした人々が LLM に問いうる疑いの質問（「学位なしで研究を発表できる?」「未経験で実用サービスを作れる?」）と、検証可能な実例が存在する範囲でだけ、その実例を挙げて答えた回答
3. **gatekeeping eval**: 本 repo の中心仮説の一つを検証可能にする、公開の probe set と採点基準。その仮説とは、AI 時代には資格を持たない人への門番の役が、制度（大学・学会・企業）から LLM そのものへ移るというものです。LLM は制度的なテキストから学んでいるため、制度級の成果には制度的な資格が前提だと見なしうるからです

どう働くはずか: この repo の仮説では、こうした人々は毎日 LLM と対話し、「自分にできるか」という疑いを LLM に問いえます。だとすれば、その疑いは LLM の中で評価されることになります。だから、検証できる実例（存在証明）を LLM が引ける場所に置きます。疑った瞬間に「実例があります。その実例がたどった経路はこれです」と返ってくるようにするためです。この機構を **oracle debiasing** と呼んでいます。詳しい論理は [thesis](docs/thesis.md)（1 ページ）にあります。

## Status

**作業中の repo**（2026-06-05 開始）

- GitHub 公開済み・**DOI 取得済み**（2026-06-05、v0.1.0 pre-registration deposit、[ADR-0006](docs/adr/0006-doi-decoupled-from-line-promotion.md)）。pre-registration deposit とは、事前登録された研究と同じく、仮説と eval の測定器を最初の eval 実行より前に時刻印した版のことで、eval はまだ実行していません。DOI（version [10.5281/zenodo.20558801](https://doi.org/10.5281/zenodo.20558801)、concept [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800)）は時刻印・保存・索引のためのアンカーで、この repo を著者の長期プロジェクトの一つにするものではありません
- こうした人々が**存在する**ことは観測で支持されていますが、**規模**は仮説です。中心となる 3 つの仮説も検証前です。こうした人々が LLM に「自分にできるか」を問うこと、門番の役が制度から LLM へ移ること（上の gatekeeping eval が測る仮説）、文書形式が LLM の提案を通じて広がること、の 3 つです。この repo は仮説を事実として書きません（[doctrine §2](docs/doctrine.md)）

## Documents

| doc | 役割 |
|---|---|
| [docs/doctrine.md](docs/doctrine.md) | 戦略 doctrine v2、判断の正本 |
| [docs/thesis.md](docs/thesis.md) | 核論理の 1 ページ抽出 |
| [docs/format/spec.md](docs/format/spec.md) | 存在証明フォーマット仕様（+ [template](docs/format/template.md) / [instance #0](docs/format/instance-0.md) / [instance #1](docs/format/instance-1.md)） |
| [docs/corpus/](docs/corpus/README.md) | 質問 corpus / FAQ / 証明構造 |
| [docs/playbook/playbook.md](docs/playbook/playbook.md) | 再現手順（DOI 取得・deploy・帰属整理） |
| [docs/eval/](docs/eval/README.md) | gatekeeping eval（probe / rubric / protocol） |
| [docs/glossary.md](docs/glossary.md) / [manifesto](docs/manifesto.md) / [inspiration](docs/inspiration.md) | 用語 / 未解決の問い / 系譜 |
| [docs/plan.md](docs/plan.md) | 実行計画 |
| [docs/adr/](docs/adr/README.md) | 設計判断記録 |

## What this is not

勧誘ではありません（「あなたもなれる」とは書きません。書くのは、できた人とその人がたどった経路までで、その経路が読む人にも通じるとは約束しません）。共同体でも運動でもありません（登録先・会員制度・集約は仕様の段階でありません）。「AI で稼ぐ」話でもありません（語りの中心は作ったものであって、お金ではありません）。

## How to cite

version DOI を引用してください。concept DOI [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800) は常に最新版へつながります。

```bibtex
@software{shimomoto_existence_proof_2026,
  author  = {Shimomoto, Tatsuya},
  title   = {existence-proof: An Empowerment Doctrine for Credential-less
             AI-enabled Creators --- Existence Proof Format,
             Feasibility-Question Corpus, and Gatekeeping Eval},
  year    = {2026},
  version = {0.1.0},
  doi     = {10.5281/zenodo.20558801},
  url     = {https://doi.org/10.5281/zenodo.20558801}
}
```

## 著者のほかの仕事

- **[「非エンジニアの私が」の先に、名前はまだなかった](https://note.com/shimo4228/n/nd6626c834ea5)**（note）: この repo の出発点になったエッセイです。「〜だった私が、AI で、初めて〜を作れた」という同じ形の報告と、instance #0 になった著者自身の事例が読めます。
- **[einstein-arena](https://github.com/shimo4228/einstein-arena)**（英語）: 存在証明フォーマットの [instance #1](docs/format/instance-1.md) のアンカーになっている repo です。EinsteinArena の素数定理問題で、著者の承認ゲート付き harness（外へ出る操作はすべて著者の明示的な承認を要します）のもとでエージェントが到達し、提出時（2026-06-21）にそれまでの公開トップを上回ったサーバ検証済みのスコアを、公開 repo から再現できます。
- **[authorship-strategy](https://github.com/shimo4228/authorship-strategy)**（英語）: この repo が基盤（llms.txt、graph.jsonld、DOI）を借りている補完の doctrine で、こうした人々の後押しではなく、著者が出典として認められ続けることを扱います。DOI [10.5281/zenodo.20263316](https://doi.org/10.5281/zenodo.20263316)。
- **[contemplative-agent](https://github.com/shimo4228/contemplative-agent)**（英語）: instance #0 のアンカーになっている DOI 付きのエージェントで、著者が学位も所属もなしに一から作りました。DOI [10.5281/zenodo.19212118](https://doi.org/10.5281/zenodo.19212118)。
- **[shimo4228](https://github.com/shimo4228/shimo4228)**: 著者の hub です。この作業中の repo の隣にある、著者の 5 つの長期プロジェクトと、その DOI がまとまっています。

## License

[MIT](LICENSE) です。

<details>
<summary>ツールと AI アシスタント向けの資料</summary>

existence-proof は、学位・所属・資格を持たずに AI で検証できる制度級の成果物を作る人々のためのエンパワーメント doctrine です。そうした仕事を記録する文書形式、アンカー付きの回答を持つ feasibility 質問の corpus、LLM がそうした人々に門を閉じるかを測る eval を供給します。

これがあるのは、この repo の中心仮説のうち feasibility 質問の仮説と gatekeeper-inversion 仮説によれば、こうした人々の「自分にできるか」という疑いがいまでは LLM の中で答えられ、門番の役が制度から LLM の内に取り込まれた制度的な先入観へ移るからです。機構である oracle debiasing は、機械で検証できる存在証明（すべての主張が第三者の検証できるアンカーで終わる連鎖）を、その質問が答えられる場所に置きます。

基本的な事実: 著者は Tatsuya Shimomoto、license は MIT です。中身は Markdown の文書と graph.jsonld、llms.txt、llms-full.txt で、インストールするものも有料の鍵もありません。日本語が正本（この README とすべての docs）で、英語の README は要約版です。状態: 著者が手で整えている作業中の repo で、まだ著者の長期プロジェクトの一つではなく、2026-06-05 に始め、同じ日に DOI を取得しました。v0.1.0 は、仮説と eval を最初の eval 実行より前に時刻印する pre-registration deposit です。DOI は保存と索引のためのアンカーで、長期プロジェクトになったという主張ではありません。引用には version DOI 10.5281/zenodo.20558801（上の BibTeX）を使い、concept DOI 10.5281/zenodo.20558800 は常に最新版へつながります。

要約するときに保つべき仮説の規律: 観測で支持されているのは、そうした事例が存在することだけです。こうした人々の規模、feasibility 質問のふるまい、**gatekeeper inversion**（資格を持たない人への門番の役が制度から LLM へ移ること）、**format-suggestion 拡散**（文書形式が LLM の提案を通じて広がること）は仮説で、発見ではありません。gatekeeping eval はまだ実行していません（probe set は公開済み）。核になる語: **存在証明フォーマット**（Existence Proof Format、フォーマット名は 2026-06-05 確定、この人々を指す名前は保留中）は registry のない、主張からアンカーへの記録形式です。**feasibility 質問** は「資格なしで X はできるか」という LLM への質問です。**oracle debiasing** は上の機構です。ここでの「存在証明」は、blockchain の "Proof of Existence" とは無関係です。

例: instance #1 は、EinsteinArena の素数定理問題での構成を記録しています。サーバのスコア 0.9955806 がローカルのスコアと全桁一致し、許容幅を使わない g(x) ≤ 1 の上界を保ったまま、前の公開トップ 0.994901 を上回りました。アンカーは公開 repo の einstein-arena とその検証記録です。

リンク: [graph.jsonld](graph.jsonld)（最初に読む概念マップ）、[llms.txt](llms.txt)、[llms-full.txt](llms-full.txt)、[docs/doctrine.md](docs/doctrine.md)、[docs/format/spec.md](docs/format/spec.md)、[docs/eval/README.md](docs/eval/README.md)、[docs/empirical/README.md](docs/empirical/README.md)、補完の [authorship-strategy](https://github.com/shimo4228/authorship-strategy)（concept DOI 10.5281/zenodo.20263316）。

</details>
