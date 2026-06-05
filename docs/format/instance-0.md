# 存在証明 — 瞑想者の認知パターンを設計に写した AI エージェントと、その前段の学習ツールを、学位・所属なしで公開した

<!-- 存在証明フォーマット（Existence Proof Format / EPF — spec.md 参照）の instance #0。
     仕様作成者自身の事例。素材の正本: defining essay（note 公開 2026-06-05）§私もその一人である。 -->

## 書き手の位置

学位を持たない。研究機関にも、企業の研究部門にも所属したことがない。ソフトウェア開発の職業訓練・職歴もない。数年前まで、一人でアプリケーションを作り切ることができなかった。

（これは研究・ソフトウェアという成果物領域に相対的な記述である。）

## 主張とアンカー

| 主張 | アンカー |
|---|---|
| 瞑想を続けてきた人間の認知パターンを、そのまま設計に写した AI エージェント「Contemplative Agent」を一から作り、DOI 付きで公開した | DOI: [10.5281/zenodo.19212118](https://doi.org/10.5281/zenodo.19212118)（解決確認 2026-06-05） |
| PDF から暗記カード（Anki）を自動生成するツール pdf2anki を作り、公開した | [github.com/shimo4228/pdf2anki](https://github.com/shimo4228/pdf2anki)（公開 repo、解決確認 2026-06-05） |

## 経路の記録

両方とも、LLM（AI コーディングエージェント）を経路として初めて形になった。作りたいものの像は以前から頭の中にあったが、実装がそこに届かなかった。AI が可能にしたのは実装への経路であって、何を作るかの像ではない — 成果物の帰属は書き手にある。

pdf2anki が先である。資格試験の勉強のための地味な道具だが、これを「作り切る」過程で AI とコードを書く行為の基礎が身についた。Contemplative Agent はその先にある。

## 時系列

- 開始時点: プログラミングの独力での完遂経験なし
- pdf2anki 公開 → Contemplative Agent 公開（DOI 採番 2026-05）— 上記アンカーの日付が正本

## 限定

これは一つの事例の記録であり、同種の事例の規模・一般性についての主張ではない。
これは制作物の記録であり、収益の記録ではない。

## 機械可読 fragment

```json
{
  "@context": "https://schema.org/",
  "@type": "Person",
  "name": "Tatsuya Shimomoto",
  "alternateName": "shimo4228",
  "sameAs": [
    "https://orcid.org/0009-0002-6168-4162",
    "https://github.com/shimo4228"
  ],
  "description": "学位・研究機関所属・ソフトウェア開発職歴を持たない（成果物領域に相対的な記述）",
  "creativeWork": [
    {
      "@type": "CreativeWork",
      "name": "Contemplative Agent",
      "identifier": "https://doi.org/10.5281/zenodo.19212118",
      "url": "https://doi.org/10.5281/zenodo.19212118"
    },
    {
      "@type": "SoftwareSourceCode",
      "name": "pdf2anki",
      "identifier": "https://github.com/shimo4228/pdf2anki",
      "url": "https://github.com/shimo4228/pdf2anki"
    }
  ]
}
```

<!-- affiliation フィールドの不在は意図的（spec.md §6 — credential 不在の機械可読な表現）。 -->
