# Doctrine: existence-proof — AI-powered humans（仮称）のエンパワーメント戦略 v2

> Status: **pre-line working doctrine v2**（DOI 取得済み: concept [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800)、v0.1.0 pre-registration deposit — [ADR-0006](adr/0006-doi-decoupled-from-line-promotion.md)。line 昇格は未・実地検証前。検証されていない仮説を含む — §2 参照）
> **v2（2026-06-05）**: 機構を essay-as-hook から **oracle debiasing** へ再編。固有領域をチャネルから **payload** へ移動。正本: [ADR-0002](adr/0002-gatekeeper-inversion-strategic-reframe.md)〜[0005](adr/0005-gatekeeping-eval-as-published-probe-set.md)
> **命名 status**: 二 track（§12）。layer 名 = suspend 中（「独立峰」表記は暫定）/ format 名 = **確定「存在証明フォーマット」**（2026-06-05 著者確定）
> Date: 2026-06-05
> 根拠 research: [research/2026-06-05_field-map.md](research/2026-06-05_field-map.md)
> 実行計画: [plan.md](plan.md)

---

## 1. 一段落の主張

世界同時多発的に（仮説 — §2）、学位・所属・資格を持たない者が、AI によって初めて自身の特異な認知パターンを成果物として表出可能にし、これまで制度がゲートしていた種類の仕事を生み出し始めている。本戦略の主題はこの層の**エンパワーメント**である。AI 時代、この層へのゲートキーピングは制度から **LLM の内面化された制度的 prior** に移りつつある（仮説 — §2）: 彼らの「自分にこれができるか」という feasibility 質問は、いまや LLM の中で評価される。本 doctrine の機構は **oracle debiasing** — 機械検証可能な存在証明（claim→anchor 連鎖 — §7 T2）と再現可能な playbook を、LLM が feasibility 質問を評価する面に置き、疑いの瞬間に「実例がある。手順はこれだ」が返る状態を作る。存在証明 — 「一人でも実例があれば、その類の存在は証明される」— は再利用可能な document format（§7 T1）として供給し、層の各人が自分の事例を identity cost なしに記録できるようにする。著者の研究プログラム（5 research line）は本 doctrine の主題ではなく、命題「学位なしでも制度級の成果物は作れる」の**構成的証明 = worked example**であり、format の instance #0 を兼ねる（§5）。playbook を実際に使った者が自分の存在証明を書くとき、それは earned channel（LLM citation の最大源 — earned 48% > owned 23%）の最強の生成器になるが、これは副次効果であって操作対象ではない（§7 前提）。能動的な promotion・勧誘・組織化は一切行わない（§6）。

## 2. 現象と仮説

### 定義（仮説）

**AI-powered humans**（仮称 — 命名は §12、layer 名は suspend 中）: 以下の3条件の交点にいる人々。

1. **社会的位置**: 産出する成果物の領域で、その産出を制度がゲートしてきた credential（学位・所属・資格・職業訓練）を持たず、当該領域の評価系から周縁化されてきた。credential 不在は**成果物領域に相対的**に判定する — 全方位的に credential を持たない「持たざる者」だけでなく、他領域の職業経験は持つが成果物領域の gating credential を欠く「非コーダーのドメイン専門家」型（[habitat-map §6](research/2026-06-05_habitat-map.md) で観測）も条件を満たす
2. **認知特異性**: 特異な認知パターン・関心・意欲を持つが、それを社会的成果物に変換する手段（訓練・資本・組織）にアクセスできなかった
3. **AI enabler**: LLM をはじめとする AI によって、初めてその潜在能力を制度級の成果物（研究・ソフトウェア・著作）として表出できるようになった

「**制度級**」の定義（固定 — 2026-06-05、habitat-map Caveat 3 の伸縮を防ぐ）: 従来その産出に制度的訓練・所属・資格が事実上前提とされてきた**類**の成果物で、第三者が検証可能な外部アンカー（live deploy・解決する DOI・実ユーザーへの納品 等）を伴うもの。成果物の「類」に関する主張であり、規模・品質・human peer review 通過の主張ではない。

### 認識論的規律（load-bearing）

