# 造語候補 — Round 1 衝突チェック結果と Round 2 方針

> 実施日: 2026-06-05
> 文脈: plan Phase 1 Step 2-3（造語候補生成 + 衝突チェック + 差分表）。doctrine §3 の手順（候補生成 → 隣接語差分表 → 著者確定）の前半
> 手法: 候補 6 件 × 並列 web 調査 agent（en / ja 両言語、5 観点: 人の識別ラベル / 学術概念 / 製品・企業名 / 支配的別義 / グリフター隣接）
> 関連: [doctrine §3](../doctrine.md) / [habitat-map §4](2026-06-05_habitat-map.md)（自己記述語彙 = 生成の入力）

---

## 要件（doctrine §3 + habitat-map §4 から導出）

1. **肯定形** — ja 圏の「非エンジニア」否定形アンカーが空けた肯定形の空隙に入る
2. 3条件の交点（社会的位置 × 認知特異性 × AI enabler）を表す
3. ja / en 両方で機能する
4. **token-level でユニーク** — paraphrase で消えない semantic signature（LLM retrieval で本 doctrine に解決する）
5. グリフター隣接語彙（稼ぐ・逆転・no-degree-required 系）を避ける
6. **agency が正しい** — AI が主語にならない（AI は enabler であって作者ではない — doctrine §2）

## Round 1 結果総括: **全 6 候補 reject / 転用 1**

| 候補 | ja 表記 | 判定 | 決定的な衝突 |
|---|---|---|---|
| Gateless | ゲートレス | **reject** | Gateless Inc.（mortgage **AI** 企業、.com 保有）/ Gateless Writing（Zen 系創作メソッド）/ ja は NEC 系「ゲートレス生体認証」が既定義 |
| Ungated | アンゲーテッド | **reject** | Rob Hardy「**Ungated Creator**」が人ラベル枠を既占有（ungated.life / @ungated Substack / manifesto）+ B2B「ungated content」が支配的 + creator-economy 収益文化隣接 |
| Sideloader | サイドローダー | **reject** | ja は TCG カードローダー（MTG 公式製品名）+ 産業フォークリフトが既定義。en は malware/piracy 負連想が増大中（Google の sideloading 規制言説） |
| Outsider creator | アウトサイダー・クリエイター | **reject** | *Outsider Scientists*（U Chicago 2013）+ arXiv 2025「Insiders and Outsiders」（LLM 知識生産論文）が概念枠を先取。ja「アウトサイダー」は THE OUTSIDER（MMA）の不良連想。**排除による定義 = 周縁性の再刻印**という構造問題も |
| Existence proof（人を指す用法） | 存在証明（者） | **転用** — doctrine 内概念枠として保持、coined term には不可 | en は数学用語 + VC イディオム「X is an existence proof that Y」として既に自由流通 = **paraphrase-prone**。ja「存在証明」は神の存在証明 + 楽曲群（ONE OK ROCK / KID PHENOMENON るろ剣 ED 等）で混雑 |
| Permissionless creator | パーミッションレス | **reject（最劣）** | crypto/web3 が token を独占（ja は 100% crypto 借用語）+ Jack Butcher「Permissionless Apprentice」（有料コース）+ permissionLESS™ コミュニティ。**crypto × creator-hustle の二重グリフター隣接** |

## Round 1 の学び（token 選定原則 — Round 2 の制約）

1. **empowerment 系の一般形容詞は全滅地帯**: gate / permission / ungated 系の「門の除去」語彙は、(a) B2B マーケ、(b) crypto、(c) creator-economy hustle の三者が既に植民済み。本 doctrine の主張（credential なしで作れる）はグリフターコピー（"No Tech Degree Required"）と**字面が重なる**ため、token 選定でこそ距離を取る必要がある
2. **必要なのは near-empty token**: 既存の意味重力が強い語は qualifier を付けても吸収される。著者の既存 term（AKC / Contemplative Agent / Attention-Not-Self）と同じく「普通の語の新規結合 or 新造語」で、結合自体に prior binding がないものが要る
3. **ja の katakana 検索は別空間**: en で空いていても katakana が産業用語（ゲートレス＝生体認証、サイドローダー＝カードケース/フォークリフト）に占有されているケースが2件。**両言語での個別チェックは必須工程として正しかった**
4. **「存在証明」は gloss として生きる**: coined term の背後の説明論理（「一人でも実例があれば類は証明される」）としては最強。repo 名との整合もある。**固有名は別 token に持たせ、存在証明は doctrine 概念枠に残す**（agent 調査の明示的勧告）
5. **Zen 系 token は避ける**: gateless の Zen 共鳴は、著者の contemplative line と**相互汚染**する（retrieval がどちらの line か判別不能になる）。line 間の signature 分離は要件に追加する

