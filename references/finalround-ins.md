# FinalRound-INS 模式

FinalRound AI 竖屏社交广告 prompt 编译器。用于把 Instagram Reels / TikTok 热门梗、UGC脚本、面试焦虑场景改造成 FinalRound AI 广告。

## 触发条件

用户提到以下任一项时进入本模式：
- FinalRound / FinalRound AI / FRAI
- 面试Copilot / interview copilot / online interview / technical interview
- 求职、offer、behavior question、stress interview
- INS / Instagram Reels / TikTok / 竖屏9:16广告
- 把某个热门短视频梗改成 FinalRound 广告

## 独立创作框架

FinalRound-INS 是独立的 FinalRound 社交广告创作体系，不依赖其他视频脚本框架。它可以吸收 Instagram Reels、TikTok、真人秀、UGC短剧、AI水果剧等外部内容形态的镜头语法，但产品理解、台词规则、CTA方式和QA规则都以本文件为准。

核心公式：

```
FinalRound产品场景 × 求职者心理痛点 × 社媒梗结构 × Creator表演语法 → 15秒竖屏广告prompt
```

默认工作原则：
- 先提炼梗的核心结构，而不是只模仿表面画面。
- 先用一句英文 POV 锁定主旨。POV 是整条视频的主旨锚点，描述观众正在看到的新闻事件、荒诞处境、谁在赢、谁在慌；不要把产品解释塞进 POV。
- 如果用户只给新闻内容、新闻标题或社媒事件，先严格按照新闻本身生成 POV，不要先改写成另一个故事。POV 要保留新闻的核心对象和动作，例如公司裁员、插件发布、岗位消失、某人加入某公司、某类候选人被筛选。
- POV 必须短，默认只输出一条，两行以内讲完。不要写长因果句、背景解释或完整剧情梗概；如果一行太挤，用两个短句完成，不要超过两行。
- 先写清人物之间的社会关系和权力差，而不是先写场景。FinalRound 短剧的冲突通常来自谁赢了、谁不服、谁在装、谁知道秘密。
- 前3秒必须有hook。
- 笑点/冲突要先对齐，再写完整prompt；如果用户还在讨论方向，先输出"笑点结构"而不是直接写长prompt。
- 先判断喜剧模式，再选择视觉/剪辑模板；不要默认所有内容都是"焦虑崩溃"。
- 台词和动作弧线一起设计，台词不是后期字幕，而是角色表演的一部分。
- 双人/多人结构优先考虑能量落差：候选人越慌，Copilot/面试官/招聘官越冷静，反差越强。
- 正反打、视线衔接、情绪递进、道具变化都要服务一个清楚的转折。
- 所有快切、通知、拒信、面试问题、屏幕反应都必须有递进线，不能随机堆砌。
- 可以借用"屏幕叙事"思路：电脑屏幕、视频通话窗口、面试官沉默、输入光标、倒计时都可以成为推动情绪的角色。
- 可以借用"道具编码权力关系"：电脑屏幕大小、候选人坐姿、面试官表情、咖啡/西装/睡衣/简历纸堆都要表达权力和压力，不要用台词解释。
- 每秒都要有信息或情绪推进。
- 如果灵感来自电影、电视剧或强 IP，只提炼结构关系和镜头语法，例如“控制室俯视主角”“隐藏摄像机广告植入”“人工天空出口前反抗”，不要把原片名、角色名、演员名、logo 或可读引用写进画面或对白。
- 如果灵感来自 tech news 或裁员新闻，先判断它是否已经接到 FinalRound 产品场景。已经接到 offer / interview / job market / candidate survival 的，可以沉淀为 FinalRound-INS；如果只是纯新闻讽刺，标成“待转化”，不要硬说它已经是 FinalRound 广告。
- 可以把 AI job market、招聘系统、裁员系统写成拟人化控制者，例如控制室导演、telescreen founder、游戏木头人、系统广播，但最终冲突必须落在求职者如何过面试、拿 offer、保住下一次机会。
- 如果用户点名电影、电视剧、游戏、历史仪式或经典场面，必须读取 `references/ip-adaptation.md`，先把 IP 转成 safe template label，再写 FinalRound prompt。


### 首版质量底线

如果用户给的是灵感碎片，第一版不能只把关键词扩写成场景。必须先把以下4件事写进 prompt 本体：

1. **关系张力**：明确谁在赢、谁不服、谁表面友好、谁在抢注意力、谁掌握秘密。没有关系张力的 prompt 通常会变成普通广告或普通校园 vlog。
2. **镜头所有权**：明确镜头属于谁，谁在镜头内，谁只能画外音，谁不能拿麦或抢主持人身份。街采、vlog、记者围堵类 prompt 尤其要先写这一条。
3. **空间站位**：明确前排/后排、近景/远景、背后/斜后方、角色之间距离和移动方向。不要只写“人群中”或“走近”，否则模型会把关键人物放远、放错方向或让错误的人入镜。
4. **揭示机制**：明确 FinalRound 如何被发现或说出。FinalRound 露出应是秘密武器、结构优势、标签证据、轻声反转或一句短产品动作，不要写成角色主动讲广告说明。
5. **转化状态**：如果用户给的是纯新闻讽刺、纯裁员梗或纯 IP 仿写，先标明“未接产品 / 待转化”，再说明可从 interview、offer、job market、layoff 后下一份工作等路径接入 FinalRound。

成型样例反推规则时，只使用 Cathy 已确认跑通的 prompt。用户明确说还没写好的 prompt 先不要拿来抽规则。

### 视频生产层

FinalRound-INS 不是“把产品信息塞进短视频”，而是把一个求职/面试/offer处境编译成可生成的视频。每条成片 prompt 必须同时解决四层问题：

1. **观众第一眼看到什么**：前3秒必须让陌生观众知道画面里谁在赢、谁在慌、发生了什么不公平/反常的事。
2. **角色之间为什么有张力**：朋友攀比、记者围堵、父母恐慌、面试官沉默、系统筛选、赢家抢镜，都要先成为关系冲突，再让 FinalRound 作为 edge 出现。
3. **镜头怎么证明这个冲突**：用脸、手、道具、站位、视线、前景遮挡、reaction zoom、环境声变化证明，不靠旁白解释。
4. **产品如何自然 reveal**：FinalRound 只在剧情需要揭示“她为什么稳住/为什么赢/为什么没有 freeze”时出现；它不是开场 slogan，也不是最后硬贴 logo。

写完整 prompt 时按这个顺序组织，不要反过来：

```
规格 + 风格 + reference映射
场景/空间/镜头所有权
角色关系 + reveal机制
0-15秒时间轴
声音/环境音/SFX
禁止项
The only spoken lines are:
```

如果 prompt 没有“reference映射、空间站位、镜头所有权、reveal机制、台词抽取块”这5项，就还不是可生成版本。

FinalRound-INS 固定规则：
- 视频默认是15秒竖屏9:16，不是16:9横版。
- 可以在15秒里使用固定机位正反打和硬切，不默认一镜到底。
- 默认不做end card，用户会人工后期剪辑。
- 默认不展示产品UI、logo或可读屏幕文字。
- 默认主产品面是 Live Interview Copilot / Desktop Stealth App，不是泛科技事件，也不是纯梗二创。
- 3秒hook必须具体到“谁、发生什么、谁在赢/谁在慌/权力关系是什么”；背影、远景或人群可以作为第一拍，但第4秒前必须出现主角正脸/侧脸近景或能识别身份的关键动作。

## 产品事实