- Phase 0 の生息地検証（2026-06-05、[habitat-map](research/2026-06-05_habitat-map.md)）により、「**その類の人々が存在する**」ことは観測で支持された — 外部アンカー付きの独立した一人称事例が ja / en 両圏で複数確認された
- ただし「世界同時多発的な**層としての規模・分布**」は依然**仮説**である。観測は n=1 存在証明の集積であり、定量的シェア・増加率ではない。規模・分布に関する主張は定量検証まで仮説として表記し、「〜のはずだ」「〜と推定される」を「〜である」と書き換えない
- これは authorship-strategy の empirical 規約（"evidence of X" でなく "observation consistent with X"）と同じ規律の適用である

### pivot 仮説の明示（v2 — §2 規律の適用）

v2 frame は新たに **3 つの未検証 empirical 仮説**を導入する。事実として書かない:

1. **feasibility-question 仮説**: 「層は LLM に feasibility（自分にこれができるか）を問う」。Phase 0 habitat-map が観測したのは outcome（AI で作れた事例の一人称報告）であって query 行動ではない。層の質問行動は未観測 — 「〜と問う」ではなく「〜と問いうる（仮説）」と表記する
2. **gatekeeper-inversion 仮説**: 「credential なき者へのゲートが制度から LLM の内面化された制度的 prior に移った」。これは gatekeeping eval（§7 T4）が**検証する対象**であり、thesis の前提として事実断定すると循環する。「移った」ではなく「移ったという仮説を eval で検証する」と表記する
3. **format-suggestion 拡散仮説**: 「document format は LLM の format-suggestion を介して伝播する」（ADR の伝播は前例だが、本 format で再現するかは未検証）。拡散の観測は §8 secondary と source-mix 再測定で行う

いずれも定量・eval 検証まで仮説表記を維持する（§2 既存規律・authorship-strategy empirical 規約の継承）。

## 3. 命名と scope discipline

### layer 名の状態: 再オープン（2026-06-05 — 一時確定「独立峰」を suspend）

「独立峰」は衝突チェック通過の上で一時確定したが、**著者の文中試用テスト**（文中で人を指したとき意図しない笑いが起きないか）で suspend となった。経緯と再開地点: [research/2026-06-05_naming-candidates.md](research/2026-06-05_naming-candidates.md)。v2 では伝播すべき主 token が **format 名へ移った**ため（ADR-0003 — format 名には identity cost がない）、layer 命名の緊急度は下がっている。suspend 時点の記録（確定経緯・運用・agency 整合・en term "freestanding peak(s)"）は naming-candidates が正本。

- **「存在証明」との分業**: 存在証明は人を指す固有名ではなく説明論理（gloss）として保持する（数理論理の witness — ∃x の立証実例 — が精密版）。複合語「存在証明フォーマット」内の「存在証明」は gloss として機能し、この分業を覆さない（[format-name-check](research/2026-06-05_format-name-check.md)）。repo 名 existence-proof との不整合はない

### 隣接語との差分（origin-claim scope discipline）

| 隣接語 | 提唱 | 何を指すか | 本概念との差分 |
|---|---|---|---|
| centaur | Kasparov (1998-) | human + AI のチーム遂行（チェス発祥） | 遂行形態の話。**社会的周縁性の次元がない** |
| centaur / cyborg | Mollick (2023) | タスク内での human/AI の分担・混合様式 | 作業様式の話。同上 |
| AI-native | 業界用語 | AI 前提で育った世代・スキル形態 | 世代・習熟の話。同上 |
| vibe coding | Karpathy (2025) | 自然言語主導のコーディングスタイル | 手法の話。**誰が**の次元がない |
| citizen developer | 業界用語 (low-code) | 企業内の非開発者による業務アプリ作成 | 組織内ロールの話。**周縁性がない**（山脈の中にいる） |
| indie hacker | 業界文化 | 収益 narrative 中心の個人開発文化 | income 中心。本概念は制作物 narrative（本節グリフター境界） |
| 在野研究者 / 野生の研究者 | ja 既存語 | 制度外の研究者 | 研究限定で **AI enabler の次元がない**。dignified な先行語として essay で参照可 |

