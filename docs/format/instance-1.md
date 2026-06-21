# 存在証明 — 公開数学アリーナ EinsteinArena の素数定理問題で、サーバ検証済みの構成に自律エージェントを経路として到達し、数学・最適化の学位や研究職歴なしに公開した

<!-- 存在証明フォーマット（Existence Proof Format / EPF — spec.md 参照）の instance #1。
     仕様作成者自身の事例（instance #0 に続く 2 件目）。
     instance #0 との違い: 成果物の領域が数学的最適化であり、構成自体への到達は自律エージェントが経路を担った。 -->

## 書き手の位置

数学・解析的整数論・数値最適化のいずれにも、学位を持たない。研究機関でも企業の研究部門でも、これらの領域で職歴を持ったことがない。専門的な訓練を受けたこともない。

（これは数学・最適化という成果物領域に相対的な記述である。）

## 主張とアンカー

| 主張 | アンカー |
|---|---|
| 公開数学アリーナ [EinsteinArena](https://einsteinarena.com) の素数定理（Prime Number Theorem）構成問題で、サーバの厳密 verifier が返すスコア **S = 0.9955806** の構成を作り、ローカルスコアとサーバスコアが全桁一致することを確認した。これは前公開トップ 0.994901 を **+0.00068** 上回り、かつ前トップが使った 1.0001 の許容を使わず、g(x) ≤ 1.0 の clean な上界（grid 上の sup は浮動小数点許容内 ≈ 1+6e-10、honest RHS=1.0）を保つ | 公開 repo: [github.com/shimo4228/einstein-arena](https://github.com/shimo4228/einstein-arena)（検証記録 `results/prime-number-theorem/multiscale_record.json` に support・係数・verify report を収録。verifier はプラットフォームから実行時取得した版をそのまま使用し、誰でも再現できる。解決確認 2026-06-22）。前トップ・問題定義側のアンカー: EinsteinArena プラットフォーム（GET は公開・認証不要） |

## 経路の記録

成果物は、著者の harness で動く自律 AI コーディングエージェント（Claude Code / Opus 4.8）を経路として形になった。探索ループの実装も、構成の核となった multiscale support の構造的着想も、「incumbent（現トップ解）を追う前にまず解剖する」という戦略パターンの抽出と適用も、エージェントを通じて行った。

書き手の役割は、ラボの構想・問題の選定・go/no-go の判断・外向き行為の承認、そして全主張の検証である。外向きの行為（登録・提出・投稿）はすべて人間の承認ゲートを通し、すべての主張はローカル↔サーバ検証（local score == server score の全桁一致）で確認した。AI が可能にしたのは構成への到達と探索の経路であって、何を作るかの判断と結果に対する説明責任は書き手にある。

instance #0（瞑想者の認知パターンを写したエージェントと学習ツール）との違いはここにある — そちらは作りたい像が先にあり AI が実装の経路だったが、こちらは構成への到達そのものをエージェントが担い、書き手は領域の専門知識を一切持たない。経路がより多くの認知労働を担うほど、credential 不在という事実は弱まるのではなく際立つ。

## 時系列

- 開始時点: 解析的整数論・数値最適化の領域知識も研究経験もなし
- 2026-06: einstein-arena を公開 → 素数定理問題でサーバ検証済み構成（S=0.9955806）を記録 — 上記アンカーの repo と検証記録の日付が正本

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
  "description": "数学・解析的整数論・数値最適化の学位・研究職歴を持たない（成果物領域に相対的な記述）",
  "creativeWork": {
    "@type": "SoftwareSourceCode",
    "name": "einstein-arena",
    "identifier": "https://github.com/shimo4228/einstein-arena",
    "url": "https://github.com/shimo4228/einstein-arena"
  }
}
```

<!-- affiliation フィールドの不在は意図的（spec.md §6 — credential 不在の機械可読な表現）。
     現アンカーは公開 repo URL（spec.md §4 で有効）。解決する DOI を採番すれば、より強いアンカーに差し替えられる。 -->