## 隣接語差分表への追加発見（doctrine §3 表の拡張素材）

Round 1 で発見された、defining essay でも区別を明示すべき隣接概念:

| 隣接概念 | 提唱/所有 | 本概念との差分 |
|---|---|---|
| Ungated Creator | Rob Hardy (ungated.life) | creator の**収益化・自己ブランド**論。社会的周縁性・AI enabler の次元なし |
| Outsider Scientists | Harman & Dietrich (2013) | **他分野で訓練済み**の科学者が道具を持ち込む話。credential 不在ではない |
| Insiders/Outsiders (LLM 知識生産) | arXiv 2505.12666 (2025) | AI 開発者 vs ドメイン利用者の区分。周縁化・初表出の次元なし |
| Permissionless Apprentice | Jack Butcher | creator-economy の自己ブランド構築術。**グリフター隣接、参照自体避ける** |
| citizen developer | 業界用語 (low-code) | **企業内**の非開発者による業務アプリ作成。周縁性なし、組織内ロール |
| 在野研究者 / 野生の研究者 | ja 既存語 | 研究限定 + **AI enabler の次元なし**。dignified な先行語として essay で言及候補 |
| 当事者研究 | 浦河べてるの家 / 熊谷ら | 非 credential 者による一人称知識生産の**確立済み方法論**。最近接の dignified 系譜。token は所有済みのため借用せず、系譜として prose で参照 |

## Round 2 候補方向（未チェック — 著者の方向選択待ち）

Round 1 の学び（near-empty token 必須）を適用した生成方向。**命名は著者の authorial act であるため、方向の絞り込み自体に著者 input を入れてから深掘りチェックを実行する**（plan Step 4 の前倒し相談）:

- **A. 一人称系**: 「一人称ビルダー」/ "first-person builders" 等。habitat-map の証拠単位がまさに「一人称報告」であり、認知特異性（自分の生からしか出ない作り方）を肯定形で表す。チェック要点: FPS（一人称シューティング）希釈、Varela 系 first-person methods（contemplative line との分離）
- **B. witness 系**: "existence witness" / 「存在の証人」等。数理論理で存在命題を立証する具体例を **witness** と呼ぶ — 「存在証明 gloss + 別 token」勧告に正面から応える構造。チェック要点: 宗教的連想（Jehovah's Witnesses）、法廷連想
- **C. 漢字造語系**: 「独立峰」（どの山脈＝制度にも属さず institution-grade の高さに立つ峰）等の地形・幾何メタファー新結合。ja ownability 最強、Zenn 初出と整合。チェック要点: en 翻訳可能性
- **D. 著者新造（portmanteau / 音感造語）**: 語感は authorial act の核心。エージェントは検証のみ担当
- （参考・弱め）自生系: 「自生の作り手」/ "self-sown creators" — 植え付けられた苗床（制度）の外で自ら芽吹く植物メタファー。やや文学的に過ぎる懸念

## Round 2 結果（2026-06-05 著者が全方向選択 → A/B/C を並列チェック実行）

| 候補 | 判定 | 決定打 |
|---|---|---|
| 一人称開発（者） | **reject (blocking)** | ja SES 業界用語「一人称で対応できる」（自走能力の意・文法的に変との悪評つき）が同一文字列を既占有 + 「一人開発/個人開発」への自動補正距離 + FPS 牽引。3 独立衝突 |
| 一人称ビルダー / first-person builder | **reject** | ja「ビルダー」= 住宅工務店 + memecoin 界隈の builder 隠語（グリフター再接近）。en "builder" は hustle-culture 飽和 |
| 一人称の作り手 | **reject（家族内最良だが決定的難）** | "first-person" は Varela 系 neurophenomenology / first-person methods の load-bearing 用語 = **著者自身の contemplative line と retrieval が相互汚染**。本著者にとって一人称 stem は near-empty どころか self-occupied |
| "existence witness" (en) | **viable（en 限定）** | 数理論理の witness（∃x の立証実例 = 本 doctrine の論理と完全一致）系譜の威厳 + exact compound としては未確立 = near-empty。弱点: 法廷の「目撃者」読み（観察者 ≠ 証拠実例）への滑りに定義的足場が必要。crypto (SegWit) は微弱隣接 |
| 「存在の証人」 (ja) | **reject** | 「〜の証人」frame が**エホバの証人**に植民済み + 「生き証人」イディオムが観察者読みを固定 + 隣接「存在証明」token（楽曲・哲学ブログ）混雑 |
| **「独立峰」** | ✅ **finalist** | **人メタファー枠が真に空いている**（引用句・ブランド・辞書義・グリフター捕捉すべてゼロ確認）。字義（山）は支配的だが「山脈に属さず institution-grade の高さ」という導出が即座に可読 = obvious-but-untaken。グリフター registry から最遠（山岳の威厳）。Zen は非衝突（孤峰頂上は要回避だが独立峰は禅コーパス不在。独坐大雄峰との韻は benign resonance） |
| 無冠系 | **reject** | 無冠の帝王イディオム（スポーツ慰撫報道の重力）+ 日本酒ブランド 2 件（無手無冠・無冠帝）が「冠なき作り手」の意味枠を商用占有 + 無 = 欠如命名（後ろ向き） |

