---
layout: default
title: "Horizon Summary: 2026-09-07 (ZH)"
date: 2026-09-07
lang: zh
---

> 从 9 条内容中筛选出 5 条重要资讯。

---

1. [Asahi Linux 宣布正式支持 Apple M3 Mac](#item-1) ⭐️ 9.0/10
2. [一文抨击不披露 LLM 写作有违智识诚信](#item-2) ⭐️ 8.0/10
3. [A/I 集体被美方列为恐怖组织后宣布关闭](#item-3) ⭐️ 8.0/10
4. [末日刷屏加剧焦虑，侵蚀深度阅读习惯](#item-4) ⭐️ 7.0/10
5. [欧盟 AI 合规栈正演变成为三个互不连通的层级](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Asahi Linux 宣布正式支持 Apple M3 Mac](https://asahilinux.org/2026/09/m2-episode-1/) ⭐️ 9.0/10

Asahi Linux 宣布正式支持 Apple M3 Mac，这是在 Apple Silicon 上运行 Linux 的一个重大里程碑。这项支持是通过对 M3 硬件进行大量逆向工程来实现 Linux 内核和设备驱动的。 这会将 Linux 生态系统扩展到苹果最新的 Mac 硬件上，为用户提供可行的开源替代方案来取代 macOS。这也彰显了社区逆向工程如何跟上苹果专有芯片平台的步伐。 某些功能仍不完善，例如待机/唤醒和 HDMI 支持，这可能阻碍用户采用。早期用户报告还显示，GPU 计算性能（如 llama.cpp）仍不及 macOS 上原生 Metal 后端的表现。

hackernews · mdp2021 · 9月6日 14:08 · [社区讨论](https://news.ycombinator.com/item?id=49586698)

**背景**: Asahi Linux 是一个由志愿者驱动的项目，旨在将 Linux 内核及相关软件移植到 Apple Silicon Mac 上。由于苹果不提供 M 系列芯片的公开文档，该项目需对硬件和驱动接口进行逆向工程。这项工作始于 M1 芯片，并逐步扩展到 M2 等更新 SoC，现在又扩展到 M3。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Asahi_Linux">Asahi Linux — Grokipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞这一工程成就，并表达了对项目的支持。然而，一些用户指出采用障碍，如待机和 HDMI 支持不完善；还有用户报告称 llama.cpp 的 GPU 性能比 macOS 的 Metal 后端差得多。另有用户询问在 M2 MacBook 上如何将 Asahi 与 macOS 双启动。

**标签**: `#linux`, `#apple-silicon`, `#asahi-linux`, `#gpu`, `#open-source`

---

<a id="item-2"></a>
## [一文抨击不披露 LLM 写作有违智识诚信](https://bcantrill.dtrace.org/2025/12/05/your-intellectual-fly-is-open/) ⭐️ 8.0/10

布莱恩·坎特里尔（Bryan Cantrill）于 2025 年 12 月 5 日发表文章，认为在写作中使用大语言模型（LLM）却不披露属于智识上的不诚实。该文在软件工程社区引发了大量讨论。 这篇文章触及 AI 伦理的核心争论：未经披露的 LLM 辅助是否会损害真实性与信任。它之所以重要，是因为写作被广泛视为思考的一部分，而外包写作可能影响工程师和写作者在职业上的声誉。 文章的核心观点是，LLM 不擅长写作，而且最关键的是它们不是你。有评论者指出，写作迫使你把想法条理化，过程中观点本身也可能发生改变。

hackernews · cyb0rg0 · 9月6日 11:56 · [社区讨论](https://news.ycombinator.com/item?id=49585644)

**背景**: 布莱恩·坎特里尔是知名的系统工程师，以共同创造 DTrace 闻名，并经常撰文讨论技术与文化。文章标题借用「拉链开了」的比喻，暗示未披露的 AI 生成文字会让人陷入尴尬或丑闻。近年来 LLM 的能力使生成流畅文本变得更加容易，也引发了新闻和软件工程界关于披露规范与智识诚信的讨论。

**社区讨论**: 大多数评论者认同文章立场。jeremyjh 补充说，写作即思考，写作过程可能改变自己的观点；jgrahamc 强调个人风格和价值；ericbarrett 用餐厅比喻说明真实性。dynm 则对「因为 LLM 写得不好所以不该用」的论证持怀疑态度，认为真正的问题在于真实性。

**标签**: `#LLM`, `#writing`, `#AI ethics`, `#intellectual honesty`

---

<a id="item-3"></a>
## [A/I 集体被美方列为恐怖组织后宣布关闭](https://keepitfree.ai/announcements/a/i-shuts-down-stay-human/) ⭐️ 8.0/10

2026 年 8 月 26 日，美国国务院将意大利技术集体 Autistici/Inventati（简称 A/I）认定为“特别指定全球恐怖分子”。A/I 随后宣布关闭，并在告别信息中写道“保持人性”。 此次事件是美国反恐制裁罕见地直接压垮一个小型、以隐私为核心的技术集体，其影响远不止于该组织自身。这很可能对独立的互联网基础设施服务提供者以及依赖这类服务的异见者造成寒蝉效应，并加剧围绕言论自由、监控与技术自主权的争论。 根据美国的这项认定，美国人和美国金融机构不得与 A/I 开展业务，其在美管辖范围内的资产也会被冻结。美国国务院及支持这一决定的媒体声称，A/I 为与 Antifa 有关的活动人士搭建了数字基础设施，并指称波特兰的 Antifa 与哈马斯及伊朗伊斯兰革命卫队（IRGC）存在关联。

hackernews · captainmuon · 9月6日 14:34 · [社区讨论](https://news.ycombinator.com/item?id=49586898)

**背景**: Autistici/Inventati，简称 A/I，是一个总部位于意大利的集体，2001 年成立，向活动人士、独立记者以及 Indymedia 等社会运动提供安全电子邮件、网站托管和其他数字服务。它长期抵抗国家监控，包括 2004 至 2005 年意大利邮政警察的窃听事件，以及 2010 年其挪威服务器被查扣。美国国务院 2026 年 8 月 26 日的“特别指定全球恐怖分子”认定成为压垮该集体的决定性压力，最终导致其自愿关闭。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Autistici/Inventati">Autistici/Inventati - Wikipedia</a></li>
<li><a href="https://political.org/2026/08/26/state-dept-designates-italy-based-a-i-collective-as-global-terrorist-exposing-portland-antifas-links-to-hamas-and-irans-irgc/">State Dept. Designates Italy-Based A/I Collective as Global ...</a></li>
<li><a href="https://thepostmillennial.com/revealed-extremist-group-a-i-collective-builds-digital-infrastructure-to-support-antifa">REVEALED: ‘Extremist group’ A/I Collective builds digital ...</a></li>

</ul>
</details>

**社区讨论**: 评论区弥漫着悲伤与声援，有人感叹：一旦你从“中性客户”变成“负担”，通向孤立的路就会非常短。也有人以讽刺口吻指出美国“言论自由绝对主义者”这次反而沉默，甚至开玩笑说要“指定”美国政府为国际恐怖组织。另一些评论则提出更广泛的担忧，例如欧洲 NGO 被切断银行服务，还有人质疑 A/I 的用户审核机制凭什么能成为指控其“实质协助”恐怖主义的依据。

**标签**: `#AI`, `#government`, `#shutdown`, `#free speech`, `#surveillance`

---

<a id="item-4"></a>
## [末日刷屏加剧焦虑，侵蚀深度阅读习惯](https://www.edwest.co.uk/p/doomscrolling-ourselves-to-death) ⭐️ 7.0/10

文章指出，末日刷屏（doomscrolling）和算法驱动的社交媒体信息流会加剧焦虑和拖延，同时削弱深度阅读与持续专注的能力。它呼吁读者采取更有意识的信息消费方式，而不是被动地沉浸在无休止的短内容中。 这篇文章将个人数字习惯与注意力经济、科技对心理健康的更广泛社会影响联系起来。它引发了热烈讨论（例如 Hacker News 上大量评论），表明这一话题引起广泛共鸣，也丰富了关于社交媒体如何塑造认知与福祉的现有辩论。 本文发表于 edwest.co.uk，属于观点与社会评论，而非新的实证研究。根据资讯条目，它在 Hacker News 上获得 361 个点赞和 256 条评论，显示出极高的社区参与度。

hackernews · shubhamjain · 9月6日 11:53 · [社区讨论](https://news.ycombinator.com/item?id=49585627)

**背景**: 末日刷屏（doomscrolling）指一种强迫性地大量消费负面新闻和社交媒体内容的行为，往往会损害人的心理状态。“注意力经济”描述的是数字平台如何争夺用户有限的时间和专注力，通常借助算法信息流和旨在最大化参与度的短内容。这些现象常被用来解释人们对长文阅读耐心下降以及焦虑情绪上升的原因，这正是本文关心的核心问题。

**社区讨论**: 评论者大多认同文章的观点，并分享了个人在焦虑、拖延以及信息流取代长文阅读方面的挣扎。一位读者坦承自己起初只是略读文章，后来意识到跳过长文正是问题所在；其他人则讨论阅读书籍减少究竟是因为信息过载还是注意力缺失。还有一条批评性评论指出，重度使用社交媒体会在明显程度上改变人的性格，而重度看电视并不会如此。

**标签**: `#doomscrolling`, `#digital wellbeing`, `#social media`, `#attention economy`, `#technology and society`

---

<a id="item-5"></a>
## [欧盟 AI 合规栈正演变成为三个互不连通的层级](https://news.google.com/rss/articles/CBMiuwFBVV95cUxNTDNhdDVxaEtfV0QtbktKRWZRZERzNy15d2pZUjJPRjJjaUVYNmczSG9UUUFRRThZOThVbzRGZy1qY2w5Vlo0Vl9EYktpcm8zU21HZmxINTZvTlludlBRbkhZeHp4WHR1a3hhN3JvYXNZb3JNMkVHSjRpRUJGMnZRRkwwbXJScENCZTNEand0UkZyaWxESTVFTkFDSmNfNkdnNUE3ZmhWS1RSVW5obEZiSVltZjRoTlJKMU9F?oc=5) ⭐️ 6.0/10

欧盟的 AI 合规版图不再只是《AI 法案》：它已固化为三个不同步的层级——《AI 法案》《网络弹性法案》以及 MiCA/DORA，彼此之间互不认可。企业现在需要在这三套制度下运行并行的合规流程，而时间表相互错位。 这种碎片化提高了在欧盟境内开发或部署 AI 系统的企业的合规成本和法律不确定性。它同时说明审慎的企业必须同时跟进多套规则，这可能会拖慢欧洲 AI 创新的步伐。 这三个层级缺乏互认或统一的时间表，迫使企业进行重复的合规工作。一个 AI 产品可能要同时承担《AI 法案》的义务、遵守《网络弹性法案》的网络弹性要求，以及满足 DORA 的金融行业运营韧性规则，而这一切由相互独立的机制分别管理。

rss · GoogleNews-欧盟监管 · 9月6日 14:44

**背景**: 《欧盟 AI 法案》是欧盟针对人工智能的标志性风险分级立法，而《网络弹性法案》对数字产品和服务制定了网络安全要求。MiCA 监管加密资产，DORA 则聚焦金融服务中的数字运营韧性。它们共同构成所谓的“三层”，但由于各自独立起草，彼此并不互通，也没有统一的合规框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yahoo.com/news/world/articles/eu-ai-compliance-stack-crystallizing-144426898.html?fr=sycsrp_catchall">The EU AI Compliance Stack Is Crystallizing Into ... - Yahoo</a></li>
<li><a href="https://www.europesays.com/europe/131675/">The EU AI Compliance Stack Is Crystallizing Into Three Layers – and None of Them Talk to Each Other – Forkast - Europe</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI compliance`, `#AI regulation`, `#interoperability`

---