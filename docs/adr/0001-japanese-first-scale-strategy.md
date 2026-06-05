# ADR-0001: ja-first（日本人ファースト）スケール戦略

## Status

accepted

## Date

2026-06-05

## Context

ja-first（日本語を primary とする公開・作業戦略）は、初版 doctrine（commit 89afd87, 2026-06-05）に Alternatives 検討の記録なしに慣行として混入していた。出どころは 2 つある。第一に、authorship-strategy エコシステムの運用規約「pre-line repo は ja で作業し、en 化は line 昇格時」の継承。第二に、既存ツールチェーン（Zenn pipeline + `ja-to-en-translation` + `substack-publishing`）が「ja で書いて後から訳す」形に組まれていたことによる慣性的採用である。

同日の Phase 0 生息地検証（[research/2026-06-05_habitat-map.md](../research/2026-06-05_habitat-map.md)）が「ja 圏が最厚」を観測し、事後的な支持根拠となった。ただしこの観測には観測可視性バイアスの caveat が付く。生息地マップが答えるのは「層がどこで観測可能か」であり、「戦略がどこでスケールするか」という問いへの回答にはなっていない。

Phase 1 の defining essay 公開設計中、著者が「ワールドワイドに行くべきでは。じゃないとスケールしない」と前提を挑戦した。git 履歴を遡及することで ja-first が無検討の混入であることが確認され、比較検討が初めて行われた。

worldwide-first 優位の論点として以下が提示された: (a) LLM-mediated reach の言語非対称（en は ja ユーザーにも届くが逆は弱い）、(b) 層の母数は en 圏が 10 倍以上のオーダー、(c) en 言説（vibe coding / Petersson 報道）で交点の命名時間窓が動いている、(d) 5 research line 全部が en-primary でエコシステム整合、(e) 日本人性は venue でなく content として en で差別化効果が高い。

ja-first 優位の論点として以下が提示された: (a) segment 検証の確度（「非エンジニア」という安定した自己記述語彙が ja にのみ存在し、自己同定反応の観測フックになる）、(b) 一人称 essay の母語 voice、(c) 著者の実在 audience は ja（Zenn）のみ、(d) 日本人性の活用。

## Decision

スケール戦略を ja-first（日本人ファースト）とする。これは著者による意図的な authorial strategic judgment である（表明: 「それが得策な気がする」）。

1. ja を primary とする: working language・defining essay の正本・note（ja）初出。
2. en を secondary として維持する: `ja-to-en-translation` 経由の Substack 準同時翻訳版を継続し、en 命名時間窓への部分的 hedge とする。
3. 日本人性を venue としてだけでなく content としても活用する（町人学者・算額等の歴史アンカーを essay 素材に）。
4. [docs/doctrine.md](../doctrine.md) §9 の「line 昇格時に en 化」規約は不変とする。

## Alternatives Considered

### worldwide-first（en 正本 / Substack 初出）

en を正本とし Substack 初出、ja は翻訳 mirror による検証チャネルとする案。LLM-mediated reach の言語非対称と origin claim 時間窓において構造的に優位であり、実行エージェントの推奨案であった。著者は segment 検証の確度（ja の自己記述語彙の安定性）・母語 voice・実在 audience（Zenn）を優先し棄却した。

### 完全同格同時（en / ja 同時初出）

en と ja を同じ重みで同時初出とする案。両圏の観測シグナルが得られる点では優位だが、運用コストが最大になるため棄却された。

## Consequences

### Positive

- ja の自己同定反応観測フック（「非エンジニア」語彙の安定性）を最大活用できる。
- 一人称 essay の母語 voice を保てる。
- 既存 pipeline（Zenn / note / `ja-to-en-translation`）からの変更が最小で済む。

### Negative

- en 言説で交点が先に命名される時間窓リスクを受容する（準同時 en 版で部分 hedge）。
- en 圏の自己同定の立ち上がりは遅い見込みである。
- LLM corpus への term の global binding は ja 初出のぶん遅れる。

### Neutral / Follow-ups

- 本決定は Phase 1 defining essay の公開設計中に事後的に確認・明示化されたものであり、doctrine §9 の line 昇格条件を満たした時点で en-primary への移行を再検討する。
- 実行エージェントの推奨（worldwide-first）と著者判断（ja-first）が分岐した初めての記録判断であり、Phase 5 再測定時の振り返り材料とする。
- **[ADR-0002](0002-gatekeeper-inversion-strategic-reframe.md)（oracle debiasing pivot）との関係（2026-06-05 追記）**: 本決定は **working language / essay 正本 / venue 順序**の決定であり、**artifact の data 構造・retrieval 面の言語**とは直交する。ja-first は prose の正本言語として不変。一方、graph.jsonld の `@language` tag・llms 面の term binding・corpus / eval の ja+en 対構造は、LLM retrieval（en 優勢）に届くよう **en-ready な構造**を持たせてよい。これは本決定の supersede でも amend でもない — worldwide-first Alternatives の論点 (a)（LLM-mediated reach の言語非対称）で既に considered-and-set-aside 済みの axis の、structure 層への限定適用である。