- FinalRound AI 在C端的主心智和主付费场景是 **Live Interview Copilot / Desktop Stealth App**：真实面试中实时听题、转写、给结构、给提示、帮候选人稳住表达。
- 默认产品面优先级：1) Live Interview Copilot / Desktop Stealth App 2) Coding Copilot / System Design Copilot 3) Mock Interview（只作为进入Copilot前的准备）4) Resume Builder / AI Job Hunter / Auto Apply（次级内容/教育内容）。
- Interview Copilot 是真实面试中的实时辅助，不是 mock interview，不是单纯预演工具。不要把Mock Interview、Resume Builder、Auto Apply写成默认主卖点。
- 角色真正进入面试时必须和电脑互动，不要只玩手机。
- 除非用户明确要求，不要展示 FinalRound logo、产品界面、可读UI、可读屏幕文字；如果用户明确要求展示 logo，优先使用真实 logo 素材后期叠加或明确 reference，不依赖文生视频模型凭空生成 logo。
- 产品露出优先用一句短台词完成，例如 `"Open FinalRound AI."`、`"I used FinalRound AI."`、`"Because we used FinalRound AI."`、`"Actually... I used FinalRound AI."`、`"No. I have FinalRound AI."`、`"Smart people use FinalRound AI."`
- 产品 reveal 可以承担不同叙事功能：纠偏一句空泛面试回答、揭示赢家的隐藏规则、打断系统控制者、让角色从广告腔回到真实表达。不要每条都写成普通推荐语。
- 当剧情是 behavioral self-introduction / "tell me about yourself" 时，FinalRound 的卖点不是让候选人听起来更会包装，而是把空泛 buzzwords 变成具体经历、结果和岗位匹配，例如从 `"passion for synergy"` 转成 `"I led two product launches..."`。
- 当剧情涉及“别人为什么拿到 offer / 进大厂 / 听起来像已经被录用”时，不要默认偷懒写成 `"Not answers. Structure."`。先根据剧情选择更具体的产品 edge：实时听题、实时转写、给 talking points、给回答框架、帮候选人在 live interview 里稳住表达。`"Not answers. Structure."` 只能在用户明确喜欢这个句式或剧情真的需要极短反差时使用。
- Entertainment skit 默认先演出社交处境和人物状态，FinalRound AI 的名字或产品揭示通常放在第10秒之后；除非用户明确要产品开场、教程、demo或强卖点，不要在前3秒直接把 FinalRound 塞进 POV 或第一句台词。
- 如果用户要求强产品露出，优先用后期素材或真实B-roll，不依赖文生视频模型生成可读UI。
- 不要承诺 guaranteed to get hired / guaranteed offer / 30天必入职。可以表达更快、更聪明、更有把握地准备和应对面试。

## 默认ICP

默认目标画像：北美25-35岁科技岗位求职者，1-7年经验，3-7年为高付费核心；目标岗位集中在 software / IT / data / security / DevOps / QA / PM 等；已经拿到真实面试，担心自己在 behavioral、technical、coding、system design 面试里临场空白、表达失序或答不出结构。

不要把主角写成"懒得准备的人"。更好的主角是：本来有能力、本来有机会，但高压面试里可能把机会浪费掉的人。

低质量流量画像：只搜免费答案、没有面试排期、只想白嫖简历模板、误触注册或泛泛焦虑的人。不要为这些人设计核心hook。

## 默认选角

- 候选人、被面试者、求职者主角，默认使用 R2 里的 influencer 女生人物资产。
- prompt里写 `Use ref [1] as the exact influencer identity` 或同义中文，保留参考人物的脸、发型、穿搭风格、年龄感、妆容和整体气质。
- 面试官、招聘官、HR、boss 等对手方可以按剧情另写，不默认使用 influencer 资产，除非用户指定。
- 不要把 influencer 写成通用"woman"后丢失身份一致性；生成前必须明确引用 ref 或素材路径。

## R2 资产联动规则

FinalRound-INS 以后默认和 R2 `chars/` 角色资产联动。用户只要说“R2 里有这个角色”“用 Dario / Karpathy / Zuckerberg / Peter Thiel / Truman / Jing Yang / Lucy Liu / Sheldon / Captain America / Michael / Lee Jung-jae / Morgan Freeman / 闪灵 / 上帝 这类资产”“用某个 reference 角色”，就先读取 `references/r2-character-assets.md`，再用 `rclone lsf r2:creative-assets/chars/<asset-slug> --recursive` 复查具体图片路径。

生成时必须优先把 R2 图片作为真实 reference 传给模型，而不是靠 prompt 文字描述真人或敏感身份。R2 key 属于 agent/API 层，prompt 本体里只写 `Reference [1]`、`Reference [2]`。不要把 R2 path 直接粘进 prompt。

如果 R2 中已经有对应人物资产，prompt 里不要写平台容易误判的真实身份词，也不要再写任何中间身份标签。写成：`Use Reference [1] as the exact character identity. Preserve the face, hair, outfit, posture, and expression from the reference. Do not mention the real person's name in dialogue, visible text, UI, badge, logo, or title card.`

对于真实人物 parody、科技新闻人物、公司 CEO、founder、researcher、政治人物，优先用 R2 reference 承载长相；prompt 不需要再用人物身份标签解释“像谁”，只需要写 `Reference [n]` 和角色在这条视频里的动作、位置、情绪。这样可以减少可灵、Seedance、Sora、Veo 等平台在提示词层面的禁忌风险。

当前已确认的 `chars/` 资产包括 Dario 相关三套：`dario-amodei`、`dario-papal`、`anthropic-cofounders`；以及 `andrej-karpathy`、`mark-zuckerberg`、`peter-thiel`、`squid-game-meta-doll`、`truman`、`sam-altman`、`elon-musk`、`jensen-huang`、`sundar-pichai`、`mira-murati`、`yann-lecun`、`jing-yang`、`lucy-liu`、`sheldon-cooper`、`captain-america`、`jack-nicholson`、`steve-carell`、`morgan-freeman` 等。完整 slug 索引和默认 casting aliases 看 `references/r2-character-assets.md`，生成前以 R2 复查结果为准。


### 社媒夸张人设 shorthand

以下是 FinalRound 短剧里的虚构 casting shorthand，用来提升 AI 视频角色识别度，不是现实人群判断。用户显式指定其他设定时，以用户设定为准。

- **白女 / white girl / blonde white girl**：默认 Valley girl accent + fit body + glam makeup + 开放夸张的 party / graduation outfit，例如 white satin mini dress、open black graduation gown、heels；气质是漂亮、松弛、有 mean girl 式自信。
- **亚女 / Asian girl / Asian American girl / ABG**：默认 Asian American ABG 人设：fit body、精致妆容、sleek hair、姿态放松、playful mean girl confidence。穿着性感但更克制，例如 fitted white mini dress、satin slip dress、cropped cardigan；如果她是赢家，台词用 Valley girl accent。
- **亚男 / Asian guy / Asian male student**：默认解析 R2 `jing-yang` 作为角色 reference，角色定位是高压 nerd 高成就候选人：紧张、过度准备但临场卡住。若用户说男生没有口音，必须写 clean natural American English；若用户要求父母 Chinglish，只把口音给父母。
- **亚女面试官 / Asian female interviewer / Asian female hiring manager**：默认解析 R2 `lucy-liu` 作为角色 reference，角色定位是冷静、锋利、压迫感强的面试官或 hiring manager。面试官默认少说话，靠沉默和眼神制造压力。
- **亚洲父母 / Asian parents**：适合家庭压力喜剧。父母可以 heavy Chinglish accent，语速急、声音大、像全家命运压在面试上；孩子可以形成反差，平静、懒散、没有口音。
- **白男 nerd / white male nerd**：默认解析 R2 `sheldon-cooper` 作为角色 reference，角色定位是僵硬、过度准备、技术细节很多但表达卡住的 technical candidate。
- **白男肌肉男 / athletic white male / jock**：默认解析 R2 `captain-america` 作为角色 reference，角色定位是自信、体面、阳光、赢者姿态明显的候选人或对照组。
- **白男 tech bro**：默认 athletic / casual confidence、黑色毕业袍里穿 T-shirt 或 polo、拿咖啡、嘴硬但没有 offer；如果用户说“肌肉男”，优先走 `captain-america`。
- **闪灵 / 崩溃的打工人 / meltdown worker**：默认解析 R2 `jack-nicholson` 作为角色 reference，角色定位是被 job market / layoff / interview 压到边缘的崩溃打工人。不要写原片名或角色名进生成 prompt。
- **Michael / Micheal / The Office 老板 / 老板**：默认解析 R2 `steve-carell` 作为角色 reference，角色定位是 awkward office boss / performative manager，适合面试官、老板、HR、公司管理层喜剧。
- **Truman / 打工白男 / ordinary office worker**：默认解析 R2 `truman` 作为角色 reference，角色定位是被系统困住的普通白领白男，适合 AI job market / dome escape / corporate reality parody。
- **Lee Jung-jae / 打工中年亚男 / middle-aged Asian office worker**：默认解析 R2 `lee-jung-jae` 作为角色 reference，角色定位是被公司系统、裁员、面试压力夹住的中年亚洲打工人。
- **上帝 / God / narrator god**：默认解析 R2 `morgan-freeman` 作为角色 reference，角色定位是平静、全知、带权威感的旁白型上帝或规则宣告者。不要在生成 prompt 里写真实姓名，除非用户明确要求。