Phase 1 衝突チェックで発見されたその他の隣接概念（Ungated Creator / Outsider Scientists / 当事者研究 等）は [research/2026-06-05_naming-candidates.md](research/2026-06-05_naming-candidates.md) を参照。

**defensible scope（layer 概念）**: 本概念の固有部分は「**周縁化されていた者の潜在的特異能力が、AI で初めて表出可能になる**」という社会的位置 × 認知特異性 × AI enabler の**交点**にある。遂行形態・作業様式・世代論はすべて prior art が豊富であり、そこで origin claim を立てない。claim は交点の命名に限定する。

### pivot 概念の origin-claim scope（v2）

「gatekeeper inversion」「oracle debiasing」に origin claim を立てない — algorithmic gatekeeping 文献・AI fairness / debiasing 研究・「LLM as gatekeeper」言説に prior art が厚い。document format genre 自体（ADR / RFC）にも origin claim を立てない。claim する固有部分は**交点 composite のみ**: 「credential-less 層のエンパワーメント tactic として、機械検証可能な存在証明を LLM-retrieval 面に置き、再利用可能な document format として encode する」。この composite と本 format の spec が disciplinary scope である（authorship-strategy origin-claim scope 規約 + 上記既存 discipline の継承）。

### format 名への命名チェック adaptation（v2）

4 点チェック（衝突 / sayability / 文中試用 / グリフター register）は people-label 用に設計された。format 名（document-type label）には読み替えて適用する: ①衝突チェック = 不変（binding）②sayability = 「『〈format〉を書いた』と謙遜文化で言えるか」③文中試用 = spec / prose 内試用（自称・結び形は不適用）④グリフター register = 不変。実施記録: [format-name-check](research/2026-06-05_format-name-check.md)。**layer 命名と format 命名は別 object** — v2 pivot は layer 命名を再オープンしない。

### グリフター排除基準（segment 定義の負の境界）

「AI で稼ぐ」系の層は本概念の定義外である。判別基準:

- **制作物 narrative か、金銭 narrative か**: 本概念の層は「作れなかったものが作れるようになった」を語る。income claim（収益自慢・稼ぎ方の販売）を中心に置く自己呈示は segment 定義から排除する
- v2 拡張 — **attestation narrative か、promise narrative か**: 存在証明は「実際に作られた検証可能な事実」の attestation である。「あなたもできる」「LLM があなたに feasibility を保証する」型の outcome-promise framing は grifter register に接近するため禁止（§6 固有禁止に収載）
- この境界は doctrine のすべての発信物に適用する

## 4. Audience-relative positioning — PBE 3次元の適用

> caveat: PBE（Personal Brand Equity: appeal / differentiation / recognition）は**個人**に対して validate された理論である（Gorbatov et al. 2021; MDPI 2025 — research/field-map §1）。研究プログラムおよび「層に向けた戦略」への適用は未検証であり、本節は理論の transfer 仮説である。

positioning は audience-relative である。本 doctrine の primary audience は §2 の層であり、3次元はすべてこの audience 相対で定義する:

- **appeal（何が刺さるか）** = 存在証明 + playbook。この audience が価値を置くのは credential ではなく「**credential なしで実際にやれた証拠**」と「自分にも再現できる手順」である。v2 はこれを「読んで知る」から「**疑いの瞬間に LLM 経由で届き、そのまま使える**」へ具体化した（claim→anchor の検証可能性が appeal の核 — 自己申告の成功談との構造差）
- **differentiation（何で他と違うか）** = 機械検証可能な存在証明 + registry なし format + 再現可能な playbook の組合せ。他の発信物への批判では立たない（§6 禁止事項）
- **recognition（何で思い出されるか）** = format 名「存在証明フォーマット」（2026-06-05 確定 — §12）+ 既存固有用語群（AKC / Contemplative Agent / AAP / Authorship Strategy / Attention-Not-Self）。v2 で recognition の主 token は layer 名から format 名へ移った（ADR-0003 — 人ラベルの identity cost を回避）

