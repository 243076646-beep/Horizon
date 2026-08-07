---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 9 条内容中筛选出 5 条重要资讯。

---

1. [DeepSeek V4 Flash 0731 发布：更快、更便宜、获用户好评](#item-1) ⭐️ 8.0/10
2. [Oracle 的 OpenJDK 禁止 AI 生成的代码贡献](#item-2) ⭐️ 8.0/10
3. [科技从业者普遍悲伤与职业信仰丧失的现象剖析](#item-3) ⭐️ 7.0/10
4. [App Store 以不存在的塔罗牌功能拒绝应用，引发审核争议](#item-4) ⭐️ 7.0/10
5. [别再找便宜广告，用购买后追加销售提升订单额](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 发布：更快、更便宜、获用户好评](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731，这是 V4 Flash 模型的更新版本，现已通过官方 API 公开测试版提供。它保持了与 V4-Flash-Preview 相同的架构，但经过了重新后训练，在速度、能力和性价比上均有显著提升。 此次发布加剧了 AI 模型提供商之间的价格竞争，输入成本低至每百万 token 0.0028 美元，直接挑战 OpenAI 和 Anthropic。高速度与低成本的结合，可能让更多开发者和普通用户用上先进的 LLM 能力。 该模型是一个稀疏专家混合（MoE）模型，总参数 284B，激活参数 13B，适合编码、推理和智能体工作流。DeepSeek 指出此次更新仅升级了 V4-Flash API，V4-Pro 版本保持不变。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek 是一家以低价发布高性能模型而著称的中国 AI 实验室。V4 Flash 系列采用稀疏专家混合架构，在总共 284B 参数中只激活一小部分，以节省算力并保持强劲性能。这个 0731 版本紧跟在早前的 V4-Flash-Preview 之后推出，定价极具攻击性，不过 DeepSeek 已宣布即将大幅涨价。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://deepseek.com/en/index.html">DeepSeek</a></li>
<li><a href="https://api-docs.deepseek.com/updates/">Change Log | DeepSeek API Docs</a></li>

</ul>
</details>

**社区讨论**: 用户反应热烈，有人称速度是“杀手级功能”，并在 2x RTX Pro 6000 上测出约 8k tok/s 的预填充速度。还有用户强调运行成本极低，并质疑 OpenAI 或 Anthropic 如何与这样的价格竞争。不过，有用户提醒 DeepSeek 已宣布将大幅涨价，另有一位用户分享了账号被封的无关经历。

**标签**: `#deepseek`, `#llm`, `#ai`, `#model-release`, `#machine-learning`

---

<a id="item-2"></a>
## [Oracle 的 OpenJDK 禁止 AI 生成的代码贡献](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

OpenJDK 发布了一项临时政策，禁止 AI 生成的代码贡献，理由是法律问题和审查负担。该政策发布在 openjdk.org/legal/ai 上，并表示最终版本正在由他们的律师起草。 这之所以重要，是因为 OpenJDK 支撑着无数企业使用的 Java 平台，这一政策可能影响其他正在应对 AI 生成代码的开源项目。它也凸显了 Oracle 对 AI 的大量投入与其谨慎的法律立场之间的张力。 该临时政策明确提到了对代码来源、版权以及“人类审查者本已有限的时间”的担忧。最终版本正在由 OpenJDK 的法律团队撰写，社区预计它可能不会有太大改进。

hackernews · delduca · 8月7日 17:36 · [社区讨论](https://news.ycombinator.com/item?id=49213754)

**背景**: OpenJDK（开放 Java 开发工具包）是 Java 平台标准版的免费开源实现，最早由 Sun Microsystems 于 2006 年启动，2010 年被 Oracle 收购。作为 Java 的参考实现，它被众多大型企业广泛使用，因此其贡献政策影响重大。该项目有着版权和许可纠纷的历史，这很可能影响了 Oracle 对 AI 生成贡献的谨慎态度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK - Wikipedia</a></li>
<li><a href="https://www.redhat.com/en/topics/application-modernization/openjdk-vs-oracle-jdk">OpenJDK versus Oracle JDK</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Oracle 的动机表示怀疑，指出 Oracle 大力推广 AI 却又在 OpenJDK 中禁止 AI，具有讽刺意味。一些人支持该政策，认为这是减轻审查者负担的合理方式，而另一些人则怀疑此举是为了保留 Oracle 对“AI 洗白”代码提起诉讼的法律选择。

**标签**: `#OpenJDK`, `#AI Policy`, `#Open Source`, `#Legal`

---

<a id="item-3"></a>
## [科技从业者普遍悲伤与职业信仰丧失的现象剖析](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 7.0/10

《Noema》杂志这篇文章探讨了为何许多科技从业者深感悲伤并丧失职业信仰。文章指出，有毒的网络文化和行业深远变化是主要原因，并追问这对劳动力队伍意味着什么。 科技行业长期被视为创新与机遇的来源，因此集体士气低落可能影响生产力、人才留存和行业前景。理解这种幻灭感对雇主、政策制定者和从业者本人都有重要意义。 这篇文章出自《Noema》杂志，并在 Hacker News 上引发了大量关注，获得 338 个点赞与 477 条评论。社区回应包括关于职业倦怠的个人经历描述，以及与印刷业衰落的历史类比。

hackernews · RickJWagner · 8月7日 12:42 · [社区讨论](https://news.ycombinator.com/item?id=49209539)

**背景**: 科技从业者通常被视为享有特权和充满热情，但文章暗示许多人如今感到疏离和沮丧。文章将这种情绪与敌对的网络空间和颠覆性的行业变化联系起来，并与过去一些失去地位的技术行业进行类比。这一背景有助于解释为何这篇文章能在读者中引发强烈共鸣。

**社区讨论**: 评论者反应各异：有人将科技行业与印刷业的衰落相类比，有人指出当今网络的毒性，还有一位有二十年从业经验的程序员坦言自己如今甚至幻想流落街头。也有不同意见认为这篇文章的语气过于幸灾乐祸，但承认其具有社会意义。

**标签**: `#tech industry`, `#mental health`, `#career burnout`, `#online culture`, `#workforce trends`

---

<a id="item-4"></a>
## [App Store 以不存在的塔罗牌功能拒绝应用，引发审核争议](https://daringfireball.net/2026/08/app_store_rejection_of_the_week_dark_hours) ⭐️ 7.0/10

Daring Fireball 的一篇文章讲述了一位开发者的应用被 App Store 拒绝的经历：苹果 App 审核委员会声称该应用包含实时塔罗牌解读功能，但实际上应用中并没有塔罗、星座或任何占星相关功能。开发者多次升级申诉，但都以这一错误前提为由被驳回。 这一事件说明了 App Store 审核决定的随意性和不透明性，而对依赖 iOS 分发的开发者来说，这类决定可能产生巨大影响。它也加剧了人们对移动应用分发中“守门人”现象的批评，尤其是像主打占星的 Co-Star 这类应用曾获得 App Store 编辑推荐，形成了鲜明对比。 App 审核委员会的书面回复称“我们理解该应用包含实时塔罗牌解读功能”，然而开发者及其询问过的所有人都找不到这一功能。开发者在向 App 审核委员会层层升级申诉后，原拒绝决定仍被维持；文章将此视为审核流程失灵的一个典型案例。

hackernews · \_da\_ · 8月7日 18:59 · [社区讨论](https://news.ycombinator.com/item?id=49214863)

**背景**: App Store 要求所有 iOS 应用通过人工审核流程，以确保符合苹果的指导方针，但许多审核决定带有主观性，开发者往往缺乏有效的申诉途径。由于 iOS 和 Android 是两大主流移动平台，它们的应用商店政策实际上充当着大多数移动软件分发的“守门人”。这引发了关于公平性、透明度以及平台运营商对开发者权力的长期争议。

**社区讨论**: 评论者对这一荒谬裁定表示不满：szidev 指出完全基于占星的 Co-Star 曾获 App Store 编辑推荐，aliasxneo 则描述了在两大商店维护应用时遇到的各种不可预测性。MerrimanInd 认为两家公司把守着大多数移动软件分发是系统性问题，并推广了 Keep Android Open 运动；guessbest 则提到苹果目前似乎几乎不批准任何应用，并引用了开发者论坛上的讨论。

**标签**: `#App Store`, `#Developer Experience`, `#Mobile Apps`, `#Platform Governance`, `#Tech Criticism`

---

<a id="item-5"></a>
## [别再找便宜广告，用购买后追加销售提升订单额](https://www.reddit.com/r/ecommerce/comments/1vhz3gb/you_dont_need_cheaper_ads_you_need_bigger_orders/) ⭐️ 6.0/10

一位 Reddit 用户在 r/ecommerce 板块主张，店主不应再纠结广告成本，而应通过 Shopify 购买后页面的一键式追加销售来提高订单金额。帖子中附有具体财务算例，并推广了作者自己的 Shopify 应用 Abakira。 其重要性在于，广告成本不断上升，使得 CPA 难以压低，因此提高平均客单价是更省钱且更安全的利润杠杆。购买后追加销售尤其能在不危及已成交订单的情况下增加利润，这对处于盈亏平衡点的小型商家很有价值。 示例假设 AOV 为 45 欧元、产品成本 18 欧元、获客成本 25 欧元；如果每十个买家中有一个接受价值 20 欧元、成本 8 欧元的追加商品，平均订单额增加 1.20 欧元，每单利润从 2 欧元增至 3.20 欧元。作者的应用会在买家拒绝后展示另一个分支优惠，覆盖 Apple Pay 和 PayPal 订单的感谢页面，并采用固定费用、不抽成。

reddit · r/ecommerce · /u/water\_808 · 8月7日 12:20

**背景**: 购买后追加销售是指在买家完成付款后展示的优惠，通常出现在 Shopify 的购买后页面或感谢页上，买家只需点击一下即可把商品加入订单，无需重新填写支付或收货信息。它是 Shopify 结账流程中一种用于提升平均客单价（AOV）的产品优惠扩展。帖子还提到了 CPA（单次获客成本）——商家常试图通过广告优化来降低它——以及一种策略：在买家拒绝第一个优惠后，再以更优价格展示第二个优惠。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://shopify.dev/docs/apps/build/checkout/product-offers/build-a-post-purchase-offer">Build a post-purchase product offer checkout extension</a></li>
<li><a href="https://shopify.dev/docs/apps/build/checkout/product-offers">About product offers - Shopify Developers Platform</a></li>
<li><a href="https://gempages.net/blogs/shopify/post-purchase-pages">Post-Purchase Pages — Everything You Need to Know [2026]</a></li>

</ul>
</details>

**标签**: `#ecommerce`, `#shopify`, `#upsell`, `#AOV`, `#advertising`

---