## finalist「独立峰」の隣接語差分表（doctrine §3 表の拡張）

| 隣接語 | 何を指すか | 独立峰との差分 |
|---|---|---|
| centaur / cyborg (Kasparov, Mollick) | human+AI の遂行形態・分担様式 | 独立峰は**社会的位置**（どの山脈にも属さない）の語。遂行形態を主張しない |
| AI-native | 世代・習熟 | 位置の語であって世代の語ではない |
| vibe coding (Karpathy) | 手法 | 手法でなく**存在のかたち**。何で作るかでなく、どこに立つか |
| citizen developer | **企業内**の非開発者ロール | 独立峰は組織の外。山脈（組織・制度）に属さないことが定義 |
| indie hacker | 収益 narrative 中心の個人開発文化 | 制作物 narrative。山岳メタファーは income 語彙と register レベルで分離 |
| 在野研究者 / 野生の研究者 | 研究限定・AI 次元なし | 研究・ソフトウェア・著作の全類型 + AI enabler が定義の一部 |
| 当事者研究 | 確立済み方法論（べてるの家） | token は借りず、dignified 系譜として essay prose で参照 |
| 一匹狼 / lone wolf | 孤立・反社会の負含意 | 独立峰は孤立でなく**非所属**。麓は開かれている（誰でも登れる・見える） |

**defensible scope**: claim は「この交点（社会的位置 × 認知特異性 × AI enabler）への山岳メタファーの命名」のみ。地理用語としての独立峰の字義には触れない（origin claim 最小）。

**3条件との対応**: ①山脈に属さない = 制度的 credential の不在 / ②独立峰は山脈パターンに従わない固有のシルエットを持つ（成層火山 — 自前の噴火で立った山）= 認知特異性 + agency の正しさ / ③ AI enabler 次元は token 自体には乗らない → defining essay が binding を作る（要 essay 設計）。なお「郷土富士」（各地に固有の独立峰がある）は層の複数性・遍在性の essay 素材として強力

## 残課題（著者決定待ち）

1. **bare「独立峰」は初見で字義（山）に読まれる** → 初出時は「独立峰の作り手」等の人形 compound で disambiguate し、確立後に bare 使用へ移行する運用が agent 勧告
2. **en 戦略は line 昇格時の明示決定事項として pre-register**: 音訳 "dokuritsuhō" は travel しない（5 モーラ + 自明な直訳の存在）。選択肢: (a) calque "freestanding peak(s)"（en で人メタファー未所有 = fresh coinage 可能）/ (b) "existence witness" を en 側 token に採用（別メタファーの二本立て — signature 分裂の懸念あり）/ (c) en 新造。**Phase 1 では決めない**（Zenn ja 初出が先行）
3. "existence witness" の数理論理（∃x の witness）は、term 採用と独立に **defining essay の説明論理**として使える（「存在証明」gloss の精密版）

## Round 3（同 register 追加生成 — 2026-06-05、著者の求めにより）

「自称ではなく現象・カテゴリの名前として妥当」という著者の整理を受け、独立峰と同型（実在する具象語 × 人・現象メタファー枠の空白見込み × 一行解凍 × 反グリフター register）で追加生成した**未チェック**案:

