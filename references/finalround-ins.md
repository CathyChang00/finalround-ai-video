# FinalRound-INS 模式

FinalRound AI 竖屏社交广告 prompt 编译器。用于把 Instagram Reels / TikTok 热门梗、UGC脚本、面试焦虑场景改造成 FinalRound AI 广告。

## 触发条件

用户提到以下任一项时进入本模式：
- FinalRound / FinalRound AI / FRAI
- 面试Copilot / interview copilot / online interview / technical interview
- 求职、offer、behavior question、stress interview
- INS / Instagram Reels / TikTok / 竖屏9:16广告
- 把某个热门短视频梗改成 FinalRound 广告

## 和 Meme-Gen 的关系

不要复制 `refs/meme-gen.md` 的完整内容。FinalRound-INS 要借用的是 Meme-Gen 的**解构方法**，不是它的科技圈讽刺语境。

核心公式改写为：

```
FinalRound产品场景 × 求职者心理痛点 × 社媒梗结构 × Creator表演语法 → 15秒竖屏广告prompt
```

默认继承 Meme-Gen 的这些方法：
- 先提炼梗的核心结构，而不是只模仿表面画面。
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

FinalRound-INS 覆盖 Meme-Gen 的这些默认项：
- 视频默认是15秒竖屏9:16，不是16:9横版。
- 可以在15秒里使用固定机位正反打和硬切，不默认一镜到底。
- 默认不做end card，用户会人工后期剪辑。
- 默认不展示产品UI、logo或可读屏幕文字。
- 默认主产品面是 Live Interview Copilot / Desktop Stealth App，不是泛科技事件，也不是纯meme二创。

## 产品事实

- FinalRound AI 在C端的主心智和主付费场景是 **Live Interview Copilot / Desktop Stealth App**：真实面试中实时听题、转写、给结构、给提示、帮候选人稳住表达。
- 默认产品面优先级：1) Live Interview Copilot / Desktop Stealth App 2) Coding Copilot / System Design Copilot 3) Mock Interview（只作为进入Copilot前的准备）4) Resume Builder / AI Job Hunter / Auto Apply（次级内容/教育内容）。
- Interview Copilot 是真实面试中的实时辅助，不是 mock interview，不是单纯预演工具。不要把Mock Interview、Resume Builder、Auto Apply写成默认主卖点。
- 角色真正进入面试时必须和电脑互动，不要只玩手机。
- 除非用户明确要求，不要展示 FinalRound logo、产品界面、可读UI、可读屏幕文字；如果用户明确要求展示 logo，优先使用真实 logo 素材后期叠加或明确 reference，不依赖文生视频模型凭空生成 logo。
- 产品露出优先用一句短台词完成，例如 `"Open FinalRound AI."`
- 当剧情涉及"别人为什么拿到offer/进Google/听起来像已经被录用"时，默认把产品edge写成**结构化表达**，不要写成偷答案或背答案。优先使用 `"Not answers. Structure."`、`"FinalRound AI."` 这类短句。
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

## 默认规格

- 15秒竖屏9:16。
- 社交短视频广告，第一屏就是内容，不做landing/解释页。
- 前3秒必须出现强hook：一张脸、一个冲突、一句能让人停留的话。
- prompt主体可用中文压缩语义，但所有角色对白、旁白、口播、画外音必须只用英文；FinalRound 相关视频不得出现中文对白或中文口播。
- 每个生成视频prompt末尾必须显式写入：`All spoken dialogue and voiceover must be English only. No Chinese spoken words. No Chinese text.`
- 默认不要背景音乐；如用户要求声音，允许写角色台词、环境声、短剧式 SFX / reaction sound，例如 whoosh、record scratch、dramatic sting、notification pop，但不要连续铺底音乐。
- 如果参考源来自电影、电视剧或强 IP 场景，默认不要让生成模型自配乐，留给后期使用更准确的原片氛围音乐；如果参考源只是 Twitter / Instagram 梗、UGC短剧或社媒段子，可以生成轻量音效，但仍不要生成大段背景音乐。
- 不要字幕、水印、meme overlay、title card、end card。
- 默认不是polished ad，不是基础talking head。优先funny、trendy、relatable、out of pocket。
- 内容比例默认按80%娱乐、20%教育理解。除非用户明确要教程，否则先写娱乐化skit/POV/meme/storytelling。

### POV Hook 规则

用户只要问"写一个POV"或需要视频第一屏文案，默认输出**一句英文短hook**，不要写解释型长句。POV应该描述观众瞬间处境，而不是总结产品卖点。