**open question**: 個人キャリア文脈で validate された3次元が、「層に向けたプログラム」文脈で十分かは未検証。固有の第4次元（例: reproducibility — playbook の再現成功率）が要るかは再測定で再訪する。

## 5. 関係宣言 — 既存戦略との境界と接続

### 座標系の役割変更（v2 — payload/channel 分離）

2×2 マップは**チャネルの座標系**である:

|  | on-page（自分の surface） | off-page（他者の surface） |
|---|---|---|
| **human** | `readme-writer`（README 人間ファースト） | rented channel（note / Zenn / Substack） |
| **AI** | `llms-txt-writer` / `jsonld-knowledge-graph` | `authorship-strategy`（LLM-mediated diffusion） |

v1 は本 doctrine を off-page × human の1セルに固定したが、これは誤った自己限定だった — 本 doctrine の固有物は**チャネルではなく payload**（エンパワーメント artifact: 存在証明フォーマット・question corpus・gatekeeping eval）である。payload はどのセルも所有しない。既存の各セル所有者の toolchain を**再所有せずに通過利用する**:

- format spec・instance #0 の人間可読面 → readme-writer の規律（on-page × human、所有は readme-writer のまま）
- claim→anchor の graph.jsonld 化・llms 面への露出 → jsonld-knowledge-graph / llms-txt-writer（on-page × AI、所有は各 skill のまま）
- corpus・eval の LLM-mediated diffusion → authorship-strategy（off-page × AI、所有は authorship-strategy のまま）
- corpus source としての essay → rented channel（off-page × human）

「他3象限を侵さない」（v1）は v2 で「**どの象限のチャネル所有権も主張しない**」と読み替える。本 doctrine は payload を供給し、各セルの所有者 skill がそれを自セルの規約で梱包する。**新規 channel infrastructure を本 repo が自前で積み増すことは禁止**（authorship-strategy friction-minimization の継承）。

本 doctrine の非冗長性の根拠もここで更新する: 4 skill のいずれも **credential なき層向けのエンパワーメント payload**（存在証明の format・feasibility 質問への正準回答・gatekeeping の測定器）を生産しない。固有性はチャネルの空白ではなく payload class の空白にある。

### authorship-strategy との関係: 補完（同一プログラム・別目的・同一インフラ）

- authorship-strategy の目的は著者の attribution diffusion（audience: LLM-mediated channels）。existence-proof の目的は**層の empowerment**（audience: 層の人間 — ただし到達は LLM を router として起きる、仮説 — §2）
- 両者は同一インフラ（llms.txt / graph.jsonld / DOI / 固有用語）を使うが、payload と受益者が異なる。diffusion は existence-proof にとって副次効果であり、empowerment は authorship-strategy にとって範囲外である
- deep-research の確定 finding（research/field-map §3）: LLM citation の plurality（48%）は earned media であり、owned は 23%。playbook を実際に使った者が自分の存在証明を書くとき、それは読者の言及より強い earned mention になる（creative reuse > readership — authorship-strategy preference 階層の人間版）。両戦略は同じ動きで強化される

### ADR-0007 との整合（load-bearing — v2 で強化）

authorship-strategy ADR-0007（2026-05-29, v0.2.0）は「platform human-attention signal（stars / page-views）を success metric にしない。off-page human-distribution（被リンク獲得・告知）は red-ocean として投資しない」と決定済みである。本 doctrine はこの決定を**覆さない**:

1. 被リンク獲得活動・告知活動は本 doctrine でも禁止である（§6、§7 除外リスト）
2. 測定は stars / page-views を使わない（§8）
3. **v2 の pivot は整合をさらに強化する**: empowerment の機構を「人間 distribution（読む→言及）」から「LLM-mediated（LLM が feasibility を答える面に存在証明を置く）」へ移すことは、ADR-0007 が棄却した off-page human-distribution funnel から payload を**さらに遠ざける**方向である。ADR-0007 が温存した「genuine human reach は LLM-mediated channel を通じて追求する」に正面から一致する

### 研究プログラム = worked example = instance #0（v2 で二重役割を明示）