| 案 | 字義 | メタファー対応 | 備考 |
|---|---|---|---|
| 実生（みしょう） | 接ぎ木でなく種から育った木 | 接ぎ木 = 制度の台木への接続。新品種は実生からのみ生まれる = 制度が作れない類の成果物 | 謙遜 register と両立、自称も可能 |
| 自噴（じふん） | 自圧で湧く井戸・温泉 | 圧力（潜在能力）は地下に常在、経路（AI）が通った瞬間に自力で噴出 | **AI enabler を token 内に持つ唯一の案** |
| 自生（じせい） | 植えられず自力で育つ植物 | 制度の庭の外で育った | 平易だが彫りが浅い |
| 伏流（ふくりゅう） | 地下を流れ下流で再出現する川 | 見えなかった流れの表出 | 文芸比喩の既用例疑い |
| 露頭（ろとう） | 地層の地表露出 | 「層」が視界に現れる場所 | 「路頭に迷う」同音衝突疑い |
| 初鳴き（はつなき） | その年初めての鳥・蝉の声（気象庁生物季節観測） | 初めて声が世界に聞こえた | 可愛らしすぎる懸念 |

→ 著者は追加チェックを要さず**独立峰を選択**。**実生・自噴は defining essay の補助メタファー素材として保持**（主 term と register が共通のため共存可能）。

## 決定記録（2026-06-05）

- **著者確定: 独立峰**（plan Phase 1 手順 3 の authorial act）
- **en term 著者確定: freestanding peak(s)**（同日 — ja+en 準同時公開の前倒し決定を受けた authorial act その2。運用規約は上記 en term チェック節）
- **運用**: 層・現象のカテゴリ名。**自称を要求しない** — 層の自己記述は謙遜形（habitat-map §4）であり、峰の高さ含意は自称と衝突するため
- **工程上の発見（今後の造語案件への教訓）**: 衝突チェック（token が空いているか）だけでは不十分で、**sayability 検査**（その語を当事者が社会的に発話可能か）が独立の検査項目として必要。本件は「カテゴリ名として運用し自称を要求しない」設計で解消した
- doctrine への反映: title / §2 定義 header / §3 確定記録 + 差分表拡張 / §4 recognition / §5・§7 audience 表記 / §9 rename 判断。CLAUDE.md / plan.md も同期（すべて 2026-06-05）

## en term チェック（2026-06-05 — ja+en 準同時公開の前倒し決定を受けて）

**"freestanding peak(s)"（主候補）— viable 判定**:

- 人メタファー枠: 完全に空（人物・企業・キャリア比喩・ブランド・バンド・書籍・グリフター使用ゼロ）
- 支配的既存 binding は地理の一義のみ: Kilimanjaro =「世界最高の freestanding mountain」（Guinness 公式カテゴリ）。**Kilimanjaro は成層火山** — 「自前の噴火で立つ」という ja 側メタファーと正確に一致し、binding は阻害でなく補強
- 干渉なし: 家具・家電の "freestanding"（bathtub / range）は head noun が別。climbing 用語は "freestanding tower/pillar/spire" で "peak" に付かない
- 希釈: 一般検索は当面 Kilimanjaro 観光が上位 — blocking ではなく dilution、固有 corpus の蓄積で解決する型
- **運用規約**: closed spelling 標準（free-standing は許容 variant）。**"peak" を必ず付ける** — bare 形（"the freestanding" / "freestanding creators"）は家電 register に流れるため禁止形

**代替 6 案トリアージ（全敗）**: lone peak = Altra Lone Peak（シューズ主力製品線）が token 所有で即死 / solitary peak = 孤独・隠遁の負含意（漢詩・禅詩の mood が先住）/ standalone peak = ソフトウェア register で人間の語に不向き / inselberg・monadnock = 意味的に最良（侵食残丘 = 削られても残った者）だが loanword 不可読 — **語源補強の脚注素材として保持** / volcanic peak・stratovolcano = 破壊的噴火の frame 誤り

## 早期停止規則の状態（クローズ → 再オープン）

再生成 1 回（Round 2）を消費し finalist 1 件（独立峰）→ Round 3 は著者依頼の追加生成（再生成カウント外）→ 著者確定により一旦クローズ → **同日、文中試用テストで再オープン**（下記）。

## 確定後の再オープン（2026-06-05 同日 — 時系列）