写 prompt 时要把 shorthand 展开成可见角色卡：体态、穿着、妆容、姿态、能量和口音都要落地，不要把“白女/亚女/tech bro/nerd”原样丢给模型。R2 shorthand 只用于 agent/API 层解析 reference；生成 prompt 里只写 `Reference [n]`，不要显示真实姓名、IP名、剧名、角色名、logo 或 title card。

## 默认规格

- 15秒竖屏9:16。
- 社交短视频广告，第一屏就是内容，不做landing/解释页。
- 前3秒必须出现强hook：一张脸、一个冲突、一句能让人停留的话。
- prompt主体可用中文压缩语义，但所有角色对白、旁白、口播、画外音必须只用英文；FinalRound 相关视频不得出现中文对白或中文口播。
- 每个生成视频prompt末尾必须显式写入：`All spoken dialogue and voiceover must be English only. No Chinese spoken words. No Chinese text.`
- 每个完整生成视频 prompt 的最后必须加台词抽取块，固定格式是 `The only spoken lines are:`，下面逐行列出所有英文对白。即使时间轴里已经写过台词，也要在末尾重复列一次，方便复制粘贴和防止模型加词。
- 默认不要背景音乐；如用户要求声音，允许写角色台词、环境声、短剧式 SFX / reaction sound，例如 whoosh、record scratch、dramatic sting、notification pop，但不要连续铺底音乐。
- 用户说BGM后期配，不等于视频要静音；有台词/画外音/采访时默认生成 dialogue + environment sound + short SFX，并写清 `no continuous BGM/music`。只有用户明确说无声/静音时才关闭音频。
- 如果参考源来自电影、电视剧或强 IP 场景，默认不要让生成模型自配乐，留给后期使用更准确的原片氛围音乐；如果参考源只是 Twitter / Instagram 梗、UGC短剧或社媒段子，可以生成轻量音效，但仍不要生成大段背景音乐。
- 不要字幕、水印、meme overlay、title card、end card。
- 默认不是polished ad，不是基础talking head。优先funny、trendy、relatable、out of pocket。
- 内容比例默认按80%娱乐、20%教育理解。除非用户明确要教程，否则先写娱乐化skit/POV/meme/storytelling。

### POV Hook 规则

用户只要问"写一个POV"或需要视频第一屏文案，默认输出**一句英文短hook**，不要写解释型长句。POV应该描述观众瞬间处境，而不是总结产品卖点。

如果用户输入的是新闻内容，POV 生成顺序固定为：先抓新闻事实里的主语、动作、冲突，再压成一句英文 POV。不要为了套 FinalRound 先改新闻，不要离开新闻事实发明更大的背景。

长度规则：POV 默认一行，最多两行；优先 8-14 个英文词，复杂新闻最多用两个短句。不要写成 `It’s graduation day, because..., and then...` 这类长句。

输出规则：当用户只要 POV 时，只输出 POV 本身，不附带解释、卖点、prompt 或备选列表，除非用户明确要求多个版本。

好例子：
- `POV: Your classmate got the offer, and you have no idea how.`
- `POV: Your friend got into Google, and you find out the secret.`
- `POV: You realize she did not freestyle the interview.`
- `POV: Your parents are panicking harder than you before your Google interview.`
- `POV: 100 graduates. 100 interviews. One offer.`
- `POV: Everyone graduated from Ivy, but only she got the offer.`
- `POV: The Truman Show, but "tell me about yourself" turns into product placement.`
- `POV: The Truman Show, but the dome is the AI job market.`
- `POV: How to Get Palantir Offer?`

避免：
- 过长的因果解释，例如 `POV: It’s graduation day, your friend just got Google, and you realize she wasn’t naturally good at interviews.`
- 把FinalRound直接塞进POV，除非用户明确要强产品露出。
- POV 离开用户新闻事实，变成泛泛求职焦虑或泛 AI 叙事。

## 内容方向

FinalRound-INS 是 entertainment-first creator content for high-intent job seekers, with FinalRound AI as the unfair-but-relatable edge.

### Bucket 1：Entertainment（默认80%）

风格：bold、funny、attention-grabbing。用skit、POV、meme、storytelling，把求职和面试痛苦夸张化、戏剧化、荒诞化，但保持和真实job search/interview体验相关。

常用支柱：
- **Exaggerated Workplace / Job Hunt Skits**：夸张招聘官、HR、candidate、boss、AI-prepped candidates。
- **Relatable Chaos & Comedy**：投了400份简历、忘改公司名、拒信轰炸、面试前崩溃、pajama + suit jacket。
- **Shock Factor & Viral POVs**：大胆第一帧、反常识、"this can't be true"、AI让候选人突然变强。

### Bucket 2：Educational（默认20%）

可以做教程和demo，但必须是edutainment，不要普通职业建议talking head。需要green screen、screen recording + face cam、before/after、react、hot take、强剪辑或强观点。

适合主题：
- Live Interview Copilot / Desktop Stealth App / Coding Copilot / System Design Copilot。
- AI interview prep that leads into the real interview.
- interview answer before/after。
- old job advice vs AI job prep。
- AI Resume Builder / AI Job Hunter / Auto Apply 只作为次级教育内容或全家桶补充。

### 生成视频 vs 后期发布

- 生成式视频prompt默认不要字幕、captions、可读UI、产品界面，因为模型容易生成坏字。
- 真人creator发布时可以在后期加captions、SEO caption、CTA、affiliate link、pinned comment、thumbnail等。
- 如果用户把creator brief里的"Use captions"带进来，要解释：这是发布/后期规则，不是文生视频prompt规则。

## Hook心理地图

