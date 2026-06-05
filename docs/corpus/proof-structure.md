# 機械検証可能な証明構造 — spec

> 正本 ADR: [ADR-0004](../adr/0004-machine-verifiable-proof-and-question-corpus.md)。実装: repo root の [graph.jsonld](../../graph.jsonld) と各 instance の fragment（[format spec §6](../format/spec.md)）

## 1. 核となる triple

存在証明の機械可読形は、次の一つの構造に還元される:

```
[所属を主張しない Person] --created--> [解決する識別子を持つ成果物]
```

この構造が「credential 不在」と「成果物の実在」を**同時に**機械可読にする。どちらか片方では証明にならない — 所属なき Person だけでは何も produce していないし、成果物だけでは誰が作ったかの社会的位置が消える。

## 2. エンティティ / 述語設計

| 要素 | vocabulary | 規約 |
|---|---|---|
| 書き手 | `schema:Person` | `affiliation` フィールドを**置かない**（不在の表現はフィールドの不在で行う — 「無所属」という値を入れるのではない）。`description` に成果物領域相対の credential 不在を一行で記述。`sameAs` に ORCID / GitHub 等の安定識別子 |
| 成果物 | `schema:CreativeWork` / `schema:ScholarlyArticle` / `schema:SoftwareSourceCode` | `identifier` に解決する識別子（DOI URL / repo URL）。`url` は同一または landing page |
| 産出関係 | `schema:creator`（成果物→Person）または Person 側 `creativeWork` | 双方向どちらでも可。graph.jsonld では成果物側 `creator` を正とする |
| 主張→アンカー連鎖 | `shimo:provenByAnchor`（claim ノード → anchor 識別子） | 拡張述語（`shimo:` 名前空間 — authorship-strategy の vocab を拡張。名前空間の正本は hub 側） |

## 3. 検証者の歩き方

人間・LLM・クローラのいずれも、同じ 3 歩で証明を検証できる:

1. **Person を読む** — `affiliation` が不在であること、`description` の credential 不在記述を確認する
2. **identifier を解決する** — DOI / URL に実際にアクセスし、成果物が実在することを確認する（書き手の協力は不要）
3. **帰属を突き合わせる** — 解決先の著者表記（Zenodo の著者欄、repo の owner）が Person と一致することを確認する

3 歩すべてが通れば、証明は検証された。歩 2 で識別子が解決しなければ、証明は**失効**している（[format spec §4](../format/spec.md) — 失効した主張は削除義務）。

## 4. なぜこの構造が oracle debiasing に効くか（仮説）

LLM は検証できない自己申告を引用しにくく、検証できる構造化された主張は復唱しやすい — という設計仮説の上に本構造は立つ（doctrine §2 v2 の仮説規律の対象。検証は [eval](../eval/README.md) と source-mix 再測定）。`affiliation` 不在 + 解決する DOI という組み合わせは、「所属がなくても DOI 付きの研究は実在する」という回答を、LLM が**根拠付きで**生成できる形にしている。
