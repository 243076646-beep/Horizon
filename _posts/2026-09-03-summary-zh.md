---
layout: default
title: "Horizon Summary: 2026-09-03 (ZH)"
date: 2026-09-03
lang: zh
---

> 从 17 条内容中筛选出 6 条重要资讯。

---

1. [谷歌发布 Gemini 3.8 Flash 与 Flash Cyber 模型](#item-1) ⭐️ 9.0/10
2. [Meta 的 Muse Spark 1.3 以低价刷新 DeepSWE 最好成绩](#item-2) ⭐️ 8.0/10
3. [调查发现三个网站生成 21.5 万篇“最佳软件”页面，被 AI 工具频繁引用](#item-3) ⭐️ 8.0/10
4. [谷歌在反垄断案中免于被拆分广告技术业务](#item-4) ⭐️ 7.0/10
5. [Mistral 数据训练退出选项引发企业信任争议](#item-5) ⭐️ 7.0/10
6. [每周追踪 120 万 TikTok Shop 商品，揭示销量增长最快的爆款](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [谷歌发布 Gemini 3.8 Flash 与 Flash Cyber 模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/) ⭐️ 9.0/10

谷歌发布了新一代 AI 模型 Gemini 3.8 Flash 与 Gemini 3.8 Flash Cyber。Flash 是一款快速、低成本的“主力”模型，在多项基准测试中排名前列，尤其擅长 HTML/JavaScript 生成；Cyber 则是谷歌在漏洞检测和自动修复方面最强的网络安全模型。 这表明谷歌正在快速迭代高效、低成本的模型，使它们在关键基准测试上足以匹敌甚至超越旗舰模型。这有望让开发者以更低成本获得前沿 AI 能力，而专门的 Cyber 模型也可能帮助安全团队大规模自动化防御工作。 据 Ars Technica 报道，这是谷歌六周内第三次发布 Flash 模型，Flash Cyber 取代了较早的 3.5 版本。社区早期测试显示，该模型在 Artificial Analysis 上的智能得分为 59，与 Opus 5 medium 相当；simonw 还报告称，仅花约 1.8 美分、13 秒就生成了一个可运行的 HTML/JavaScript 演示。

hackernews · bratao · 9月2日 15:12 · [社区讨论](https://news.ycombinator.com/item?id=49537553)

**背景**: Gemini 是 Google DeepMind 开发的多模态大语言模型系列，继承自 LaMDA 和 PaLM 2 等早期模型。Flash 系列定位为轻量、高效的模型，在保持较强推理能力和音频、视频等多模态输入能力的同时降低成本。Flash Cyber 则是面向网络安全任务的专门版本，用于漏洞检测和自动修复，并通过谷歌新的 Fairwind 计划提供给受信任的防御者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/">Introducing Gemini 3.8 Flash and 3.8 Flash Cyber</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.8 Flash — Google DeepMind</a></li>
<li><a href="https://arstechnica.com/ai/2026/09/google-releases-gemini-3-8-flash-its-third-flash-model-in-six-weeks/">Google releases Gemini 3.8 Flash, its third Flash model in six weeks - Ars Technica</a></li>

</ul>
</details>

**社区讨论**: 开发者整体反应积极。simonw 特别提到该模型速度快、成本低且 HTML/JavaScript 生成能力强，并认为多模态支持是最有趣的差异化优势，不过他也怀疑低“思考强度”相比 3.7 有所回退。还有评论者指出该模型在 DeepSwe 上击败 Opus 5，在智能分数上与 Opus 5 持平；jampa 则称赞了它在旅行规划应用中的真实世界知识和文档解析能力。

**标签**: `#gemini`, `#google`, `#ai-models`, `#benchmarks`, `#machine-learning`

---

<a id="item-2"></a>
## [Meta 的 Muse Spark 1.3 以低价刷新 DeepSWE 最好成绩](https://developer.meta.com/ai/models/muse-spark/) ⭐️ 8.0/10

Meta 发布了 Muse Spark 1.3，这是 Muse Spark 模型系列的最新版本，并宣称其 DeepSWE 得分为 75.4，是迄今看到的最高成绩。该模型的价格也非常便宜，社区测试显示一次简单的 API 生成只需几美分。 以如此低的价格取得 DeepSWE 顶尖成绩，会给前沿编程模型的定价带来压力，并可能加速 AI 编程市场的竞争。对开发者来说，这提供了一个价格便宜、性能优秀的软件工程选项，也说明基准领先并不一定意味着高昂的成本。 Muse Spark 1.3 的设计目标是维持长时间（long-horizon）任务，能使用工具并在一个长对话线程中处理多个工作流。社区早期实测中，用文本提示生成一张 SVG 花费了 38 秒、API 成本为 4.2266 美分，而且结果明显优于 Muse Spark 1.2 在相同任务上的输出。

hackernews · bvaldivielso · 9月2日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49541256)

**背景**: Muse Spark 是 Meta 开发的大语言模型系列，用于推理、编程以及多模态 AI 辅助工作。DeepSWE 是一个软件工程基准，用来评估编程代理在原创、长时间跨度任务上的表现，并设计为“无污染”基准，以减少旧有公开测试中常见的基准泄漏问题。因此，DeepSWE 高分被视为编程代理真实能力的重要信号。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.meta.com/ai/models/muse-spark/">Muse Spark 1.3 | Meta</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-spark-1-3">Introducing Muse Spark 1.3 | Meta AI Research</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>

</ul>
</details>

**社区讨论**: 总体来看，评论者对 Muse Spark 1.3 的 DeepSWE 成绩和极低价格非常兴奋；有人指出 Google Gemini 3.8 Flash 的榜首仅保持了几小时就被超过，并预计竞争会继续推低价格。实测中，1.3 在同一 SVG 生成任务上明显优于 1.2，还有多人称赞 Meta 的“contributor”定价方式，因为它透明地标出了允许用用户数据训练的价值。也有一部分人保持警惕，担心 Meta 在用户数据激励和企业行为方面的问题，例如涉及青少年与社交媒体的未决诉讼。

**标签**: `#AI`, `#Meta`, `#Muse Spark`, `#Large Language Models`, `#Machine Learning`

---

<a id="item-3"></a>
## [调查发现三个网站生成 21.5 万篇“最佳软件”页面，被 AI 工具频繁引用](https://trellner.com/reports/manufactured-sources-behind-ai-recommendations/) ⭐️ 8.0/10

一项调查发现，三个网站创建了 215,128 个“最佳软件”页面，这些内容很可能是 AI 制造的 SEO 垃圾内容。Perplexity 及类似 AI 工具在回答用户查询时频繁引用这些页面。 这很重要，因为 AI 问答引擎将低质量的自动化内容当作权威推荐呈现，削弱了人们对 AI 搜索的信任。它也揭示了一个反馈循环：AI 生成的垃圾内容被 AI 引用，既污染用户回答，又污染未来的 AI 训练数据。 报告似乎描述的是采用程序化 SEO 构建的网站，即用模板和数据批量生成针对搜索及 AI 引用关键词的对比页面。该调查特别指出仅三个域名就生成了 215,128 个页面，以此证明这不是正常的编辑内容。

hackernews · jakobgreenfeld · 9月2日 13:59 · [社区讨论](https://news.ycombinator.com/item?id=49536375)

**背景**: Perplexity AI 是一种 AI 驱动的搜索引擎，它将大型语言模型与实时网络数据相结合，在每条答案中标注引用来源。程序化 SEO 是一种常用技术，网站会自动生成成千上万个基于模板的页面以获取特定关键词流量，如今它越来越多地被用于让 AI 助手引用，而不再只是在传统搜索引擎中获得排名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Perplexity_AI">Perplexity AI</a></li>
<li><a href="https://www.semrush.com/blog/programmatic-seo/">What Is Programmatic SEO? Examples + How to Do It</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍批评 AI 生成回答的可靠性，有人说 LLM 似乎更偏向 AI 生成的文本而非人类编写的内容。还有人分享了 AI 工具编造地点或引用低质量生成页面的例子，一位用户指出 Perplexity 为追求速度已导致结果明显变差。另一位评论者认为，问题源于模型缺乏对信息来源动机的质疑，但他预计随着模型改进，这一漏洞窗口将会关闭。

**标签**: `#AI`, `#SEO spam`, `#Information quality`, `#Perplexity`, `#LLM training`

---

<a id="item-4"></a>
## [谷歌在反垄断案中免于被拆分广告技术业务](https://www.nytimes.com/2026/09/02/technology/google-ad-tech-remedies.html) ⭐️ 7.0/10

2026 年 9 月 2 日，美国法院驳回了政府要求谷歌出售其广告技术业务的请求，谷歌赢得此次反垄断诉讼，未被法院强制拆分。 这是一项重大的反垄断结果，意味着谷歌保住了年收入约 300 亿美元的广告技术业务。该案也凸显出在针对大型科技平台的反垄断案件中，拆分等补救措施极难实现，对监管机构、发布商和广告主都有深远影响。 谷歌的广告技术业务去年收入约 300 亿美元，占母公司 Alphabet 营收约 8%；不过该业务收入已连续 16 个季度下滑，分析师估计其利润占比不足 1%。此次裁决终结了司法部推动的强制剥离该业务的主张。

hackernews · donohoe · 9月2日 14:46 · [社区讨论](https://news.ycombinator.com/item?id=49537131)

**背景**: Ad tech 是“广告技术”的简称，指连接广告主与发布商、用于在网站、社交媒体和流媒体平台上买卖数字广告的软件和工具。谷歌长期以来控制着一套占主导地位的广告技术链条，涵盖广告购买、广告交易平台和发布商广告服务器等环节。美国反垄断执法机构此前主张，这种纵向控制使谷歌垄断了在线展示广告的关键环节，并要求其出售相关资产。此次法院裁决暂缓了拆分，不过谷歌在其他领域仍面临反垄断审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://advertising.amazon.com/library/guides/what-is-adtech">What is AdTech ? A Beginner&#x27;s Guide | Amazon Ads</a></li>
<li><a href="https://business.linkedin.com/advertise/resources/marketing-terms/what-is-adtech">What is AdTech ? The fundamental guide</a></li>

</ul>
</details>

**社区讨论**: 评论区普遍对判决持怀疑或不满态度。有评论者认为，合并公司应当和拆分公司一样困难；还有人建议对垄断企业征收累进税，促使它们自行拆分。另有评论批评科技巨擘越来越善于提前规避反垄断执法，也有人质疑谷歌广告技术业务是否真如报道所称那样边缘化。

**标签**: `#antitrust`, `#google`, `#adtech`, `#regulation`, `#tech policy`

---

<a id="item-5"></a>
## [Mistral 数据训练退出选项引发企业信任争议](https://help.mistral.ai/en/articles/455207-can-i-opt-out-of-my-input-or-output-data-being-used-for-training) ⭐️ 7.0/10

Mistral 的帮助文档解释了用户在何种条件下可以退出让其输入或输出数据用于训练。然而，Hacker News 上一些评估企业级使用的评论者报告称，Mistral 近期对 Team 版设置的变动，使基于提示词的训练默认开启，同时移除了在管理后台集中禁用该功能的选项。 企业客户越来越多地出于隐私、合规和数字主权考虑选择欧洲 AI 供应商，因此训练数据的默认策略和退出透明度直接影响采购决策。相关变动表明，即便是被定位为“可信替代方案”的供应商，政策也可能迅速变化，加深企业对无法可靠控制自身数据的担忧。 据用户反映，Mistral 的 Pro 版会默认将账户纳入提示词训练；切换到 Team 版以获取企业管理员控制后，用户发现相关设置也已变更：Team 版同样默认参与训练，并且集中退出的开关被移除或被隐藏。行业分析也指出，退出选项通常不能追溯撤销过去的数据使用，而且企业很少明确说明对输入/输出数据的“训练”具体包含什么。

hackernews · teekert · 9月2日 12:30 · [社区讨论](https://news.ycombinator.com/item?id=49535284)

**背景**: Mistral AI 是一家 2023 年成立、总部位于巴黎的法国人工智能公司，以开发大语言模型（其中许多开源）著称；截至 2025 年其估值已超过 140 亿美元，被视为欧洲应对中美 AI 竞赛的旗舰企业。在更广泛的行业中，AI 服务商经常使用客户的消息与内容来训练模型，而“退出”政策因服务而异，许多只适用于未来的交互数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mistral_AI">Mistral AI</a></li>
<li><a href="https://www.yahoo.com/lifestyle/opt-having-data-train-chatgpt-164450720.html">How to opt out of having your data ‘ train ’ ChatGPT and other AI ...</a></li>

</ul>
</details>

**社区讨论**: 许多评论者公开表示怀疑任何 AI 公司“不用你的数据做训练”的承诺，有人提到行业普遍存在数据抓取，还有人讲述微软 Copilot 在注册数月后擅自更改默认设置的前车之鉴。一位出于欧洲隐私管理而选择 Mistral 的用户表示，Pro 和 Team 两个版本都被曝默认纳入训练，令其两次失望，凸显根本性的信任问题。也有参与者批评这个 HN 标题对帮助页面具有误导性，还有人设想未来也许能通过对模型进行“知识探测”来证明自己的数据被擅自使用。

**标签**: `#AI ethics`, `#data privacy`, `#Mistral`, `#enterprise AI`, `#policy`

---

<a id="item-6"></a>
## [每周追踪 120 万 TikTok Shop 商品，揭示销量增长最快的爆款](https://www.reddit.com/r/ecommerce/comments/1w5cbaf/tracking_12m_tiktok_shop_products_week_over_week/) ⭐️ 6.0/10

一位 Reddit 用户分享了一套追踪系统的分析，该系统以滚动 7 天窗口覆盖 120 万个美国 TikTok Shop 商品，并公布了本周销量增幅最大的商品。本周增幅第一的是 LIGHT DOT 的男士快干运动 T 恤，单价 28.77 美元，周增约 311,823 件。 这项分析为电商卖家提供了一个基于周度数据的经验信号，帮助在商品变得拥挤之前发现即将进入 TikTok Shop“长尾右端”的潜在爆款，而不是依赖只能反映过去赢家的累计销量。它还揭示了 TikTok Shop 销售集中度极为极端，这对评估平台风险或机会的人都很有用。 数据显示这是一个典型的幂律市场：商品销量中位数仅为 4 件，均值约为 750 件，30%的上架商品从未售出，而头部约 1200 个商品各自销量超过 10 万件。约 60%的商品目录定价在 10 至 50 美元之间；作者在统计每周销量增量时，会筛选 4.0 以上评分且每家店铺只保留一款商品。

reddit · r/ecommerce · /u/dataform · 9月2日 14:42

**背景**: TikTok Shop 是 TikTok 应用内的电商功能，卖家可以直接通过短视频和直播进行销售。在幂律分布的市场中，极少数商品占据了总销售额的绝大部分，因此平均销售数据具有误导性，大多数上架商品销量很低。作者认为，相较累计销量，周环比销量增量是更能前瞻的指标，因为它能显示哪些商品眼下正在加速增长。

**标签**: `#ecommerce`, `#data-analysis`, `#tiktok-shop`, `#market-trends`, `#power-law`

---