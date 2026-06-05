# 生息地マップ — AI-powered humans（仮称）の実在検証 Deep Research レポート

> 実施日: 2026-06-05
> 手法: deep-research workflow (107 agents / 25 sources fetched / 111 claims 抽出 → 25 検証 → 19 confirmed / 6 killed、3票 adversarial verification)
> 依頼文脈: plan Phase 0 タスク 3（生息地検証）。doctrine §2 の load-bearing 仮説「学位・所属・資格を持たない者が、AI によって初めて制度級の成果物を表出し始めている（世界同時多発的に）」の最初の実地検証
> 関連: [doctrine §2](../doctrine.md) / [plan Phase 0](../plan.md) / [field-map](2026-06-05_field-map.md)

---

## 結論

**層の実在仮説を支持する観測が得られた**。「制度的 credential を持たない個人が、LLM/AI によって初めて制度級の成果物を作れた」という一人称報告は、日本語圏（Zenn / note / Qiita）と英語圏（個人 blog / Medium / 報道メディア）の両方で、独立した複数の事例として確認できた。検証可能な外部アンカー（live deploy URL・解決する Zenodo DOI・複数メディアの cross-corroboration）を伴う事例が複数ある。

**ただし規模は依然として仮説である**。全事例は n=1 の存在証明の集積であり、「世界同時多発的」「高密度」は「独立した著者による複数事例が容易に発見できた」という意味であって、定量的なシェア・増加率ではない（→ Open Questions 1）。doctrine §1 の存在証明の論理（「一人でも実例があれば、その類の存在は証明される」）に照らせば、**「その類の人々が存在する」ことは観測で支持された**が、「層として世界同時多発的に出現している」という規模・分布の主張は Phase 0 終了後も仮説表記を維持する。

## 1. 生息地: 日本語圏（Zenn / note / Qiita）— 最も厚い【確度: 高】

primary first-person source（著者本人の投稿）が中心で、外部検証アンカー付き。独立した一人称事例 6 件以上:

| 著者 | 自己記述 | 成果物 | 検証アンカー |
|---|---|---|---|
| ze1ny | 事務員・プログラミング完全未経験・「`<div>` が何かも知らなかった」・独学2ヶ月 | AI 学習 SaaS『CodeSensei』（Claude API、2ヶ月で構築・ローンチ） | codesensei-iota.vercel.app live 確認（15 courses / 188 lessons） |
| mattun3835 | 非エンジニア・プログラミング経験ほぼゼロ | ドラム教室予約システム（認証・リアルタイム更新・管理ダッシュボード、3日） | Vercel + Firebase deploy、実ユーザーに納品 |
| emptybaba | コードが書けない Web ディレクター（20年） | 校正 SaaS『fuSen』のコアアーキテクチャ | fusen.cloud live 確認 |
| akinat | コーディング素人・PM 10年 | スタートアップの Flutter チーム開発に実コードで参加 | 一人称報告（primary） |
| 関口 (farm_eolica) | 個人農家・34歳・前職出版社営業・プログラミング経験ゼロ | IoT 営農システム + データスタック（センサー→Raspberry Pi/MySQL→自作 Web アプリ、BigQuery 統合、Looker Studio、市況データ約200万件、self-host n8n、versioned repo） | 一人称報告で全アーティファクトを verbatim 確認。「AI がなければこのレベルのシステム統合はそもそも不可能だったと断言できます」 |
| 竹内 | 非エンジニア・工業高校卒・学位なし・所属なし・「独立研究者」 | v5.3 AI Alignment Framework + Zenodo preprint | **DOI 10.5281/zenodo.18691357 が解決**、著者欄に「Independent Researcher (no institutional credential)」。Wantedly / Qiita / DEV で cross-corroborated |
| teddy_on_web (Chikara Kawashima) | 個人開発者（学位・所属の主張なし） | 研究 preprint 3 件を Zenodo deposit | DOI 10.5281/zenodo.18730531 解決（XPathGenie）。caveat: 「査読」は LLM 5 体によるもので human peer review ではない |

ソフトウェア事例（上 5 行）と学術事例（下 2 行）の両方が存在する点が重要 — doctrine §2 定義の「制度級の成果物（研究・ソフトウェア・著作）」のうち 2 類型が日本語圏だけで確認された。

## 2. 生息地: 英語圏 — 存在するが報道メディア経由の比重が高い【確度: 高（事例単位）】

