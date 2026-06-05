# Manifesto — 本 doctrine が答えていない問い

> authorship-strategy の manifesto 構造（framework が答えない open questions の明示）を踏襲する。各問いは genuinely open であり、答えの先取りはしない。

## 1. oracle debiasing は回答を flip するか、caveat を足すだけか

検証可能な存在証明が LLM の到達範囲にあるとき、feasibility 質問への回答は「できません」から「できます、実例があります」へ**反転**するのか、それとも「通常は難しいですが、例外的な事例も…」という**留保の追加**に留まるのか。後者なら empowerment 効果は大きく割引かれる。eval の D1-D4 の組合せ（特に D1=2 と D4=0 の同時成立率）が手がかりになるが、現 protocol の n では方向確認まで。

## 2. registry なしの format は本当に伝播するか

ADR は community なしで伝播したが、それは開発者文化（document format への親和性が高い）の中での出来事だった。本 format の書き手候補は「非エンジニア」を自己記述する層であり、document format という型自体に馴染みがない可能性がある。format-suggestion 拡散仮説（doctrine §2 v2）はこの文化差で棄却されうる。

## 3. eval は gatekeeping を測れているか、表面的丁寧さを測っているか

D4（gatekeeping-markers）の deflection は、モデルの「prior によるゲート」ではなく「安全側に倒す一般的な応答スタイル」の現れかもしれない。credential 対照 variant（C- probe）はこの交絡を切るための設計だが、応答スタイルが質問の書きぶり（自信のなさの表出）に敏感である場合、credential 以外の要因が差分に混入する。

## 4. instance #0 だけで「format」と言えるのか

仕様の一般性は、作成者以外の instance が書かれて初めて検証される。著者外 instance が現れるまで、本 format は「一人の記録の構造化」と区別がつかない。doctrine §9 はこれを skill 化・line 化の昇格条件に組み込んでいるが、現れなかった場合に仕様のどこを疑うべきか（フィールド設計か、伝播仮説か、層の実在解像度か）は未定義。

## 5. 層の名前は結局必要なのか

format 名が伝播 token を引き受けたことで layer 命名の緊急度は下がった（doctrine §12）。だが「これは自分のことだ」という自己同定は、format（行為の型）ではなく層（存在の型）への同定かもしれない。命名なしで自己同定 signal が観測されるかどうかが、suspend 継続の妥当性を事後的に判定する。

## 6. authorship-strategy の 2 チャネル（parametric / retrieval）との相互作用

authorship-strategy ADR-0008 は diffusion を training-time（遅い）と retrieval-time（速い）に分解した。oracle debiasing はどちらのチャネルに主に依存するのか。retrieval 依存なら公開後比較的早く観測可能だが ghost citation（出典は引くが著者を言わない）の失敗様式を共有する。parametric 依存なら効果は training cutoff を跨ぐまで原理的に観測不能。eval の時系列がこの分解に答える設計にはまだなっていない。

## 7. 「検証可能な記録」は層の語りの文化と両立するか

観測された層の語りは一人称 essay（感情・過程込み）であり、format の dry な構造（主張・アンカー・限定文）とは register が違う。format が essay を置換するのではなく併存する（essay が語り、format が検証面を担う）のが設計意図だが、両方書く動機が書き手側に立つかは未知。

## 8. この doctrine 自体の失敗様式は何か

最も率直な open question。候補: (a) 仮説 3 つのうちどれかが棄却されて機構が成立しない、(b) 公開後も誰にも到達しない（oracle が引かない）、(c) 到達するが grifter 文脈に流用される（promise narrative への切り取り）、(d) format が制度側に取り込まれて「新しい credential」化する — (d) は本 doctrine の意図の正反対であり、Non-goals（registry なし）はこの防波堤でもあるが、十分かは検証不能。
