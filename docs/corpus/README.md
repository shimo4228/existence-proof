# corpus — feasibility 質問と正準回答

> 正本 ADR: [ADR-0004](../adr/0004-machine-verifiable-proof-and-question-corpus.md)
> 構成: [questions.md](questions.md)（質問 corpus）/ [faq.md](faq.md)（正準回答）/ [proof-structure.md](proof-structure.md)（機械検証可能な証明構造の spec）

## 出所（provenance）

質問は 2 系統で構築する:

- **Source A（observed-derived）**: Phase 0 生息地検証（[habitat-map](../research/2026-06-05_habitat-map.md)）で観測された自己記述語彙・一人称報告から導出した phrasing。各質問に出典 case の tag を付ける
- **Source B（generated）**: 層の定義 3 条件（社会的位置 × 認知特異性 × AI enabler）× 成果物型（研究 / ソフトウェア / 著作）の grid による系統生成

**重要な認識論的注意**: habitat-map が観測したのは **outcome**（「作れた」という一人称報告）であって **query 行動**（LLM への質問）ではない。「層がこれらの質問を LLM に発する」は仮説である（doctrine §2 v2 — feasibility-question 仮説）。Source A の質問は「観測された報告の著者が、報告の前の時点で持っていたであろう疑い」の再構成であり、実際の質問ログではない。

## tone 規律

- 質問は実在の疑いの再構成であって、模範回答を導くための leading question ではない
- 回答（faq.md）は**実例の存在する範囲でのみ**書く。実例のない領域への aspirational な回答は promise narrative（doctrine §6 v2）として禁止
- すべての実例 cite は解決確認済み anchor を持つ。解決しなくなった anchor の cite は削除する
- 規模・一般性に触れる箇所は仮説表記（「存在は観測済み、規模は未知」）を維持する