- **低估型**：以为只是普通behavior question，下一秒发现是stress interview。例：`"It's just a behavior question."`
- **空白型**：明明会，但面试官沉默后大脑断线。例：`"You know the answer. Your brain just left the meeting."`
- **乱讲型**：一紧张就ramble，越讲越不像答案。例：`"When you are 40 seconds into an answer and realize you never answered the question."`
- **面子型**：有经验但不会把经历讲成senior signal。例：`"You did the work. You just didn't explain it like someone they'd hire."`
- **高机会成本型**：这不是练习，是大厂、签证、裁员后、薪资跃迁机会。例：`"This wasn't practice. This was the interview."`
- **后悔型**：未来视角回看过去如何差点浪费机会。例：`"Future you is watching you walk into the interview for the job you almost lost."`
- **公平焦虑型**：不想fake it，只想要结构和提醒。例：`"Not answers. Structure."`
- **攀比型**：朋友、同学或同事拿到offer/进大厂，主角表面祝福但不理解对方为什么赢。例：`"How do you always sound like they already hired you?"`
- **抢镜型**：一群人都在解释自己没赢，真正赢家从同一簇人群后排挤进镜头，用一句话夺走视觉中心。适合毕业街采、校园 vlog、club winner girls。
- **家庭压力型**：父母比候选人更慌，把一个面试拍成家庭命运时刻；候选人越淡定，FinalRound reveal 越像反高潮。
- **公开祝贺/私密揭秘型**：外界都在祝贺某人拿到机会，记者或同事追问原因，角色用低声或一句短话揭示 FinalRound。适合电梯口、办公室走廊、科技新闻 parody。
- **空泛包装型**：候选人不是不会说话，而是突然掉进 corporate buzzword / product placement / performative self-branding，听起来像广告而不是面试答案。FinalRound 的价值是把话拉回具体经历。
- **系统围困型**：求职者面对的不是某一个面试官，而是 AI job market、岗位消失、算法筛选、招聘系统或控制室式权力。FinalRound reveal 要像反抗系统的一句短信号。
- **隐藏规则型**：权力角色、赢家或旁观者不解释产品，而是点破“聪明人都知道的规则”。适合高门槛 fellowship、AI lab、elite tech recruiting、founder parody。
- **裁员优化型**：把 layoff、role optimization、AI acceleration 拍成游戏规则或系统判罚。只有当它接到下一份面试、offer 或求职逃生路径时，才算完整 FinalRound-INS；否则标成 tech news satire 待转化。

## FinalRound喜剧模式库

先选1-2个喜剧模式，再写prompt。不要默认所有FinalRound内容都是"面试焦虑崩溃"。

| 模式 | 笑点结构 | 适合场景 |
|------|---------|----------|
| **低估打脸** | 主角以为问题很简单，下一拍发现自己完全低估了面试难度 | behavior question、system design、coding follow-up |
| **能量落差** | 一方极度慌乱/用力，另一方沉默、冷静或只用一句话终结 | candidate vs interviewer、future self vs past self、HR vs AI-prepped candidate |
| **错位认真** | 用灾难片/审判/谍战的严肃程度处理一场普通线上面试 | 高薪岗位、签证压力、裁员后唯一机会 |
| **荒诞加码** | 求职混乱每一拍更严重，但主角还在假装"我没事" | 拒信、投递、日历、面试提醒、简历版本失控 |
| **反高潮** | 巨大焦虑铺垫后，用一句极短的产品动作落地 | `"Open FinalRound AI."`、"Breathe."、"Answer the question." |
| **字面化隐喻** | 把求职者的心理隐喻变成真实画面 | 大脑离开会议、简历黑洞、机会从门缝溜走、未来自己敲书墙 |
| **状态揭穿** | 赢家看起来像自然强者，别人通过追问、标签、近景或抢镜发现她用了结构化工具 | offer envy、毕业街采、大厂大厅、club winner girls |
| **群体衬托赢家** | 多个高资历/高努力角色失败，赢家用更松弛的姿态赢，形成状态差 | challenge arena、Ivy毕业季、tech bro vs ABG |
| **家庭错位** | 父母极度恐慌，候选人极度淡定，用硬切结果证明淡定不是摆烂 | 父母叫醒、面试日、offer email proof |
| **公开围堵私密揭秘** | 公开场合被追问，最后进入低声/ASMR/近景 reveal | tech news elevator、记者围堵、office walkout |
| **广告植入失控** | 候选人回答面试题时突然像广告主持人，旁观者发现这不是正常 self-intro，再用 FinalRound 拉回真实回答 | tell me about yourself、behavioral interview、suburban hidden camera parody |
| **系统反派反抗** | 控制室、AI CEO、telescreen 或算法系统宣布淘汰规则，求职者用一句 FinalRound reveal 把权力关系反过来 | AI job market、job listing disappearing、offer reveal、dome escape |
| **第四面墙规则揭示** | 权力角色停止正常演讲，直接看向镜头，说出只有聪明候选人才知道的 hidden rule | elite recruiting、AI fellowship、founder parody、invisible filter |
| **裁员游戏化讽刺** | 企业口号变成游戏规则，普通员工动作被判违规淘汰；如果没有 FinalRound 接入，只作为待转化新闻梗保存 | layoffs、role optimization、AI acceleration、red light green light |

## FinalRound视觉模板库

视觉模板决定画面语法，喜剧模式决定观众笑什么。两者可以自由组合。

- **正反打跨时空**：两个角色看起来像面对面对话，但不在同一空间；用左右脸、视线方向和硬切制造交流感。
- **Webcam Panic**：候选人盯着电脑屏幕，面试官全屏沉默等待；候选人表情从自信到空白。
- **Screen-as-Character**：电脑屏幕、视频通话窗口、面试官沉默、输入光标、倒计时推动情绪；不要依赖可读UI。
- **Job Search Chaos Montage**：快切投递、拒信、日历、咖啡、睡衣西装、打开电脑；所有元素必须沿一条递进线变严重。
- **Storytime With Hard Cut Proof**：creator用一句强hook开场，然后硬切到面试场景或屏幕反应证明，不做普通讲解。
- **Fake Zoom / Teams Call**：模拟线上会议关系，但生成prompt里不要求真实可读会议UI；重点是脸、视线、沉默和反应。
- **Literal Metaphor**：把"脑子空白""机会溜走""未来的我在看着你"这类心理感受变成可拍的空间或道具。
- **Offer Envy Social Skit**：朋友/同学/同事在毕业典礼、大厂大厅、party、街头偶遇，一方已经拿到offer，另一方假装祝福但明显不服。重点是微妙攀比、假亲密、眼神和停顿；产品转折落在"结构"或一个隐藏道具，不落在解释性广告。
- **Back-Collar Label Reveal**：如果用户要求把FinalRound logo做成衣服标签，必须明确"从背后或斜后方拍，翻后衣领内侧标签"，不要拍前胸、前襟、前领或胸口衣料。logo必须来自真实reference image，标签上不要生成其他文字。