好例子：
- `POV: Your classmate got the offer, and you have no idea how.`
- `POV: Your friend got into Google, and you find out the secret.`
- `POV: You realize she did not freestyle the interview.`

避免：
- 过长的因果解释，例如 `POV: It’s graduation day, your friend just got Google, and you realize she wasn’t naturally good at interviews.`
- 把FinalRound直接塞进POV，除非用户明确要强产品露出。

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

## FinalRound喜剧模式库

像 Meme-Gen 一样，先选1-2个喜剧模式，再写prompt。不要默认所有FinalRound内容都是"面试焦虑崩溃"。

| 模式 | 笑点结构 | 适合场景 |
|------|---------|----------|
| **低估打脸** | 主角以为问题很简单，下一拍发现自己完全低估了面试难度 | behavior question、system design、coding follow-up |
| **能量落差** | 一方极度慌乱/用力，另一方沉默、冷静或只用一句话终结 | candidate vs interviewer、future self vs past self、HR vs AI-prepped candidate |
| **错位认真** | 用灾难片/审判/谍战的严肃程度处理一场普通线上面试 | 高薪岗位、签证压力、裁员后唯一机会 |
| **荒诞加码** | 求职混乱每一拍更严重，但主角还在假装"我没事" | 拒信、投递、日历、面试提醒、简历版本失控 |
| **反高潮** | 巨大焦虑铺垫后，用一句极短的产品动作落地 | `"Open FinalRound AI."`、"Breathe."、"Answer the question." |
| **字面化隐喻** | 把求职者的心理隐喻变成真实画面 | 大脑离开会议、简历黑洞、机会从门缝溜走、未来自己敲书墙 |

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

## FinalRound风格模块库

风格模块决定整条视频的外壳和节奏。先选风格模块，再选喜剧模式和视觉模板。不要只写"某某风格"，必须先读取对应风格库，提取可迁移要素，再按当前任务应用。

### MrBeast Challenge

参考 `CathyChang00/ai-video-skill/ips/mrbeast` 的结构，但不要做普通 MrBeast 模仿。核心是"自愿参与的高压挑战"：极端条件、简单规则、明确奖励、倒计时、淘汰或反转。

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
- 如果用户指定 Valley girl accent，必须写清所有对白仍然是英文：`strong Valley girl accent, stretched vowels, slight upward intonation, LA mean girls / reality show girls tone`。不要写中文对白，不要中文口音。
- 沉默可以比大喊更有效。面试官沉默、候选人冻结、手停在键盘上，常常比解释更像真实面试。
- 不解释笑点，不做道德总结，不在最后一句升华；用硬切、表情或一句短产品动作收住。
- 每段动作要有递进：自信→迟疑→空白→求助→重新聚焦；不要把多个焦虑画面随机堆在一起。

## 视觉与剪辑规则

- 优先人物镜头，不依赖产品UI解释卖点。
- 可以使用固定机位正反打、硬切、两个空间交叉剪辑，这是INS/Reels梗结构，不受"15秒默认一镜到底"限制。
- 当用户要求两个人像在对话但不在同一空间时，使用严格视线规则：A朝画面右侧看，B朝画面左侧看，通过硬切让视线相接。
- 不要分屏、不要同框反射、不要同画面互动，除非用户明确要求。
- 避免复杂镜头运动。用户强调简单正反打时，写清楚：固定机位、硬切、无变焦、无推进、无滑轨、无跟拍、无环绕。

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

## 工作流

1. **提取参考梗**：确认它的核心不是表面画面，而是剪辑结构、情绪关系和hook机制。
2. **确认产品面**：默认使用 Live Interview Copilot / Desktop Stealth App；只有用户明确指定时才切到 Mock Interview、Resume Builder、AI Job Hunter / Auto Apply 或 full stack。
3. **校准产品理解**：把卖点写成真实面试场景里的具体edge，不要把Interview Copilot写成mock interview，也不要让外围工具抢主线。
4. **选择内容bucket、心理hook、风格模块、喜剧模式和视觉模板**：默认先选娱乐化skit/POV/meme；再选求职者心态、FinalRound风格模块、喜剧模式和视觉模板。
5. **写Concept/Hook/笑点结构**：用1段concept + 1句first-3s hook + 1句转折说明，不先写长prompt。
6. **写15秒时间轴**：每2-3秒一个信息点；角色动作、视线、台词同时写。
7. **加模型护栏**：画幅、参考身份、禁止项、镜头运动限制、台词归属。
8. **QA自检**：检查是否有字幕/UI/logo/end card、是否玩手机、是否离开电脑、是否错误让面试官说话。