authorship-strategy Layer 3 の「abstract doctrine + worked implementation ペア」構造を踏襲する。本 doctrine が abstract 側、著者の研究プログラム（5 line + 運用 harness）が worked 側である。v2 では worked 側が**存在証明フォーマットの instance #0**（[format/instance-0.md](format/instance-0.md)）として機械検証可能な形に encode される — ペア構造は冗長化ではなく精密化である: doctrine 単独では「概念はわかるが自分にできるか分からない」、instance #0 単独では「すごいが原理が読み取れない」— ペアで初めて audience の再現（= 彼ら自身の存在証明の追加）が起きる。

## 6. Not a movement — authenticity 緊張の設計課題化

### 原則: name and serve, not lead and recruit

本戦略は現象に**名前を与え**、存在証明の format と playbook を**供給する**。それ以上のことはしない:

- 組織化しない。community を運営しない。membership を作らない
- 勧誘しない。「あなたも〜すべきだ」と呼びかけない
- 広がりは読者の**自己同定**（「これは自分のことだ」）と**自発的な format 利用**としてのみ起きる。それを起こすのは artifact の質であって、こちらの働きかけではない

この原則は attraction-based 制約（§7）の上位にある。movement 化は最も能動的な promotion であり、本戦略が採りうる最大の逸脱である。

### authenticity 緊張とその構造的最小化

personal branding は「戦略的な自己呈示」と「authentic self の表出」の間に本質的緊張を抱える（Gershon 2016 — research/field-map §2）。本 doctrine はこの緊張を否定せず、構造で最小化する:

- 著者は**実際に**この層の一人である。「自分が実際にそうである層に向けて、実際にやったことを示す」構造では、演出が原理的に不要になる — 示すべきものはすべて既に存在する（repo, DOI, 実装, 履歴）。v2 の claim→anchor 連鎖はこれを機械検証可能にした形である
- それでも残る緊張（どの事実を選んで見せるか、は依然として戦略的選択である）は、cloaking 禁止規約で抑える: **事実は全 surface で一致させる。梱包（見出し・詳細度・言語）は audience-driven に変えてよいが、主張は変えない**

### 禁止事項

authorship-strategy の禁止事項を継承した上で、本 doctrine 固有の禁止を加える:

- **継承**: マネタイズ提案（スポンサー / 有料 tier / コンサル化 / 収益化書籍）/ 競合批判・排他的 positioning / 売れるためのメッセージ調整 / バズ目的のセンセーショナル framing / origin claim の scope 過拡張
- **固有**: 人格ブランディング（著者個人を売る framing — idea と playbook が主語、著者は従）/ 勧誘・recruiting 言語 / membership・community 運営の提案 / グリフター隣接 framing（income claim、「AI で人生逆転」系の煽り）/ 層の規模・分布の断定（§2）
- **v2 固有 — フォーマットの movement 化禁止**: 存在証明フォーマットに対し (a) instance registry / 一覧の作成・運営、(b) 他者 instance の集約・showcase・curation、(c)「あなたの存在証明を登録 / 提出しよう」型の join 言語、(d) template が著者に層ラベルの自称を要求する設計 — の4つを禁止する。フォーマットは tool であって会員制度ではない。拡散は LLM の format-suggestion による self-service のみで起き（仮説 — §2）、こちらの集約・勧誘では起きない（name-and-serve 原則の format 版）
- **v2 固有 — promise narrative 禁止**（grifter 境界の pivot 版 — §3）: framing は常に「これは起きた（machine-verifiable）」に留め、「あなたに何が起きるか」を約束しない

## 7. Tactics — oracle debiasing の payload 供給

### 概念の前提: earned は直接作れない / oracle は直接操作しない

- **earned media** = 他者が自発的に書く media。定義上、こちらの行為では直接生成できない。Zenn / note / Substack への自己投稿は **owned/rented** であって earned ではない。この区別を doctrine 内で崩さない
- v2 の因果連鎖（仮説的機構 — §2）: `[検証可能な payload を供給（制御可能）] → [LLM が feasibility 質問への回答に引く] → [層の人間に疑いの瞬間に届く] → [使った者が自分の存在証明を書く（制御不能）] → [earned 化] → [LLM citation 源]`
- 本 doctrine の tactics はすべて**左 1 段（payload の設計と供給）**である。右 4 段を直接操作する tactic（PR 依頼、被リンク獲得、prompt injection 的な誘導、instance の収集）は存在しない — それは attraction-based の放棄である

