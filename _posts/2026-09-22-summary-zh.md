---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 17 条内容中筛选出 4 条重要资讯。

---

1. [小米发布 MiMo v2.6 开放权重 MoE 模型家族](#item-1) ⭐️ 8.0/10
2. [NASA 取消火星采样返回任务](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill 回顾：Sun Microsystems 究竟错在哪里](#item-3) ⭐️ 8.0/10
4. [随笔《Attention is all you have》：注意力才是最稀缺的资源](#item-4) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [小米发布 MiMo v2.6 开放权重 MoE 模型家族](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

小米发布了 MiMo v2.6，一个大规模开放权重的混合专家（MoE）模型家族，其中 MiMo v2.6 Pro 总参数 1.02T、激活参数 42B，MiMo v2.6 Flash 总参数 309B、激活参数 15B。此次发布附带详尽的技术报告和实时强化学习训练仪表盘，权重以 MiMo-V2.6-Pro-RL 与 MiMo-V2.6-Flash-RL 之名发布在 Hugging Face 上。 这是一家中国消费硬件企业发布的前沿规模开放权重模型，延续了中国实验室（DeepSeek、阿里 Qwen、Moonshot、Z.ai）以宽松许可证发布大模型的模式，而美国多数头部实验室的最大模型仍保持闭源。异常透明的训练方法说明和公开的强化学习仪表盘，让研究者和爱好者难得地一窥万亿参数模型的实际训练过程，社区反应也显示可负担性与开放性正成为关键竞争因素。 由于采用混合专家架构，每个 token 只激活总参数中的一小部分（Pro 为 1.02T 中的 42B，Flash 为 309B 中的 15B），使推理与训练算力远低于同等总参数量的稠密模型。发布的权重文件名带有“-RL”后缀，表明这是经强化学习调优的版本，而技术报告被评价为在方法论上异常详尽。

hackernews · volf\_ · 9月21日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=49792730)

**背景**: 混合专家（MoE）是一种机器学习技术，它把模型拆分为许多专门化的子网络（即“专家”），再加一个路由器为每个输入只挑选相关的专家；这样模型的总参数量可以极大，而每个 token 只消耗其中一小部分的算力。“开放权重”指模型训练后的参数被公开下载，他人可以运行、微调或再分发该模型，但这并不等于完全开源的 AI——后者还包括训练代码、数据和中间检查点。这一术语带有政治色彩：中国实验室普遍倾向于以 Apache、MIT 等宽松许可证发布开放权重模型，而美国主要实验室往往将最大的模型保持闭源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open_weights">Open weights</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏小米的透明度，有人称实时强化学习训练仪表盘是“极佳的学习与教学工具”，技术报告也异常全面。多位用户表示如今对中国模型的期待超过美国模型，并把可负担性视为决定性因素；也有人探讨模型的行为怪癖，比如偏爱“01 - UPPERCASE TEXT”这类设计母题，以及经典的鹈鹕 SVG 渲染测试。

**标签**: `#LLM`, `#open-weights`, `#Xiaomi`, `#Mixture-of-Experts`, `#model-release`

---

<a id="item-2"></a>
## [NASA 取消火星采样返回任务](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

NASA 已取消“火星采样返回”（Mars Sample Return，MSR）计划，这一由 NASA 与欧洲航天局（ESA）合作的多任务工程原本要取回“毅力号”火星车自 2021 年以来在火星上封存采集的岩石、土壤和大气样本。该决定实际上终结了这项筹划多年、并于 2022 年正式获批的行星科学旗舰项目。 MSR 一直被视为行星科学领域最优先的目标，它的取消可能让中国的“天问三号”（计划 2028 年发射、约 2031 年带回样本）成为人类首次成功的火星采样返回，一些观察者称这对美国而言可能是一次“斯普特尼克时刻”。这一决定同时也将重塑喷气推进实验室（JPL）的任务布局以及 NASA 与 ESA 在火星探测上的合作关系。 该计划的成本估算从约 40 亿美元膨胀到 80 亿至 110 亿美元，样本运回时间也推迟到约 2040 年；其架构依托 ESA 的地球返回轨道器以及 Ariane 64 等较老的运载火箭，而非新一代重型运载器。作为参照，阿波罗宇航员带回了 842 磅（约 382 公斤）月球岩石，而“毅力号”封存的火星样本总量仅有几百克量级。

hackernews · Muhammad523 · 9月21日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49791939)

**背景**: 火星采样返回任务的思路是用机器人采集火星的岩石、土壤和大气物质并带回地球，再由配备更灵敏仪器的实验室进行分析，尤其是寻找可能表明火星曾经存在生命的生物标志物。由喷气推进实验室（JPL）建造和运营的 NASA“毅力号”火星车一直在把样本密封在采样管中留在火星表面，等待后续取回任务。研究人员曾提出返回的火星样本可能对地球生物圈造成反向污染，但航天机构普遍认为这一风险较低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tianwen-3">Tianwen-3 - Wikipedia</a></li>
<li><a href="https://www.space.com/astronomy/mars/china-on-track-to-launch-mars-sample-return-mission-in-2028-if-accurate-this-represents-a-sputnik-moment">China on track to launch Mars sample-return mission in 2028: &#x27;If accurate, this represents a Sputnik moment&#x27; | Space</a></li>

</ul>
</details>

**社区讨论**: 评论普遍认为取消的根源在于财务上不可行以及 JPL 的管理问题，指出 110 亿美元的成本和 2040 年的样本回送时间，并有人主张该任务本应围绕 Starship 或 New Glenn 等更便宜的商业重型火箭来设计。也有读者反驳文章的叙事，称其为从旧有 NASA 拨款模式中获益的机构所写的“自我怜悯式”辩护；另一些人则强调中国并行的天问三号计划，并分享了自己遭遇多次推迟的亲身经历，例如 ExoMars 的“罗莎琳德·富兰克林”号火星车。

**标签**: `#NASA`, `#Mars Sample Return`, `#space exploration`, `#policy`, `#JPL`

---

<a id="item-3"></a>
## [Bryan Cantrill 回顾：Sun Microsystems 究竟错在哪里](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

前 Sun Microsystems 工程师、DTrace 共同创造者 Bryan Cantrill 在其博客 bcantrill.dtrace.org 上发表了题为《What Sun got wrong》的文章，剖析了导致 Sun 衰落的战略与文化层面的失误。该文在 Hacker News 上引发了 283 条评论的热烈讨论，许多从业者分享了关于 Sun 销售文化和产品决策的第一手经历。 这篇文章是一个典型案例，说明一家公司如何在技术上领先却在商业执行上落败，这种模式在当今的基础设施、AI 和硬件创业公司中依然可见。对于工程师和技术管理者而言，它提供了关于销售模式、平台锁定和错失合作机会的具体历史教训，这些因素共同塑造了现代 Unix 与服务器市场格局。 文章的分析基于 Cantrill 在 Sun 任职期间的亲身经历，而社区讨论补充了若干具体决策，例如 Sun 在 2002 年短暂取消 x86 版 Solaris，这让许多客户相信自己会被锁定在 SPARC 平台上；以及 2002 年因 Sun 坚持要了解 Google 拥有多少台服务器而未能与 Google 达成交易。评论者还指出 Sun 昂贵的销售流程：买家要面对现场销售会议和没完没了的报价修改，有时光是服务器导轨和电源线的价格就超过了一台整机配送的 Dell 服务器。

hackernews · chmaynard · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 是硅谷的先驱企业，其运行 Solaris Unix 操作系统的 SPARC 工作站和服务器支撑了互联网泡沫时代的大量基础设施，Sun 的工程师还创造了 DTrace、ZFS 等颇具影响力的技术。Solaris 于 1993 年取代 SunOS，并因在 SPARC 硬件上的可扩展性而闻名，其大部分代码在 2005 年以 OpenSolaris 之名开源。互联网泡沫破裂后连年亏损，Sun 最终于 2010 年被 Oracle 收购，OpenSolaris 被终止，其代码后来分叉为 Illumos。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://en.wikipedia.org/wiki/Oracle_Solaris">Oracle Solaris - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认同这一批评，但在侧重点上有所争论：多人回忆 Sun 的销售流程远比 Dell 痛苦，有人提到 Alpha 服务器的导轨和电源线价格就超过一台整机配送的 Dell 服务器。其他人列举了具体失误——2002 年取消 x86 版 Solaris、搞砸与 Google 的交易——也有评论者认为 Sun 从来就没真正对经营企业感兴趣，只关心打造出色的技术，还有人把这桩往事与当下 AI 时代虚高的估值联系起来。

**标签**: `#Sun Microsystems`, `#systems history`, `#engineering culture`, `#Solaris`, `#tech industry`

---

<a id="item-4"></a>
## [随笔《Attention is all you have》：注意力才是最稀缺的资源](https://alicegg.tech/2026/09/21/attention) ⭐️ 7.0/10

2026 年 9 月 21 日，一篇发表在 alicegg.tech 上、题为《Attention is all you have》的随笔提出：在现代计算中真正稀缺的资源不是算力、存储或信息，而是人的注意力，而“被刻意设计出来的分心”已成为数字产品的默认属性。该文在 Hacker News 上获得 572 分和约 170 条评论，是当日讨论度最高的非技术类投稿之一。 这篇文章把注意力问题从“个人意志力”重新定义为经济与设计问题，促使软件从业者反思以“参与度”为导向的产品设计伦理。它的热度也反映出行业风向的转变：越来越多的开发者开始质疑那些以牺牲用户专注力来换取停留时长的指标。 这是一篇反思性随笔而非技术报告，因此没有基准测试或数据集，其价值主要在于论点及由此引发的讨论。评论区用具体例子加以延伸，例如有人指出 1993 年的 Mosaic 浏览器已支持历史记录全文搜索，而后来流行的书签系统反而退步了；也有人抱怨 Firefox 砍掉了 RSS 支持，却在界面中加入类社交元素。

hackernews · zer0tonin · 9月21日 14:26 · [社区讨论](https://news.ycombinator.com/item?id=49787726)

**背景**: 标题是对 2017 年提出 Transformer 架构的论文《Attention Is All You Need》的戏仿，但文章讨论的是人的注意力，而非神经网络中的注意力机制。其核心概念是“注意力经济”：这一源自信息管理与经济学的思路把人的注意力视为稀缺商品，研究以广告为收入来源的公司如何竞相争夺用户在产品上停留的时间。社交媒体信息流、YouTube 推荐和推送通知都是典型例子，它们被设计来诱发人们常说的“末日刷屏”（doomscrolling）式强迫性浏览行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Attention_economy">Attention economy - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Attention_Is_All_You_Need">Attention Is All You Need - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 整体情绪以认同为主：多位评论者分享了自己戒断社交媒体或转向更“有意识”的媒体消费的经历，也有人坦承自己在 Hacker News 上刷屏、在 YouTube 上半看半不看了几个小时，并有人提出用事先写好的任务清单或严格单任务来纠偏。最尖锐的批评来自用户 econ：他认为整理网络这件事被人为地退化了——Mosaic 的历史全文搜索让位于糟糕的书签系统，RSS 被社交组件取代——因为帮助用户自主管理浏览内容本身并不赚钱。

**标签**: `#attention-economy`, `#social-media`, `#digital-wellbeing`, `#hacker-news-discussion`, `#product-design`

---