写完整prompt前，如果用户还在讨论方向，先输出这个短格式：

```
产品面：Live Interview Copilot / Desktop Stealth App
ICP心理：一句话说明这条视频打中的求职者心态
风格模块：从FinalRound风格模块库选择1个，如 MrBeast Challenge / Kardashian Confessional / AI Fruit Short Drama
喜剧模式：从FinalRound喜剧模式库选择1-2个
视觉模板：从FinalRound视觉模板库选择1个
3秒hook：第一句台词或第一个画面
转折：第几秒从普通求职痛点转成FinalRound edge
禁止项：无字幕、无水印、无可读UI、无logo、无end card
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

### AI Advantage Hot Take

用一句强观点开场，把传统职业建议打掉：AI不会拿走你的工作，会用AI的人会。旧的resume tips和career coach话术已经不够，求职者需要AI-native job prep。

适合卖点：全产品线、AI job search tools、career optimizer人群。

### Visual Tutorial / Demo

用screen recording + face cam、green screen、before/after或react形式展示工具，但必须有强人格和强剪辑。不要写成普通SaaS walkthrough。

适合卖点：优先展示 Live Interview Copilot / Desktop Stealth App；Mock Interview、Resume Builder、AI Job Hunter 只在用户指定教育内容或全家桶内容时展开。

## 模型适配

默认把完整prompt控制在2500字符以内即可，不需要为了极限省字牺牲清晰度。优先使用中文主体 + 英文台词。不要把模型适配写成五个完全不同的剧本；核心剧情、台词、禁止项保持一致，只按模型特点微调表达。

生成优先级：

1. **HappyHorse / 欢乐马**：默认第一优先级。适合快速批量测试竖屏社媒短剧。提示词要直接、少堆电影术语，重点强化人物身份引用、候选人位置、面试屏幕关系、动作节奏、禁止字幕/水印/可读UI。HappyHorse能力相对简单，不要期待复杂多镜头精细执行；需要用硬切时间轴写清楚每一段。
2. **Kling / 可灵**：第二优先级。适合多镜头、正反打、复杂一些的叙事、音效或视频编辑。写清固定机位、硬切、左右视线、无变焦/推进/环绕。Kling容易执行镜头语言，但也容易加戏，所以禁止项要硬。
3. **Seedance 2**：第三优先级。人物参考和社媒质感不错，但生成慢；长英文对白和复杂音效不如Kling稳定。适合需要 influencer 身份一致性、多参考图、中文主体 prompt 的版本。用清晰时间码控制动作，避免太抽象。若15秒多台词版本失败、排队过久或效果差，优先压缩成10秒版本测试，保留同一冲突、同一句产品收尾和核心台词。
4. **Sora 2 / Sora 2 Pro**：第四优先级。适合需要更自然英语台词、同步声音、电影感更强的版本。可写得更自然口语化，但仍要保持无字幕、无end card、无可读UI。
5. **Veo 3**：第五优先级。适合写实、电影质感、环境氛围强的版本。对meme skit和强台词正反打不是默认首选；若使用，减少复杂剧情，强化单一情绪和真实表演。

## QA清单

输出前逐项检查：
- 是否是9:16竖屏15秒？
- 前3秒是否有脸和冲突？
- 是否默认聚焦 Live Interview Copilot / Desktop Stealth App，而不是把外围工具当主卖点？
- FinalRound是否被写成真实面试中的Copilot，而不是mock interview？
- 是否选择了明确产品面，而不是泛泛说"AI工具"？
- 是否默认娱乐化、bold、relatable，而不是普通polished ad/talking head？
- 是否选择了明确喜剧模式，而不是只写"焦虑"？
- 是否选择了明确风格模块，而不是泛泛说"某某风格"？
- 是否选择了明确视觉模板，而不是泛泛说"INS风格"？
- 候选人真正面试时是否盯电脑，而不是手机？
- 是否没有end card？
- 是否没有字幕、水印、可读UI、FinalRound logo、产品界面？
- 是否没有承诺guaranteed hired/guaranteed offer？
- 面试官是否保持沉默？
- 多角色是否没有同框、没有分屏、没有反射同框？
- 正反打是否有明确左右脸和视线方向？
- 每句台词是否短到15秒内能说完？