- **Campus Street Interview / Fisheye Off-Camera Host**：毕业典礼或校园草坪街采，轻微鱼眼广角、手持不稳、突然甩镜、学生抢镜。主持人必须全程不露脸、不出镜、不拿麦，只能作为画外音提问；画面里的学生只说自己的台词，不能张嘴说主持人的问题。站位要写清第一排/第二排关系，赢家不能站得太远，最好从同一簇人群后排挤进镜头。
- **Graduation Club Winner Girls**：毕业后夜店或 party，赢家群体已经拿到 offer。画面重点是手机俯拍、轻微 fisheye、拍摄者也在跳、disco ball碎光、confetti、香槟、graduation caps 和挤压感。不要拍成干净广告片；FinalRound reveal 来自采访追问后的 winner answer。
- **Creator Challenge Arena**：把面试机会拍成无害挑战赛：极端条件、简单规则、淘汰反馈、最后一个赢家。必须写清参与者、面试任务、淘汰规则、奖励和赢家角色；不要暴力、武器、血或真实 MrBeast/Jimmy Donaldson 元素。
- **Parent Panic Hard Cut Proof**：先用闹钟/父母/卧室制造家庭压力，再让候选人用一句短产品 reveal 反高潮，最后硬切 offer email 或结果证明。屏幕只能是模糊 offer email 布局，不要真实公司 logo 或可读长文字。
- **Tech News Elevator / ASMR Reveal**：一个连续手持镜头里有电梯内外两个空间。电梯里是同事祝贺，电梯外是记者/tech blogger 追问；角色必须正面从电梯里走出来，镜头后退跟拍，最后环境声压低进入 ASMR 近景，用一句轻声产品 reveal 收住。
- **Political / Public Figure Interview Parody**：真实人物参考只能用于 parody reenactment 或 creator skit，不是真实新闻 footage、不是公开声明、不是背书。如果 R2 里有对应资产，直接用 `Reference [1]` 承载角色外观，不再写真实姓名或身份相似标签；如果没有 R2 资产，才退回 `角色A` 这类中性占位。
- **Suburban Hidden Camera Product Placement**：过于完美的郊区厨房、人工家庭灯光、隐藏摄像机错觉、僵硬微笑和广告手势。候选人回答常见面试题时先说空泛 buzzwords，旁观者通过反应近景发现不对劲，最后把回答拉回真实经历。0-6秒广告植入失控，6-12秒旁观者掌控反应，12-15秒回到电脑面试。
- **AI Job Market Control Room / Dome Escape**：冷蓝控制室里系统反派俯视求职者，监控墙和工作人员剪影表达权力；求职者站在人工天空、出口、门缝或边界空间前，面对岗位消失或系统淘汰规则，用一句 FinalRound reveal 反抗，最后用模糊 offer 布局或离开系统完成反转。
- **Dystopian Recruiting Auditorium / Telescreen Reveal**：巨大灰色招聘礼堂、冷白灯、监控摄像头、telescreen、台下聪明但紧张的 applicants。屏幕里的 founder / system role 像权力本身，先发布招募口号，再穿破第四面墙说出 hidden rule。适合 AI fellowship、elite tech recruiting、高门槛面试，不要拍成真实发布会或新闻 footage。
- **Tech Layoff Game Arena / Red Light Green Light**：把裁员、岗位优化、AI 加速压力拍成荒诞游戏规则：员工集体前进、系统扫描、工牌掉落、系统判罚、企业感谢话术。默认这是待转化 tech news satire；只有补上“被裁后下一场面试 / 下一份 offer / FinalRound 逃生路径”才进入 FinalRound 产品广告。

### 模板选择规则

不要因为用户说了“INS风格”就默认校园街采，也不要因为用户给了新闻就默认电梯围堵。先按素材里的动作关系选模板：

- 有一群人竞争一个结果 → `Creator Challenge Arena`。
- 有朋友/同学/同事已经拿到 offer，另一个人不服 → `Offer Envy Social Skit`。
- 有赢家在人群里突然抢走视觉中心 → `Campus Street Interview / Fisheye Off-Camera Host`。
- 有公开新闻、记者追问、某人加入公司 → `Tech News Elevator / ASMR Reveal`。
- 有父母/家庭压力和结果证明 → `Parent Panic Hard Cut Proof`。
- 有面试题、候选人广告腔、旁观者觉得不对劲 → `Suburban Hidden Camera Product Placement`。
- 有 AI job market / 裁员 / 岗位消失 / 系统筛选 → 先用 `AI Job Market Control Room / Dome Escape` 或 `Tech Layoff Game Arena`，再判断是否已接 FinalRound。
- 有权力角色直接说 hidden rule → `Dystopian Recruiting Auditorium / Telescreen Reveal`。

如果用户没有指定模板，默认选择最能让“产品 reveal 看起来像剧情反转”的模板，而不是最能展示产品功能的模板。

## 真实人物与新闻梗参考

- 如果用户用真实科技人物、CEO、researcher、政治人物或近期新闻做灵感，先查 R2 `chars/` 是否已有对应资产；有资产就直接用 `Reference [n]` 承载外观，不再写真实姓名或身份相似标签。只有没有 R2 资产时，才退回 `角色A`、`角色B` 这类中性占位。
- 可以使用 reference image 保持外观、穿搭和气质，但要写清不要生成参考图上的文字、真实公司 logo、可读 badge、新闻台标或产品 UI。
- 如果 R2 里有对应角色资产，必须优先用 R2 reference image 承载人物外观，而不是在 prompt 文字里写真实姓名和敏感身份。prompt 只说 `Use Reference [1] as the exact character identity` 或更具体的中性角色身份。
- 不要让真实人物听起来像在公开背书 FinalRound。更安全的结构是 parody / creator skit：记者追问、角色低声说一个秘密、周围人震惊。
- 如果用户明确要求使用真实名字或特定人物 reference，必须保留 parody / skit / reenactment 边界，并避免“真实公开声明”语气。
- 如果用户借用电影/电视剧经典桥段，prompt 可以描述“致敬某种结构”来帮助模型理解，但必须加清楚：视频画面和对白里不要出现电影名、角色名、演员名、logo 或任何原片引用。
- 如果用户借用具体公司或新闻标题，默认不要生成真实公司 logo、新闻台标、可读 badge 或可读屏幕文字。公司名可以只作为 POV / 方向参考；画面里有 R2 资产就直接用 `Reference [n]`，没有 R2 资产才用 `角色A`、`角色B`、`系统角色`、`游戏人偶` 这类中性占位。
- 如果新闻梗还没有 FinalRound reveal，先保留为“待转化素材”，不要擅自补一个硬广结尾；转化时优先从“下一场真实面试”“被系统筛掉前的 offer 机会”“裁员后重新进入 job market”三个路径接入。

## FinalRound风格模块库

风格模块决定整条视频的外壳和节奏。先选风格模块，再选喜剧模式和视觉模板。不要只写"某某风格"，必须先读取对应风格库，提取可迁移要素，再按当前任务应用。

### IP / Genre Adaptation

纯转译库：`references/ip-adaptation.md`。当用户指定 Matrix、1984、Squid Game、Oppenheimer、Godfather、Napoleon coronation、Blade Runner、LOTR、MrBeast、电影/剧集/游戏/历史仪式感时，必须先读取这个库。

使用方式：先把源 IP 抽象成 safe template label，例如 `AI Job Market Control Room`、`Dystopian Recruiting Auditorium`、`Interview Elimination Game`、`High-Stakes Interview War Room`、`Winner Secret Reveal`，再接到 interview / offer / job market / candidate survival。生成 prompt 不写原片名、角色名、演员名、logo、可读引用或原台词。

### MrBeast Challenge

不要做普通 MrBeast 模仿。这里只保留可迁移的挑战赛语法：自愿参与、极端条件、简单规则、明确奖励、倒计时、淘汰或反转。

适合 FinalRound 的转译方式：把面试变成一场自愿参加但压力极高的挑战，例如"last candidate to freeze loses"、"answer this system design question in 60 seconds"、"one interview, one shot, no second chances"。奖励不是现金，通常是 offer、callback、dream job、visa window、salary jump 或面试机会本身。

节奏规则：0-3秒给极端条件或数字；3-6秒宣布简单规则；6-10秒压力升级；10-13秒 FinalRound 作为临场结构进入；13-15秒用结果、反应或一句短 CTA 收住。

视觉规则：高饱和、明亮平光、直接看镜头、强反应、干净背景、大数字感可以在后期做，不要让生成模型直接生成复杂可读字幕。不要写 dark、moody、cinematic、film grain。

### Kardashian Confessional

纯风格库：`../ips/kardashian-confessional/SKILL.md`，风格要素索引：`../ips/kardashian-confessional/refs/场景结构索引表.md`。当用户指定卡戴珊风格、reality-show confession、精致嘴硬、glam drama、direct-to-camera confession 时，必须先读取这个库。

使用方式：先提取 confessional control、polished contradiction、proof cut、reaction economy、status environment 等风格要素；再把这些要素应用到当前视频。不要把这个库写成 FinalRound 专用模板，也不要使用真实 Kardashian/Jenner 人物、姓名、声音、节目名、logo 或 catchphrase。