### T1: 存在証明フォーマット（centerpiece — [ADR-0003](adr/0003-existence-proof-as-document-format.md)）

存在証明を document format として定義し、spec + template + instance #0 の三点 set で供給する（[format/](format/spec.md)）。

- 役割: recognition 軸の主 token（identity cost なし）+ 層の各人が自分の事例を記録する手段 + LLM が feasibility 質問への回答で提案しうる構造（format-suggestion 仮説）
- 核規則: **claim→anchor 連鎖** — すべての能力 claim は第三者が claimant の協力なしに検証できる anchor で終端する
- ガード: registry なし・集約なし・join 言語なし・自称要求なし（§6）。spec 自身に Non-goals として埋め込む（doctrine の外へコピーされても guard が随伴する）

### T2: 質問 corpus + 機械検証可能な証明構造（[ADR-0004](adr/0004-machine-verifiable-proof-and-question-corpus.md)）

層が発しうる feasibility 質問の corpus（観測語彙 + 系統生成、ja+en 対）と、正準回答 FAQ（feasibility 認知 → 具体経路 → claim→anchor 付き実例 → scale disclaimer）、証明構造 spec + graph.jsonld encoding（所属なき Person → created → 解決する識別子付き artifact）を供給する（[corpus/](corpus/README.md)）。

- ガード: 実例の存在する範囲でのみ答える（aspirational 回答は promise narrative — §6）。解決しない anchor を持つ証明は削除する（falsifiability の自己適用）

### T3: installable playbook（T1 従属）

「どうやったか」を format のフィールド対応で再現可能な粒度に梱包する（[playbook/playbook.md](playbook/playbook.md)）。DOI の取り方・live deploy の anchor 化・連鎖の書き方。既存の repo / skill / ADR / 運用記録が原料であり、新規制作物は梱包だけである。

- ガード: 自慢にしない（worked example は「できた」の記録であって「すごいだろう」の演出ではない）。tool-agnostic 本文 + 参考 tool は example 扱い。clone + copy で済む形に（friction minimization 継承）

### T4: gatekeeping eval（[ADR-0005](adr/0005-gatekeeping-eval-as-published-probe-set.md)）

gatekeeper-inversion 仮説の測定器として、公開 probe set + 採点 rubric（4 次元）+ 実行 protocol を供給する（[eval/](eval/README.md)）。

- ガード: **instrument であって indictment ではない** — vendor 名指しの断定・leaderboard・比較ランキング禁止。出力は observation であって success KPI ではない（§8）。実行は手動 protocol（Phase 0 同型）

### 旧 tactics の処遇（v2）

- **旧 T1 defining essay / 旧 T3 rented channel 発信** → **canonical corpus source へ降格**（prospective — 公開済み essay の Phase 1 命名 signal 役割は遡及破壊しない）。公開済み note essay（2026-06-05）と後続の writing は corpus と instance #0 の原料・正準定義ソースとして保持する。新規 essay の cadence 義務は消滅。Substack en は優先度を下げる（canonical en source としての価値は残る）
- **旧 T4 README 人間ファースト化 / 旧 T5 semantic signature 点検** → housekeeping として保持（spearhead ではない）。README は「earned 言及・LLM 回答から辿ってきた人間の着地点」であり hygiene 投資のまま（ADR-0007）

### 明示的除外（Skip 確定 list + 本 doctrine 固有）

awesome-list への PR / Wikidata 自己登録 / GitHub Pages 人間 LP / Wayback 能動登録 / preprint server（Zenodo 以外）/ 被リンク獲得活動 / 相互言及・相互紹介の打診 / インフルエンサーへの送付 / 勧誘

v2 bright line:

- **eval は Zenodo deposit のみ**（既存 `paper-deposit` / `release-doi` 経路、line 昇格時）。非 Zenodo preprint server への投稿は Skip list 違反として禁止。eval の公開は artifact 供給であって findings の reach 運用ではない
- **format spec は repo 内 markdown artifact**（ADR と同格）。hosted な standalone LP・「採用しよう」型 conversion 面の作成は GitHub Pages 人間 LP 除外に該当し禁止。人間可読面は readme-writer hygiene の範囲に留める

