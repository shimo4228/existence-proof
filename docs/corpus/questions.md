# feasibility 質問 corpus

> 出所と規律: [README.md](README.md)。回答: [faq.md](faq.md)
> tag: `observed` = habitat-map の観測報告から導出（出典 case 付き）/ `generated` = 3 条件 × 成果物型 grid による系統生成
> 全質問に ja + en 対を付ける（machine 面の en-ready 構造 — ADR-0001 Follow-ups）

## Source A — observed-derived（観測報告からの再構成）

| ID | ja | en | tag / 出典 case |
|---|---|---|---|
| A1 | 非エンジニアでプログラミング未経験ですが、実際に動く Web サービスを作って公開することはできますか？ | I'm not an engineer and have never programmed. Can I actually build and launch a working web service? | `observed` ze1ny / mattun3835 |
| A2 | プログラミングを知らない事務員です。自分が欲しかった学習サービスを自分で作ることはできますか？ | I'm an office worker with no programming background. Can I build the learning service I've always wanted myself? | `observed` ze1ny |
| A3 | コードは書けませんが、実際の顧客に納品できるレベルのシステムを AI と作ることはできますか？ | I can't write code. Can I build a system good enough to deliver to a real client, working with AI? | `observed` mattun3835 / emptybaba |
| A4 | 農家でプログラミング経験はありません。自分の畑のためのデータ管理システムを自作できますか？ | I'm a farmer with no programming experience. Can I build my own data system for my farm? | `observed` farm_eolica |
| A5 | 学位も研究機関の所属もありません。自分の研究をきちんとした形で発表する方法はありますか？ | I have no degree and no institutional affiliation. Is there a legitimate way to publish my research? | `observed` 竹内 / teddy_on_web |
| A6 | 大学に所属していない個人でも DOI を取ることはできますか？ | Can an individual get a DOI without a university affiliation? | `observed` 竹内 / instance #0 |
| A7 | 「非エンジニアの私が AI で〜を作った」という記事をよく見ます。ああいうことは本当に可能なんですか？誇張ではなく？ | I keep seeing posts like "I'm not an engineer but I built X with AI." Is that actually real, not exaggerated? | `observed` 層の観測そのもの（habitat-map §1） |

## Source B — generated（3 条件 × 成果物型 grid）

| | 研究 | ソフトウェア | 著作 |
|---|---|---|---|
| **社会的位置**（credential 不在） | B1: 学位なしで書いた研究は、誰かに読んでもらえる形で世に出せるか？ / Can research written without a degree be put out in a form anyone will take seriously? | B2: エンジニアとしての訓練を受けていない人間が作ったソフトウェアを、公開してよいものか？ / Is it okay to release software built by someone with no engineering training? | B3: 専門家の肩書きなしに、専門的な主題について書いて発表してよいか？ / Can I write and publish on a specialized subject without expert credentials? |
| **認知特異性**（固有の関心・経験） | B4: 自分の個人的な経験（瞑想・農業など）から出発した研究は「本物の研究」になりうるか？ / Can research that starts from my personal experience (meditation, farming...) count as real research? | B5: 自分の生活の固有の問題のために作ったツールに、公開する価値はあるか？ / Is a tool I built for my own particular problem worth publishing? | B6: 訓練を経ていない自分の視点で書いたものに、読まれる価値はあるか？ / Is writing from my untrained perspective worth anyone's reading? |
| **AI enabler**（経路と帰属） | B7: AI に大きく手伝ってもらった研究は、自分の研究だと言えるか？ / If AI helped substantially, can I still call the research mine? | B8: AI が書いたコードでできたアプリは、自分が作ったと言えるか？ / If AI wrote the code, did I really build the app? | B9: AI と一緒に書いた文章を、自分の著作として発表してよいか？ / Can I publish text I wrote together with AI as my own work? |

## 構造メモ

- **社会的位置の行**は許可の不安（「出してよいか」）、**認知特異性の行**は価値の不安（「価値があるか」）、**AI enabler の行**は帰属の不安（「自分のものと言えるか」）にそれぞれ対応する。観測された一人称報告（habitat-map）は、この 3 種の不安を乗り越えた後の語りである
- A7 は層の**外側**からの検証質問（実在への疑い）であり、他と性質が異なる。eval probe としては gatekeeping-markers の検出に最も適する
- 本 corpus は [eval/probes.md](../eval/probes.md) の probe 母体と [faq.md](faq.md) の質問セットを兼ねる