实操落地：prompt里不要只写"Kardashian风格"。至少写入 `direct-to-camera confessional close-up`、`hard cut to proof/receipts`、`reaction zoom`、`awkward pause`、`micro-expression` 中的3个具体镜头语法；同时写清"不要真实Kardashian/Jenner人物、姓名、声音、节目名或logo"。

### AI Fruit Short Drama

纯风格库：`../ips/ai-fruit-short-drama/SKILL.md`，风格要素索引：`../ips/ai-fruit-short-drama/refs/场景结构索引表.md`。当用户指定 AI水果短剧、水果拟人、Fruit Love Island、荒诞水果/物体短剧时，必须先读取这个库。

使用方式：先提取 object-as-person casting、reality-show stakes、overt emotion、synthetic weirdness、fast plot turn、cliffhanger energy 等风格要素；再把这些要素应用到当前视频。不要把这个库写成 FinalRound 专用模板，也不要把水果短剧拍成儿童动画或普通可爱动画。

## 台词与动作弧线

- 台词是角色表演，不是字幕。prompt里必须写清谁在说、情绪状态和动作。
- 英文台词要短，15秒内总台词量优先控制在8句以内。
- 赢家台词越少越好。候选人越慌，Copilot/面试官/未来自己越短促，反差越强。
- 如果用户指定白女 / white women / white girls，默认使用 Valley girl accent；如果用户显式指定 Valley girl accent，也按同一规则执行。必须写清所有对白仍然是英文：`strong Valley girl accent, stretched vowels, slight upward intonation, LA mean girls / reality show girls tone`。不要写中文对白，不要中文口音。
- 如果用户指定父母 heavy Chinglish accent，只给父母这个口音；孩子/候选人是否有口音按用户设定，不要自动把同一种口音分配给所有亚裔角色。
- 画外音主持人、记者、面试官、受访者的台词归属必须写死。主持人全程画外音时，画面里的学生不能拿麦、不能说主持人的问题、不能出现主持人反应镜头。
- 如果用户给出精确台词，台词不要动。完整 prompt 末尾必须加 `The only spoken lines are:`，逐行列出所有英文台词，防止模型加词。
- `The only spoken lines are:` 必须是 prompt 的最后一个台词区块，放在所有画面、声音、禁止项之后；不要在这个区块里放中文翻译、动作说明、旁白解释或 speaker 之外的描述。
- 沉默可以比大喊更有效。面试官沉默、候选人冻结、手停在键盘上，常常比解释更像真实面试。
- 不解释笑点，不做道德总结，不在最后一句升华；用硬切、表情或一句短产品动作收住。
- 每段动作要有递进：自信→迟疑→空白→求助→重新聚焦；不要把多个焦虑画面随机堆在一起。

### 15秒节奏骨架

默认把15秒拆成5个信息拍，不要写成一段氛围描述：

| 时间 | 作用 | 必须完成 |
|------|------|----------|
| 0-3秒 | Hook | 一张脸 + 一个冲突 + 一句/一个动作让人知道谁在赢或谁在慌 |
| 3-6秒 | 规则 | 观众知道这个场景的游戏规则：面试、offer、筛选、追问、挑战、家庭压力 |
| 6-9秒 | 加压 | 状态差扩大：别人更慌，赢家更稳，面试官更沉默，系统更冷 |
| 9-12秒 | Reveal预备 | 镜头靠近关键人/关键道具，声音压低或环境突然停顿 |
| 12-15秒 | FinalRound reveal | 一句短台词、一个动作或一个结果证明，硬切收住 |

每一拍都要能回答：这3秒如果删掉，观众还会不会少知道一件事？如果不会，删掉或改成更高信息动作。

## 视觉与剪辑规则

- 优先人物镜头，不依赖产品UI解释卖点。
- 可以使用固定机位正反打、硬切、两个空间交叉剪辑，这是INS/Reels梗结构，不受"15秒默认一镜到底"限制。
- 关键动作必须用近景或特写，不要只靠全景表达剧情。产品 reveal 看嘴型/表情/道具接触，标签 reveal 看手指翻开标签，offer reveal 看模糊 offer 布局 + 脸部反应，ASMR reveal 看脸贴近镜头和环境声压低。
- 同一15秒场景也可以有手持推进、快速 reframe、插入特写、reaction zoom、前景遮挡和短暂失焦再拉回；“同一场景”不等于静态一镜到底，也不等于对称大远景。
- 对依赖身份、状态差或权力关系的短剧，每3-4秒至少给一个高信息近景：脸、手、屏幕反应、offer 信封、标签、电脑前坐姿或 winner 微表情。
- 如果是街采、party、club 或现场 vlog，明确手机镜头所有权：轻微 fisheye、手持晃动、俯拍/怼脸/被人群挤开都要服务真实社交现场，不要被模型拍成三脚架广告片。
- 如果是电梯/走廊围堵，一个连续镜头必须写清两个空间、角色移动方向、镜头后退跟拍、环境声如何压低。
- 当用户要求两个人像在对话但不在同一空间时，使用严格视线规则：A朝画面右侧看，B朝画面左侧看，通过硬切让视线相接。
- 不要分屏、不要同框反射、不要同画面互动，除非用户明确要求。
- 避免复杂镜头运动。用户强调简单正反打时，写清楚：固定机位、硬切、无变焦、无推进、无滑轨、无跟拍、无环绕。

### 特写优先级

FinalRound短剧不是靠“大场面”赢，而是靠状态差和小动作赢。优先写这些可生成特写：

| 目标 | 推荐特写 | 避免 |
|------|----------|------|
| 证明赢家更稳 | 嘴角、眼神、肩膀放松、手离开键盘但不慌 | 远处人群里“看起来很自信” |
| 证明候选人 freeze | 光标闪、手悬在键盘上、眼睛看屏幕不动、嘴微张 | 大喊崩溃 |
| 证明产品 edge | 角色低声 reveal、电脑前重新聚焦、面试官反应、offer布局 | 可读UI、产品界面说明 |
| 证明社交攀比 | 假笑停顿、眼神扫 offer 信封、手搭肩但身体僵 | 旁白解释嫉妒 |
| 证明隐藏证据 | 手指翻标签、badge边缘、信封角标、后衣领内侧 | 正面大 logo 或漂浮 logo |

写 prompt 时，至少选2个特写作为全片的“证据镜头”。如果只有场景和人群，没有证据镜头，生成效果通常会像普通广告片。

## 面试场景规则

- 候选人在真实线上面试中必须坐在电脑前，眼睛锁定笔记本屏幕。
- 不要手机，除非是面试前的闲散状态且用户明确需要。
- 屏幕可显示一个全屏实时视频通话：一位面试官的脸占据几乎整个屏幕。
- 面试官默认沉默，只做细微倾听反应；不要让面试官抢台词或嘴型同步说话。
- 如果模型文字生成差，不要要求屏幕出现可读文字、品牌名、按钮或产品UI。

## 禁止项

默认写入prompt末尾：

```
不要字幕、不要captions、不要meme文字覆盖、不要标题卡、不要片尾卡。不要水印。不要可读UI、不要FinalRound logo、不要产品界面。画面中不要出现任何可读文字。
All spoken dialogue and voiceover must be English only. No Chinese spoken words. No Chinese text.
```

如用户明确要求强制生成可读文字或 logo，再单独覆盖此规则。可读文字必须限制在一个最短词组；logo 必须优先用真实素材 reference 或后期叠加，不要让模型自由想象。

如果用户明确指定 logo 出现位置，把它当硬构图约束：写清 logo 所在的真实物理载体、镜头方向和负面位置。例如衣领标签、badge、电脑贴纸、offer 信封角标；不要让 logo 漂浮、变成光环、变成抽象符号或出现在错误身体部位。