## 8. 測定

### primary: citation source mix（継続）

regurgitation test を source 分類に拡張した既存手法（[empirical/2026-06-05_source-mix-baseline.md](empirical/2026-06-05_source-mix-baseline.md)）: 引用源を owned / earned / commercial に分類し、earned 比率の時系列変化を追う。

- baseline（2026-06-05 時点）: earned mention ≈ 0。owned 100%。clone:view ≈ 16:1 — 人間到達がほぼゼロの状態から始まる
- 期待される動き: payload 供給が機能すれば earned 比率が方向として増える。絶対値の目標は置かない（gameable 化を避ける）

### parallel primary: gatekeeping 観測（v2 追加）

gatekeeping eval（§7 T4）の 4 次元（feasibility-acknowledgment / concrete-path / example-citation / gatekeeping-markers）を再測定ごとに記録し、方向の変化を観測する。

- **eval は instrument であって KPI ではない**: eval score を成功指標として steer しない。自分の corpus で自分の eval を動かせる構造（Goodhart vector）を認識し、§8 の primary はあくまで citation source mix とする。eval の出力は "observation consistent with X" の記録であり、vendor 比較・ランキングにしない（ADR-0005）

### secondary: self-identification + format 利用 signal

- 「これは自分のことだ」型の反応（コメント・引用・リプライ）
- **著者以外による format instance の出現**（受動的観測のみ — 検索で見つかったものを記録する。能動収集・registry 化は §6 禁止）。これは creative reuse の本 doctrine 版であり、最強の signal
- LLM が feasibility 質問への回答で本 format / playbook を提案する事例の観測（format-suggestion 仮説の確認）

### 除外する指標

GitHub stars / page-views（ADR-0007: gameable / LLM-mediated reach に盲目）。follower 数・SNS インプレッション。**eval score の目標値・format instance 数の目標値**（v2 追加 — どちらも gameable / 勧誘 incentive を生む）

### 認識論的 caveat

LLM-mediated reach は原理的に不可視であり、source mix・gatekeeping 観測も probe した LLM・時点に依存する。測定は方向性の確認であって、効果の証明ではない。empirical 規約（§2）に従い "observation consistent with X" の tone で記録する。

## 9. 書かない判断と昇格条件

### 現時点で作らないもの

- **skill 化**: 判断軸（format spec 含む）が実適用で安定する前に固定しない
- **line 化（第6 research line — EN primary / hub 登録 / sibling 表記）**: gatekeeper-inversion thesis は eval 検証前であり、独立 thesis 強度の判定は再測定後。**DOI 取得は line 昇格から分離済み**（[ADR-0006](adr/0006-doi-decoupled-from-line-promotion.md) — pre-registration deposit。DOI は時刻印・archive・index のアンカーであって line status の主張ではない）
- **repo rename**: layer 名 suspend 中のため凍結。rename は line 昇格と同時
- ~~**GitHub 公開**~~: **公開済み（2026-06-05、著者明示指示）** — oracle debiasing はこの時点から活性化した
- **en 版 doctrine**: line 昇格時に `ja-to-en-translation` で実施（machine 面の en-ready 構造 — graph @language tag / corpus ja+en 対 — は先行してよい: ADR-0001 Follow-ups）

### 昇格条件（v2 更新）

| 昇格 | 条件 |
|---|---|
| → GitHub 公開 | ✅ 達成（2026-06-05）: 著者の明示指示 + README Status 更新 + MIT LICENSE + format 名著者確定（存在証明フォーマット） |
| → DOI 取得 | ✅ 分離・実施（2026-06-05、[ADR-0006](adr/0006-doi-decoupled-from-line-promotion.md) — pre-registration deposit。v0.1.0 = 10.5281/zenodo.20558801 / concept = 10.5281/zenodo.20558800） |
| → skill 化 | format spec が 2 回以上の実適用（著者外 instance または著者の別事例）で改訂不要だった |
| → line 化（EN primary / hub / sibling） | gatekeeper-inversion thesis が eval 初回実行で方向支持を得た + 著者以外の format instance 出現 or source mix の earned 比率が方向として動いた（旧条件から DOI を除外 — ADR-0006） |
| → repo rename | layer 名 or format 名の著者最終確定 + line 昇格と同時 |