- **最強の事例**: Gabriel Petersson — スウェーデンの高校中退（学位なし・高卒資格なし）、OpenAI Sora チームの research scientist（「博士号保有者が通常担う役職」）。Fortune / AOL / Business Insider / 36kr が独立報道。本人の verbatim: *"Universities don't have, like, a monopoly on foundational knowledge anymore. You can just get any foundational knowledge from ChatGPT"*。具体的な ChatGPT 学習ループ（何を作るか聞く → コード生成 → バグ修正 → 概念が腑に落ちるまで掘る）を一人称で報告
- **個人 blog 事例**（確度: 中）: Medium の『Unmood』事例 — *"I built and shipped a real product within an hour … using nothing but words, vibes, and AI"*。deploy 先 live 確認済みだが、著者の credential 状態が不確実なため層への帰属は medium
- **構造差**: 日本語圏が「非エンジニアの私が初めて作れた」型 personal essay 群なのに対し、英語圏は報道（Petersson）や vibe-coding 言説に寄っている。同型の personal essay 群が英語圏に同等密度で存在するかは未確認（→ Open Questions 3）

## 3. 未観測の生息地候補

- **HN / Reddit**: HN スレッド 3 件が fetch されたが confirmed claims に直接寄与せず。生息有無は open
- **X / Discord**: login 壁のため本調査では観測不能（カバレッジ外）

「未観測」は「不在」ではない。Phase 1 以降の観測で再訪する。

## 4. 自己記述語彙（Phase 1 造語候補生成の入力）【確度: 高（ja）/ 低（en）】

### 日本語圏 — 安定した二層構造

- **支配的アンカー語: 「非エンジニア」** — 複数の独立した著者がタイトル・本文・タグで反復（『【非エンジニア】…』『非エンジニアが AI と歩んだ 1 年半』『非エンジニアである私が』『非エンジニア・工業高校卒』）
- 周辺語彙: 「独学」「駆け出しエンジニア」「ゼロから始めた（側の人間）」「素人」「個人開発者」「文系事務員」「ただの事務員」「独立研究者」「AI アライメント研究者」「個人農家 / 34歳農家」
- **構造**: 職業アンカー（事務員・農家・Web ディレクター・PM）+ **否定形の技術自己記述**（非エンジニア・素人・未経験）の二層。「自分が何者か」を既存職業で、「何者でないか」を技術 credential の否定で語る

### 英語圏 — 流動的・安定アンカーなし

- 観測された語り: "no degree / dropout" / "learned via ChatGPT" / "vibe coding levels the playing field" / "Universities don't have a monopoly on foundational knowledge"
- **棄却された語彙仮説**（3票 adversarial で killed）: 「"builder" が software engineer を置換しつつある」（0-3）、「著者が "vibe coder" を自己記述として採用」（0-3）— en 圏の自己記述語彙はまだ収束していない

### Phase 1 への含意

日本語圏の「非エンジニア」は**否定形**であり、層に固有の**肯定形の名前が空いている**ことを示す。造語はこの空隙に入る。また「credential の否定 + 職業アンカー」の二層構造は、造語が置換すべき語りの形そのものである。

## 5. グリフター境界の観測【確度: 高】

確認された全事例の framing は build narrative / capability-shift narrative（「以前は作れなかったものが今は作れる」「プログラミングが学習から創造に変わる瞬間」）であり、income claim（収益自慢・稼ぎ方の販売）とは**語彙レベルで分離**していた。複数事例で除外フィルタ（monetization / 商品・コース販売 / アフィリエイト）を明示的にチェックし、いずれも通過。doctrine §3 のグリフター排除基準（制作物 narrative か金銭 narrative か）は、実地の観測と整合する判別軸として機能する。

## 6. doctrine への含意

- **§2 実在仮説**: 「その類の人々の存在」は観測で支持。「世界同時多発的な層としての規模」は引き続き仮説（定量未実施）
- **§2 定義の境界 nuance（発見）**: emptybaba（Web ディレクター 20年）/ akinat（PM 10年）は「プログラミング credential」は持たないが「ドメイン credential（職業経験）」は持つ。**「非コーダーのドメイン専門家」という亜種**が層の一部を構成する。doctrine §2 条件 1（制度的 credential を持たない）の解像度を Phase 1 で上げる必要がある — 「どの credential を持たないことが定義的か」
- **「制度級」の語の伸縮**: deploy 済み・認証付き SaaS でも single-org・free-tier・実ユーザー1名・セキュリティ監査なしのケースがあり、修辞的に膨らみがち。defining essay（T1）で「制度級」を使うなら定義を固定すること
- **T1 を Zenn (ja) から出す順序の支持**: 層の生息密度・一人称 essay 文化・自己記述語彙の安定性のすべてで日本語圏が厚い。plan Phase 1 の公開順序（Zenn → Substack）は観測と整合する