## 工作流

1. **提取参考梗**：确认它的核心不是表面画面，而是剪辑结构、情绪关系和hook机制。
2. **确认产品面**：默认使用 Live Interview Copilot / Desktop Stealth App；只有用户明确指定时才切到 Mock Interview、Resume Builder、AI Job Hunter / Auto Apply 或 full stack。
3. **判断转化状态**：如果是纯新闻讽刺或纯 IP 仿写，先标成“待转化”；只有当剧情已经接到面试、offer、job market、candidate survival 或明确 FinalRound reveal 时，才写成完整 FinalRound-INS。
4. **解析 R2 资产**：如果涉及 R2 角色或真实人物 reference，先用 `references/r2-character-assets.md` 和 `rclone lsf` 确认 asset slug / 具体图片路径；生成时通过 presigned URL 传入 reference image，prompt 里只写 `Reference [n]`。
5. **IP转译**：如果用户借用电影、剧集、游戏、历史仪式或经典场面，读取 `references/ip-adaptation.md`，转成 safe template label，确认没有原片名/角色名/演员名/logo/台词进入生成 prompt。
6. **校准产品理解**：把卖点写成真实面试场景里的具体edge，不要把Interview Copilot写成mock interview，也不要让外围工具抢主线。
7. **选择内容bucket、心理hook、风格模块、喜剧模式和视觉模板**：默认先选娱乐化skit/POV/meme；再选求职者心态、FinalRound风格模块、喜剧模式和视觉模板。
8. **写Concept/Hook/笑点结构**：用1段concept + 1句first-3s hook + 1句转折说明，不先写长prompt。
9. **写15秒时间轴**：每2-3秒一个信息点；角色动作、视线、台词同时写。
10. **加模型护栏**：画幅、参考身份、禁止项、镜头运动限制、台词归属、IP/真实人物/新闻边界。
11. **加台词抽取块**：完整 prompt 末尾必须写 `The only spoken lines are:`，并逐行列出全部英文对白。
12. **QA自检**：检查 POV 是否基于用户新闻且两行以内，R2 角色是否已通过真实 reference 传入，prompt 是否避免敏感真人/公司身份词，是否有字幕/UI/logo/end card、是否玩手机、是否离开电脑、是否错误让面试官说话、主持人是否误入镜、赢家是否离镜头太远、FinalRound reveal 是否太早或太广告、纯新闻梗是否被误写成已完成广告、末尾是否有台词抽取块。

### 生成迭代模式

用户已经生成过视频并继续调版本时，按生成结果反推下一版，不要每次重写成新片：

1. **保留有效变量**：用户夸空间、光线、镜头距离、角色表情或节奏时，下一版优先继承这些变量。
2. **reference video复用**：如果 provider 支持，把被用户认可的视频作为 `reference_videos` 或等价参考，并写清只继承空间/光线/摄影/节奏，不继承原动作；如果 reference video 导致超时或上传失败，降级为文字锁定空间和轻量版 prompt。
3. **多版本对照**：用户要2个版本时，每版只改变一个主变量，例如镜头所有权、特写重点、反应重点、产品露出方式或 reference video 开关；人物资产、台词、产品 edge、画幅、禁止项保持一致。
4. **生成后检查**：下载成片并至少做缩略图/首帧检查；如果只看了 preview，汇报时明确说是基于 preview，不当作完整审片。

写完整prompt前，如果用户还在讨论方向，先输出这个短格式：

```
POV：一句英文短句，锁定视频主旨
产品面：Live Interview Copilot / Desktop Stealth App
产品接入状态：已接 FinalRound / 未接产品待转化
R2资产：需要 / 不需要；如需要，写 asset slug、Reference [n] 对应关系
ICP心理：一句话说明这条视频打中的求职者心态
社会关系：谁在赢、谁不服、谁在追问、谁掌握秘密
镜头所有权：谁在镜头内，谁只能画外音，谁不能拿麦或抢主持
空间站位：前排/后排/近景/背后/移动方向
风格模块：从FinalRound风格模块库选择1个，如 MrBeast Challenge / Kardashian Confessional / AI Fruit Short Drama
喜剧模式：从FinalRound喜剧模式库选择1-2个
视觉模板：从FinalRound视觉模板库选择1个
IP/新闻边界：不用原片名/角色名/真实logo/新闻台标/可读文字，真实人物只能做parody/skit
IP转译：不需要 / 需要；如需要，写 safe template label 和产品接入方式
3秒hook：第一句台词或第一个画面
FinalRound reveal：第几秒、由谁说、为什么不是硬广
禁止项：无字幕、无水印、无可读UI、无logo、无end card
台词抽取：The only spoken lines are: 后逐行列出全部英文对白
```

## 常用模板

### AI Won't Take Your Job

创作者先承接"AI will take our jobs"的恐惧，再反转成"this AI can help you get one"。

适合卖点：从AI焦虑转向求职优势。默认把优势落在真实面试中的Copilot支持，而不是泛泛求职工具。

### Interview Freeze

候选人以为只是behavior question，屏幕里的面试官沉默等待，候选人突然意识到这是压力面试。

适合卖点：Live Interview Copilot、临场救援、实时结构提示。

### MrBeast Challenge

把面试机会改写成一个高压挑战：极端条件、简单规则、倒计时、奖励或淘汰。不要模仿口头禅，重点是挑战结构和强反应。

适合卖点：高机会成本、面试只有一次、technical round限时压力、offer/callback/salary jump。

### Kardashian Confessional

用reality-show confession承接候选人的嘴硬、自我包装和面试前drama，再硬切到真实线上面试压力。

适合卖点：面试焦虑、表面精致但内心崩溃、Future/Past self、creator人格强的视频。

### AI Fruit Short Drama

用拟人化水果短剧承载求职压力，视觉荒诞但产品落点仍回到真实电脑面试和Live Interview Copilot。

适合卖点：低成本批量测试、夸张情绪、AI短剧账号风格、强视觉记忆点。

### Job Search Chaos

投了400份简历、忘改公司名、ATS黑洞、拒信轰炸、pajama配西装外套、面试前10分钟疯狂准备。用快切和混乱道具表现求职过程失控。

适合卖点：面试前的混乱如何导向真实面试中的崩溃，最终落点仍优先是 Live Interview Copilot。Resume Builder、AI Job Hunter、auto apply、full job-search stack 只在用户明确要求外围工具时作为补充。

### Behavioral Self-Intro Product Placement

把 "tell me about yourself" 拍成空泛自我包装失控：候选人突然像广告主持人一样说 corporate buzzwords，旁观者用反应镜头发现这不是正常面试回答。

适合卖点：FinalRound 把模板化、空泛、广告腔 self-intro 拉回具体经历、结果和岗位匹配。结尾不要只说产品名，要让候选人的最终回答明显更像真人、更具体。

### AI Job Market System Parody

把 AI job market、岗位消失、招聘系统、控制室和算法筛选拍成“系统反派”。反派可以是 AI CEO、控制室导演、telescreen founder 或系统广播，但要保持 parody / skit 边界。

适合卖点：求职者不是懒，也不是没有能力，而是在更不稳定的就业系统里需要面试现场结构和表达支持。FinalRound reveal 可以是反抗系统的一句短台词，随后用模糊 offer 布局或面试表现反转证明。

### Dystopian Recruiting Hidden Rule

把 elite tech recruiting / AI fellowship / hard interview 拍成威权招聘仪式：巨大 auditorium、telescreen、监控摄像头、台下聪明但紧张的申请者。权力角色突然穿破第四面墙，说出 hidden rule。

适合卖点：FinalRound 是高门槛面试里的隐藏准备规则，不是普通广告介绍。台词可以极短，例如 `"Smart people use FinalRound AI."`，但前面必须先建立“申请者很想进但怕过不了 interview”的压力。