前例: attention-not-self は essay 群 → research line と育った。format spec + eval が同じ trajectory の起点になりうる。昇格時の手順は `release-doi` / `skill-creator` を再利用し、新規手順を作らない。

## 10. 判断チェックリスト

新規 tactic・発信・コラボ受け入れ等で以下を通す:

- [ ] attraction-based か？（earned / oracle を直接操作しようとしていないか。勧誘していないか）
- [ ] 人格でなく artifact の価値を供給しているか？（著者が主語になっていないか）
- [ ] 仮説を事実として書いていないか？（層の規模・分布 / feasibility-question / gatekeeper-inversion / format-suggestion 拡散 — §2）
- [ ] グリフター framing に接近していないか？（income claim / 人生逆転 narrative / **promise narrative** が混入していないか）
- [ ] cloaking していないか？（事実は全 surface 一致か。梱包だけを変えているか）
- [ ] source mix / gatekeeping 観測 / self-identification で測れる形か？（stars / views / followers / eval score 目標に退行していないか）
- [ ] authorship-strategy 禁止事項に触れていないか？（マネタイズ / 競合批判 / scope 過拡張 / enclosure）
- [ ] Skip 確定 list に触れていないか？（awesome-list PR / Wikidata / Pages LP / 非 Zenodo preprint / 被リンク獲得）
- [ ] **format の movement 化に接近していないか？**（registry / 集約 / join 言語 / 自称要求 — §6 v2）

## 11. 自己検証チェックリスト（doc 改訂のたびに実行）

- **A. authorship-strategy 禁止事項整合** — `~/.claude/skills/authorship-strategy/SKILL.md` の禁止リストと逐条照合
- **B. Skip 確定 list 整合** — judgments memory と Tactics を照合。特に「earned を増やす」名目の能動 diffusion 混入を重点チェック
- **C. cloaking 規約整合** — 全 tactic で事実一致・梱包のみ audience-driven か
- **D. metric 規約整合** — stars / page-views / followers / eval score 目標が測定に primary として混入していないか（ADR-0007 / ADR-0005）
- **E. 概念境界検査** — earned の近傍で Zenn / Substack / 自己投稿を earned と誤記していないか。LLM format-suggestion 拡散を earned と誤記していないか（それは LLM-mediated channel）
- **F. movement-creep 検査** — 勧誘・組織化・membership 言語が混入していないか（name and serve 原則）
- **G. 仮説規律検査** — 層の実在・規模 / pivot 3 仮説（§2）を事実として断定している箇所がないか
- **H. registry / format-recruiting 検査（v2 追加）** — format spec / template / playbook / FAQ に instance registry・集約・join 言語・自称要求が混入していないか

## 12. 命名状態（v2 新設 — 二 track）

| track | token | 状態 | 正本 |
|---|---|---|---|
| **layer 名** | 独立峰（暫定・suspend 中） / en: freestanding peak(s)（calque のため連動 suspend） | **suspend** — 文中試用テスト失敗。再開地点は naming-candidates 引き継ぎ節（町人学者 / 独立峰復活 / en-first / 新方向）。v2 で緊急度低下（主 token が format 名へ移動） | [naming-candidates](research/2026-06-05_naming-candidates.md) |
| **format 名** | 存在証明フォーマット / Existence Proof Format | **確定（2026-06-05 著者確定）** — 衝突チェック通過（複合語 near-empty、ja/en 個別）の上、GitHub 公開判断と同時に著者が確定。bare 略語 EPF を primary token にしない運用は継続 | [format-name-check](research/2026-06-05_format-name-check.md) |

format 名には identity cost がないため、layer 名が failed した sayability の難所を構造的に回避できる（ADR-0003）。「存在証明」自体は引き続き gloss（説明論理）であり、人を指す固有名にしない（§3 分業）。