## Caveats

1. **母集団 vs 存在**: 全事例 n=1 の存在証明の集積。「高密度」は発見容易性の意味で、定量シェアではない
2. **Source quality の偏り**: ja 圏は primary first-person + 外部アンカーで信頼度高。en 圏は Petersson 以外、credential 状態の確認が弱い
3. **「制度級」の伸縮**: 上記 §6 参照。事例ごとに濃淡がある
4. **credential 定義の境界**: 「非コーダーのドメイン専門家」亜種の存在（§6 参照）
5. **AI による「査読」**: teddy_on_web の preprint は LLM 査読であり human peer review ではない。Zenodo preprint としては正当だが「査読済み論文」と書くのは overstate
6. **時間依存性**: 全 source は 2025-2026 の直近。層は急速に拡大・変容しうる。en 圏語彙は特に流動的
7. **反対論は未解決**: George Hotz の「AI 生成コードは検出困難な低品質 slop」という懐疑論は検証で棄却（0-3 / 1-2）されたが、これは Hotz 主張の検証可能性が低かったためであり、**アーティファクト品質への懐疑自体は未解決の論点**として残る（→ Open Questions 2）
8. **カバレッジ限界**: X / Discord は login 壁で観測不能。HN / Reddit は confirmed claims に未寄与。検索 index は en 中心バイアスの可能性

## Open Questions

1. **層の定量的規模**: Zenn / note / Qiita でこの型の投稿が何件・どの増加率で出ているか（タグ「非エンジニア」「個人開発」× AI ツール名のクロス集計等）。doctrine §2 の規模仮説の検証には別途定量調査が必要
2. **「制度級」度合いの評価**: AI 生成アーティファクトの隠れた品質問題（Hotz 的懐疑）がこの層の成果物にどの程度当てはまるか。持続性（6ヶ月後も live か）の追跡
3. **英語圏の一人称 essay 密度**: ja 圏と同型の「非エンジニアの私が初めて作れた」型 personal essay 群が en 圏に同等密度で存在するか（HN / Reddit / X / Discord の生息有無が open）
4. **語彙の変容方向**: ja「非エンジニア」アンカーと en の流動語彙の差は文化差か時間差か。empowerment narrative の語彙が安定するか、income narrative に吸収されるか

## 検証で棄却された主な claim（誤用防止）

- 「"builder" という肩書きが software engineer を置換しつつある」（sfstandard）— 0-3 で棄却
- 「非技術系社員が Walmart で agent builder 業務を担っている」（sfstandard）— 0-3 で棄却
- 「Hotz: AI 生成コードの低品質は検出困難であり、見かけ上の制度級成果物は幻」— 0-3 で棄却（ただし Caveat 7 参照）
- 「Medium 著者が "vibe coder" を自己記述語彙として採用」— 0-3 で棄却
- 「emptybaba の『世界初』機能実装の主張」— 0-3 で棄却（『世界初』は本人主張のみで検証不能。事例自体の成立には影響しない）

## 全ソース一覧（25 fetched / 確度別主要分）

**Primary（一人称 / 一次確認）**: zenn.dev/ze1ny (CodeSensei) / note.com/mattun3835 / qiita.com/emptybaba (fuSen) / note.com/akinat / note.com/farm_eolica / sg.wantedly.com (竹内) / note.com/teddy_on_web / medium.com/@anujgargbhamma (Unmood)

**Secondary（報道）**: fortune.com (Petersson) / aol.com (Petersson) / sfstandard.com (builder 言説 — 棄却) / decrypt.co (Hotz — 棄却)

**Forum**: news.ycombinator.com ×3 / discuss.huggingface.co (independent researcher endorsement 求む スレッド)

**その他 ja**: zenn.dev/shogaku / zenn.dev/yamato_snow / note.com/saekiryo_ai / note.com/nikorihito2023 / note.com/h_kosu / zenn.dev/mkj

**Contrarian / グリフター境界**: stackoverflow.blog / vocal.media (AI guru hustle culture)
