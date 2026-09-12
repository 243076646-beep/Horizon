---
layout: default
title: "Horizon Summary: 2026-09-12 (ZH)"
date: 2026-09-12
lang: zh
---

> 从 20 条内容中筛选出 3 条重要资讯。

---

1. [数学家抨击 OpenAI 在数学领域的“严重错位”](#item-1) ⭐️ 9.0/10
2. [开发者称 220 美元 Google 广告带来的安装中六成是机器人](#item-2) ⭐️ 7.0/10
3. [美国环保署拟取消数据中心污染许可的公众评审](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [数学家抨击 OpenAI 在数学领域的“严重错位”](https://mathandai.org/) ⭐️ 9.0/10

2026 年 9 月 11 日，陶哲轩发表题为《数学中 AI 的严重错位》的博客文章，而《经济学人》同日报道称，顶级数学家对 OpenAI 在数学领域的研究方法感到愤怒，争议焦点包括 OpenAI 声称其 AI 智能体解决了一个千禧年大奖难题。这场争议的核心在于 AI 公司如何将数学问题用作基准测试，以及成果应如何署名。 这场争议不仅关乎优先权或署名，更提出了 AI 生成的证明能否推进数学理解、商业激励是否正在扭曲学术研究文化等更广泛的问题。它会影响数学家、AI 实验室、期刊、资助机构，以及所有依赖可信数学知识的人。 陶哲轩的文章将这一局面称为“严重错位”，而《经济学人》指出批评者认为 AI 公司解决数学问题主要是为了给模型能力做基准测试，并称这对数学科学有害。具体的争议焦点似乎是 OpenAI 声称解决了纳维-斯托克斯方程这一千禧年大奖难题，并因其与 Buckmaster 和 Alpöge 先前工作是否独立而引发争论。

hackernews · meredydd · 9月11日 17:45 · [社区讨论](https://news.ycombinator.com/item?id=49662371)

**背景**: 陶哲轩是加州大学洛杉矶分校的数学家、菲尔兹奖得主，以在偏微分方程、组合学、调和分析和数论等领域的工作闻名。“AI 对齐”通常指让 AI 系统的目标与行为符合人类价值观和意图；陶哲轩借用这一术语来描述商业 AI 激励与数学规范之间的冲突。千禧年大奖难题是七个著名的极难数学问题，其中包括纳维-斯托克斯方程，每题悬赏 100 万美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terence_Tao">Terence Tao - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-ai-alignment">What is AI Alignment? - Stanford HAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_priority_controversy">Navier–Stokes priority controversy - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍担心 AI 公司的叙事夸大了进展，并损害学生、研究者和知识文化，不过也有数学家认为这可能类似望月新一的 abc 猜想事件：一个孤立且难以理解的证明仍激发了讨论。另一些人认为 AI 并未摧毁数学理解本身，而是打破了“解决未解决问题”这一传统衡量标准，带来署名和功劳分配问题；还有人将陶哲轩的批评比作波德莱尔对摄影的贬低。

**标签**: `#AI in mathematics`, `#AI alignment`, `#OpenAI`, `#academic ethics`, `#research culture`

---

<a id="item-2"></a>
## [开发者称 220 美元 Google 广告带来的安装中六成是机器人](https://dayzlegame.com/blog/google-ads-bot-farm/) ⭐️ 7.0/10

一位开发者在 Google Ads 上投入 220 美元推广自己的应用，通过分析获得的流量后判断约 60%的安装量来自机器人网络。这篇发表在 dayzlegame.com 上的文章在 Hacker News 上引发热议（265 分、150 条评论），讨论聚焦广告平台欺诈及如何过滤这类流量。 广告欺诈会推高每安装成本（CPI）并污染 Google 自动化应用广告系列的学习数据，使独立开发者和小型广告主的真实预算被浪费在非人类流量上。这也引发平台责任问题：投放出机器人流量的同样是 Google，而它又会通过 AdMob 以无效流量为由封禁开发者账号。 评论者指出，机器人网络通常运行在数据中心而非住宅 ISP 上，因此广告主可通过 Google Ads 后台的 IP 排除功能（Admin &gt; Account Settings &gt; IP Exclusions）按整个网段进行屏蔽，一位广告主称其在美国的排除列表已超过 4000 个网络。检测依然困难，因为点击农场使用真实设备和住宅代理，而行业报告显示即使经过平台过滤，欺诈率有时仍超过 60%。

hackernews · nickabe · 9月11日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=49662990)

**背景**: Google 应用广告系列（原通用应用广告系列）是 Google 的自动化广告产品，会把预算分散投放到搜索、Play 商店、YouTube 和展示网络以获取应用安装，通常按每安装成本（CPI）计费。移动广告欺诈由机器人、点击农场、设备模拟器和住宅代理网络制造，产生虚假点击和安装，其中住宅代理尤其难以识别，因为流量看起来来自真实的消费者网络连接。AdMob 是 Google 的移动广告变现网络，当开发者应用被判定产生无效流量时，它会例行封禁账号或扣留收入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tapper.ai/protect/google-ads/app-campaigns/click-farms">Click Farm Fraud on Google App Campaigns | Tapper</a></li>
<li><a href="https://www.anura.io/fraud-tidbits/bot-advertising-how-you-can-protect-your-roi">Bot Advertising: How Bots Hijack Ad Spend - Anura.io</a></li>
<li><a href="https://www.clickcease.com/blog/ad-fraud-is-a-problem-why-is-it-unfixable/">How To Stop Ad Fraud Problems | ClickCease Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了具体的应对手段，例如通过 Google Ads 后台排除 IP 网段（有人的排除列表覆盖 4000 多个网络），并指出一个讽刺的闭环：AdMob 以无效流量为由封禁开发者，而这些流量恰恰是 Google Ads 自己带来的。有人认为 Google 和 Meta 等付费广告平台本质上是骗局，也有人追问机器人运营者靠安装应用究竟能获得什么收益，还有读者表示这篇文章让自己去下载了这款应用，并很喜欢其清爽的界面。

**标签**: `#ad-fraud`, `#google-ads`, `#bot-traffic`, `#mobile-apps`, `#online-advertising`

---

<a id="item-3"></a>
## [美国环保署拟取消数据中心污染许可的公众评审](https://capitalbnews.org/data-centers-permit-rules-epa/) ⭐️ 7.0/10

美国环保署（EPA）提出一项新规，拟取消联邦层面对各州的要求，即在对工业设施（包括全美各地新建的数据中心）发放空气污染许可前必须通知公众并开放公众意见征询期。环保署已于周三就该提案举行公开听证会，这一变更将把公众如何——甚至是否——参与许可程序的裁量权大幅下放给各州。 数据中心依靠柴油发电机和燃气轮机进行主用与备用供电，已成为快速增长的空气污染源，因此取消公告与公众评议会让居民更难了解或反对新建设施。此举正值 AI 与云基础设施扩张与地方反对、电网瓶颈相冲突之际，也与环保署整体放松监管的方向一致。 倡导者警告，若取消公众评审，数据中心等设施可能完全规避“重大污染源”管控，许可证实际上可能在闭门状态下发放。该提案针对各州如何处理特定新增空气污染源的公众参与，而环保署此前的指导意见已允许各州在机构审核 Title V 许可证的同时并行开展公众意见征询。

hackernews · doener · 9月11日 18:05 · [社区讨论](https://news.ycombinator.com/item?id=49662672)

**背景**: 根据《清洁空气法》的新污染源审查（New Source Review）程序，许可审批机构通常必须在批准新工业污染源的空气许可证之前发布公告、开放公众评议期（通常为 30 天）并提供公开听证机会。数据中心依赖固定式燃气轮机和内燃机作为主用与备用电源，这些设备须遵守新污染源性能标准（NSPS）和有害空气污染物排放标准（NESHAP）。当前的环保署此前已发布指导意见以简化 Title V 运营许可证流程，并为数据中心开发商设立了《清洁空气法》资源页面，这是加快 AI 基础设施审批的更广泛努力的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.motherjones.com/politics/2026/07/trumps-epa-wants-fewer-people-asking-questions-about-data-center-pollution/">Trump’s EPA Wants Fewer People Asking Questions About Data ...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/aug/25/datacenters-air-pollution-epa">Trump EPA aims to exempt datacenters from disclosing air pollution, advocates warn | Trump administration | The Guardian</a></li>
<li><a href="https://www.epa.gov/stationary-sources-air-pollution/clean-air-act-resources-data-centers">Clean Air Act Resources for Data Centers | US EPA</a></li>

</ul>
</details>

**社区讨论**: 评论几乎一边倒地批评，认为该提案是环保署在当前政府下被削弱并持续放松监管的一部分，有人指出该机构“甚至不被允许衡量气候变化的影响”。多位评论者认为这一变动反过来证明了此前成功阻止数据中心的社区是正确的，也有人警告反对者若不采取极端手段，阻止项目的时间已经不多了。

**标签**: `#data-centers`, `#regulation`, `#environment`, `#AI-infrastructure`, `#policy`

---