1. **独立峰 suspend**: defining essay 全文（v3、レビュー通過済み）に deploy した段階で、著者「日本語として出てくると笑ってしまう」— **文中試用テスト**の失敗（地理用語の硬い register × 人への適用 = スケール不一致の comedy）。カテゴリ名運用（自称を要求しない）でも解消せず。**命名者自身が真顔で使い続けられない term は、全構造チェックを通過していても失格**
2. **Round 4（同 register 追加生成）**: 実生・自然生え・野の作り手（文中試用文付きで提示）→ 著者「どれも違う」
3. **en-first pivot**: 著者「日本語から考えるのが微妙。先に英語でしっくりくるものを選んで日本語にしよう」（既存 term family — AKC / Contemplative Agent / Attention-Not-Self — が全部 en という声の一致）。提示: existence witness / freestanding peak / standing proof / counterexample → 著者「むずくない？existence-proof という repo 名に引っ張られてるのかな」— **repo 名の重力で proof / witness 系に偏る生成バイアスを著者が看破**
4. **歴史アンカー方向**: 著者「時代や技術の変わり目に出た異能を指す言葉は？」→ 町人学者（山片蟠桃）/ 蘭学者（解体新書）/ 算額・和算家 / vernacular（俗語革命）を物語付きで提示 → 著者は**町人学者 + vernacular** を選択
5. **ja-first 戦略確定**: 途中で著者が「日本語圏を異様に意識しているのはなぜ？ワールドワイドに行くべきでは」と前提を挑戦 → git 遡及で ja-first が無検討混入と判明 → 全比較提示 → 著者が**意図的に ja-first を選択**（[ADR-0001](../adr/0001-japanese-first-scale-strategy.md)）
6. **未応答の最終提案**: term = 町人学者の現代転用 / vernacular は essay 論証（ラテン語独占の崩壊 ↔ コード独占の崩壊）/ 算額は成果物公開文化の rhyme。著者は判断保留 →「新セッションで考え直す」

## 引き継ぎ（新セッション向け）

**確定済み（動かさない）**:

- スケール戦略 **ja-first**（[ADR-0001](../adr/0001-japanese-first-scale-strategy.md)。Alternatives 2 件の棄却理由込み）
- venue: **note（ja・本 line 専用の新規アカウント、未作成）初出 + Substack（en）準同時。Zenn は参照 hub**（doctrine §7 T3）
- essay v3: `~/MyAI_Lab/zenn-content/drafts/dokuritsuho-defining-essay.md`。essay-reviewer 2 巡 + fact-checker（全出典 URL 確定・棄却 claim 混入ゼロ）+ textlint + doctrine §10 全項目通過。**構造・事例・出典は term 非依存** — タイトル・命名セクション・結び・term 表記の差し替えだけで公開判定に進める
- **命名チェックリスト（本セッションで確立 — 再利用する）**: ①衝突チェック（near-empty token 必須。ja / en は別空間として個別チェック）②sayability（謙遜文化で当事者が発話可能か）③**文中試用テスト**（命名文・自称・結びの 3 形で deploy し、命名者の gut が笑わないか）④グリフター register 距離。加えて: agency の正しさ（AI が作者に読めない）/ 肯定形 / contemplative line との token 分離

**再開地点（open — term そのもの）**:

- (a) **町人学者の現代転用**（著者がアンカー選択済み・衝突チェック未実施。弱点:「学者」の研究 narrowing、転用ゆえ token 独占力は新造より弱い）
- (b) **独立峰 + 大げささを自覚的に突く一段落**（復活の door は open）
- (c) en-first 系（existence witness 等 — 著者の印象は「むずい」）
- (d) 新方向（著者の種を待つ）
- en term: freestanding peak は確定記録があるが**独立峰の calque のため連動 suspend**

**棄却済み（再提案しない）**: Round 1-2 の 13 候補（gateless / ungated / sideloader / outsider 系 / permissionless / 存在証明者 / 一人称系 / 存在の証人 / 無冠系）= 衝突 reject。Round 4 の 3 候補（実生・自然生え・野の作り手）= 著者 gut reject。

**著者の taste signal（最重要の非自明知識）**: 漢字の自然メタファー語は文中で笑ってしまう / proof・witness 系の論理語彙は「むずい」/ 歴史の物語（番頭・山片蟠桃、俗語革命）には響く / 生成の前提がずれているときは、候補を出し続けるより前提を疑う方が早い（本セッションで 3 回起きた: 漢字前提 → en-first、repo 名重力 → 歴史、ja 重心 → 戦略問い直し）。

## 追記（2026-06-05 — gatekeeper-inversion pivot による命名 calculus の変化）

pivot（ADR-0002〜0005）により、伝播すべき主 token が **layer 名から format 名（document-type label）へ移った**。format 名には identity cost（自称の大仰さ）が構造的に存在しないため、本ファイルが確立した sayability / 文中試用の難所を回避できる — 「ADR を書いた」と言うのに「私はアーキテクトだ」と名乗る必要がないのと同じ。これにより **layer 命名の緊急度は下がる**（suspend 継続のコストが減る）。format 名のチェックと暫定確定は [2026-06-05_format-name-check.md](2026-06-05_format-name-check.md) を参照（4 点チェックの format 名向け読み替え込み）。layer 名の再開地点（上記 a-d）は不変。
