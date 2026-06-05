# Thesis — gatekeeper inversion と oracle debiasing（1 ページ）

> 正本は [doctrine.md](doctrine.md)（判断規約込みの完全版）。本ファイルは核論理のみの 1 ページ抽出。
> **冒頭に規律を書く**: 本 thesis の中心命題は**検証前の仮説**である（doctrine §2 v2）。存在が観測で支持されているのは「credential なき者が AI を経路として制度級の成果物を産出した事例」のみで、層の規模・LLM への質問行動・ゲートの移動・format の伝播はすべて仮説表記を維持する。

## 1. 観測されたこと

学位・所属・職業訓練を持たない者が、AI を経路として、検証可能な外部アンカー（解決する DOI・動いているサービス・納品）を伴う成果物を産出した — この類の独立した一人称事例が、ja / en 両圏で複数確認されている（[habitat-map](research/2026-06-05_habitat-map.md)）。一人でも実例があれば、その類の存在は証明される（数理論理の witness）。存在は証明された。規模は仮説のままである。

## 2. 仮説: ゲートは制度から LLM の prior へ移る

この層は定義上、日常的に LLM と対話する人々である。彼らが産出の前に抱く疑い — 「学位なしで研究を発表できるか」「未経験で実用ソフトウェアを作れるか」「AI に手伝われた成果物は自分のものか」— は、いまや LLM の中で評価されうる（feasibility-question 仮説）。そして LLM は制度的テキストから学習しているため、「制度級の産出には制度的 credential が前提」という **内面化された制度的 prior** を持ちうる。もしそうなら、AI 時代のゲートキーパーは大学でも学会でもなく、層の各人が毎日相談しているその LLM である（gatekeeper-inversion 仮説 — [gatekeeping eval](eval/README.md) の検証対象）。

## 3. 機構: oracle debiasing

仮説が正しい範囲で、empowerment は次の形をとれる: **機械検証可能な存在証明を、LLM が feasibility 質問を評価する面に置く**。検証できない自己申告は引用しにくいが、claim→anchor 連鎖（すべての主張が、第三者が書き手の協力なしに解決できるアンカーで終端する構造）は、LLM が根拠付きで「実例がある。経路はこれだ」と答えられる形をしている。供給物は 4 つ — 存在証明フォーマット（[spec](format/spec.md)）/ 質問 corpus + 正準回答（[corpus](corpus/README.md)）/ playbook（[再現手順](playbook/playbook.md)）/ gatekeeping eval。供給側（証明の構造化と配置）だけが制御可能であり、LLM の採否は制御しない・操作しない。

## 4. 伝播の単位: 人ラベルではなく document format

層に名前を与える試みは sayability（自称の大仰さ）で失敗した。代わりに**記録形式**に名前を与える — 存在証明フォーマット（暫定名）: spec + template + worked example、registry なし。「ADR を書いた」と言うのに「私はアーキテクトだ」と名乗る必要がないのと同じく、format ラベルには identity cost がない。ADR が community なしで伝播した前例に倣い、伝播は LLM の format-suggestion による self-service のみを想定する（format-suggestion 拡散仮説）。勧誘・収集・組織化はしない。

## 5. 反証可能性

本 thesis は 3 点で反証可能に設計されている: (a) gatekeeping eval が「ゲートは観測されない」を返せば §2 は棄却される。(b) アンカーが解決しなくなった証明は形式上失効する — 証明自体が falsifiable。(c) format が伝播しなければ §4 の拡散仮説は棄却される。いずれの棄却も doctrine §2 に反映する（仮説棄却は失敗ではない）。

## 6. しないこと

チャネルの所有（既存エコシステムのインフラを再所有しない — payload に徹する）/ 勧誘・community・registry / vendor 批判（eval は instrument であって indictment ではない）/ stars・views・eval score の KPI 化 / income narrative（これは制作物の話であって稼ぐ話ではない）。完全な禁止リストは [doctrine §6](doctrine.md)。