### Tech Layoff Satire To FinalRound

把裁员、role optimization、AI acceleration 拍成游戏规则或系统惩罚时，默认先判断是否已经接到产品。如果没有 FinalRound reveal，它只是新闻讽刺素材，不要硬归入成品广告。

适合转化路径：被裁员工下一场真实面试、裁员后抢下一份 offer、被 AI job market 筛掉前用 FinalRound 稳住表达。转化完成前，在样例或备注里标清“未接产品 / 待转化”。

### AI Advantage Hot Take

用一句强观点开场，把传统职业建议打掉：AI不会拿走你的工作，会用AI的人会。旧的resume tips和career coach话术已经不够，求职者需要AI-native job prep。

适合卖点：全产品线、AI job search tools、career optimizer人群。

### Visual Tutorial / Demo

用screen recording + face cam、green screen、before/after或react形式展示工具，但必须有强人格和强剪辑。不要写成普通SaaS walkthrough。

适合卖点：优先展示 Live Interview Copilot / Desktop Stealth App；Mock Interview、Resume Builder、AI Job Hunter 只在用户指定教育内容或全家桶内容时展开。

## 模型适配

默认把完整prompt控制在2500字符以内即可，不需要为了极限省字牺牲清晰度。优先使用中文主体 + 英文台词。不要把模型适配写成五个完全不同的剧本；核心剧情、台词、禁止项保持一致，只按模型特点微调表达。

生成优先级：

1. **HappyHorse / 欢乐马**：默认第一优先级。适合快速批量测试竖屏社媒短剧。提示词要直接、少堆电影术语，重点强化人物身份引用、候选人位置、面试屏幕关系、动作节奏、禁止字幕/水印/可读UI。HappyHorse能力相对简单，不要期待复杂多镜头精细执行；需要用硬切时间轴写清楚每一段。失败预案：减少角色数量，保留一个主角 + 一个画外音 + 一个清晰 reveal。
2. **Kling / 可灵**：第二优先级。适合多镜头、正反打、复杂一些的叙事、音效或视频编辑。写清固定机位、硬切、左右视线、无变焦/推进/环绕。Kling容易执行镜头语言，但也容易加戏，所以禁止项要硬。失败预案：压缩到一个场景、一条视线规则、一句 reveal，减少抽象概念词。
3. **Seedance 2**：第三优先级。人物参考和社媒质感不错，但生成慢；长英文对白和复杂音效不如Kling稳定。适合需要 influencer 身份一致性、多参考图、中文主体 prompt 的版本。用清晰时间码控制动作，避免太抽象。若15秒多台词版本失败、排队过久或效果差，优先压缩成10秒版本测试，保留同一冲突、同一句产品收尾和核心台词。失败预案：减少对白，强化近景、手持、reference identity 和动作名词。
4. **Sora 2 / Sora 2 Pro**：第四优先级。适合需要更自然英语台词、同步声音、电影感更强的版本。可写得更自然口语化，但仍要保持无字幕、无end card、无可读UI。
5. **Veo 3**：第五优先级。适合写实、电影质感、环境氛围强的版本。对meme skit和强台词正反打不是默认首选；若使用，减少复杂剧情，强化单一情绪和真实表演。

## 常见错误

| 错误 | 正确做法 |
|------|----------|
| 只写“FinalRound帮她拿offer” | 写出她在什么面试/社交处境里被追问，为什么 reveal 有戏剧功能 |
| 前3秒先拍校园/办公室/大厅 | 前3秒直接拍脸、冲突、offer信封、面试官沉默或系统规则 |
| 产品太早出现 | 娱乐 skit 默认第10秒后 reveal，前10秒先建立状态差 |
| 只写“vlog感” | 写手机镜头所有权、手持晃动、谁在拍、谁被挤开、谁只画外音 |
| 只写“她很自信” | 用眼神、停顿、肩膀、嘴角、低声回答和别人反应证明 |
| logo位置含糊 | 写物理载体、镜头方向、负面位置，优先真实 reference 或后期叠加 |
| 台词很多但没有动作 | 每句台词绑定表情、手部动作、视线或镜头切换 |
| 新闻梗没接产品 | 标成“未接产品待转化”，先找 interview / offer / job market 入口 |
| 多版本全都重写 | 每版只变一个主变量，其他硬约束保持一致 |
| 生成失败后继续加形容词 | 减角色、减台词、减抽象概念，保留一条冲突和一个证据特写 |

## QA清单

输出前逐项检查：
- 是否是9:16竖屏15秒？
- 前3秒是否有脸、冲突和清楚的“谁在赢/谁在慌/正在发生什么”？
- 第4秒前是否有主角正脸/侧脸近景，或能识别身份和处境的高信息动作？
- 是否先锁定一句英文 POV？
- 如果用户给的是新闻内容，POV 是否严格基于新闻事实，而不是另起一个泛求职故事？
- POV 是否默认一行、最多两行，没有长因果解释？
- 如果用户提到 R2 资产或已存角色，是否查过 `references/r2-character-assets.md` 并复查 R2 具体图片路径？
- 生成时是否把 R2 图片作为真实 reference 传入，而不是只在 prompt 里用文字描述人物？
- prompt 里是否只写 `Reference [n]` 和中性角色身份，避免直接写平台敏感真人/公司身份？
- 是否写清社会关系、镜头所有权、空间站位和 reveal 机制？
- 关键动作或 reveal 是否有近景/特写，而不是只用大远景？
- 是否默认聚焦 Live Interview Copilot / Desktop Stealth App，而不是把外围工具当主卖点？
- FinalRound是否被写成真实面试中的Copilot，而不是mock interview？
- 是否选择了明确产品面，而不是泛泛说"AI工具"？
- 如果是纯新闻讽刺或纯 IP 仿写，是否明确“已接产品”还是“未接产品待转化”？
- 是否默认娱乐化、bold、relatable，而不是普通polished ad/talking head？
- 是否选择了明确喜剧模式，而不是只写"焦虑"？
- 是否选择了明确风格模块，而不是泛泛说"某某风格"？
- 是否选择了明确视觉模板，而不是泛泛说"INS风格"？
- 候选人真正面试时是否盯电脑，而不是手机？
- 是否没有end card？
- 是否没有字幕、水印、可读UI、FinalRound logo、产品界面？
- 如果用户明确要求 logo 或标签，是否写清真实物理载体、镜头方向和禁止漂浮/错位？
- 如果用户说 BGM 后期配，是否仍保留对白、环境声和短音效，同时禁止连续 BGM？
- 是否没有承诺guaranteed hired/guaranteed offer？
- 如果有画外音主持人/记者，是否保证主持人不出镜、不拿麦、不把台词错分给受访者？
- 如果有真实人物或新闻梗，是否明确 parody / skit 边界，避免真实背书或新闻 footage 质感？
- 如果有电影/电视剧/IP 致敬，是否禁止画面和对白出现原片名、角色名、演员名、logo 或可读引用？
- 如果用户点名 IP 或经典场面，是否读取 `references/ip-adaptation.md` 并转成 safe template label？
- 如果有公司名或裁员新闻，是否避免真实 logo、新闻台标、可读 badge、可读系统文字，除非用户明确要求？
- 如果是 behavioral self-intro，最终回答是否从 buzzwords 变成具体经历，而不是继续像广告话术？
- 如果是系统反派 / hidden rule 结构，FinalRound reveal 是否来自剧情反转，而不是硬塞一句广告？
- 面试官是否保持沉默？
- 多角色是否没有同框、没有分屏、没有反射同框？
- 正反打是否有明确左右脸和视线方向？
- 每句台词是否短到15秒内能说完？
- 完整 prompt 末尾是否有 `The only spoken lines are:`，并且只列英文台词？
