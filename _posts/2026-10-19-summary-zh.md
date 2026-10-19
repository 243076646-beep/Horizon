---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 13 条内容中筛选出 3 条重要资讯。

---

1. [文章认为在 AI 时代，人的意图与品味仍是软件持久价值的来源](#item-1) ⭐️ 7.0/10
2. [RepRapMicron 将开源 3D 打印推向微米尺度](#item-2) ⭐️ 7.0/10
3. [DeepSeek 推出托管网页搜索与抓取 API，每千次请求 0.75 美元](#item-3) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [文章认为在 AI 时代，人的意图与品味仍是软件持久价值的来源](https://karrisaarinen.com/posts/someone-behind-the-software/) ⭐️ 7.0/10

Linear 联合创始人兼 CEO Karri Saarinen 发表了题为《Someone behind the software》的文章，提出随着 AI 接手编码乃至架构决策，产品的持久价值将转移到软件背后的人身上——即他们的意图、品味、价值观，以及决定该做什么、不该做什么的判断力。这篇文章在 Hacker News 上引发广泛共鸣，获得 304 分和 122 条评论。 这篇文章为当下许多开发者正面临的问题提供了一套说法：如果 AI 写代码比大多数工程师更快更好，那么软件从业者的价值到底体现在哪里？它的回答是产品愿景、品味和一致的观点，从而把 AI 重新定义为提升而非抹除人类判断力价值的力量，这会影响团队如何组织工作、招聘以及评估产品决策。 文章的核心观察之一是：大多数产品改动是叠加式的，而非对核心问题的改进，因为新增功能远比重新思考已有功能容易——于是产品逐渐沦为缺乏统一观点的一堆能力集合。这是定性的行业评论而非技术论断；值得注意的是作者本人领导一家产品公司，因此该文也可视为设计驱动型软件团队面对 AI 工具时的一种自我定位。

hackernews · tosh · 10月18日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50142573)

**背景**: 大语言模型编程助手与智能体工具近年进步迅速，如今由 AI 生成大量生产代码、甚至提出软件架构方案已属常态。这在软件行业引发了持续争论：究竟哪些人类技能仍然稀缺且有价值。文章引用了 Dorothy Sayers 的《The Mind of the Maker》一书，Fred Brooks 曾在《人月神话》中引用它，把创造性活动分为构想、实现与交互三个阶段——这一框架也被多位评论者提及。

**社区讨论**: 评论者普遍认同文章观点。一位 SaaS 开发者表示，如今价值既不在代码、甚至也不在架构上（这两方面 AI 正在赶超），而在于决定该做什么、不该做什么。其他人进一步指出，AI 自身并不具备价值观、意图和品味；还有读者把它与 Fred Brooks 引用过的 Dorothy Sayers 创作三阶段模型（构想、实现、交互）联系起来。一个反复出现的担忧是：基于智能体的工作流会助长叠加式、缺乏整体愿景的产品改动。

**标签**: `#AI`, `#software-engineering`, `#product-design`, `#human-judgment`, `#industry-commentary`

---

<a id="item-2"></a>
## [RepRapMicron 将开源 3D 打印推向微米尺度](https://github.com/VikOlliver/RepRapMicron/wiki) ⭐️ 7.0/10

由 RepRap 社区开发者 Vik Olliver 主导的开源项目 RepRapMicron（μRepRap）正将可自我复制的 RepRap 3D 打印机理念延伸到微米级制造，其 wiki 记录了定制硬件设计、工具头和控制软件。该项目已经成功打印出仅 0.650 毫米大小的 3DBenchy 小船模型，向实现约 10 微米乃至更小特征尺寸的目标迈出了实质性一步。 如果微米级增材制造变得廉价且普及，就有可能把微芯片和微型器件的原型制作从昂贵的洁净室转移到爱好者和小型实验室手中，正如当年 RepRap 让桌面 3D 打印走向大众一样。这一前景引发了人们对 DIY 芯片制造以及新一轮开源硬件创新的遐想。 项目 wiki 记录了诸多实用的微加工变通方法，例如在异丙醇液滴中将打印件从 Krapton 胶带上取下，以及尝试使用指甲凝胶作为材料，同时团队也承认较大物体的打印质量仍是一大挑战。该项目仍处于早期演进阶段，尚不能算作经过验证的工业级突破。

hackernews · RobotToaster · 10月18日 13:48 · [社区讨论](https://news.ycombinator.com/item?id=50141076)

**背景**: RepRap 是一个长期运行的开源项目，它创造了可自我复制的 3D 打印机，目标是让任何人都能以低成本进行 FDM 式制造。普通桌面打印机的特征分辨率通常在 0.1 至 0.4 毫米左右，而微米级制造（特征尺寸以千分之一毫米计）历来依赖光刻和半导体式洁净室设备。RepRapMicron 试图把同样开放、可改造的打印机理念缩小到这一尺度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reprap.org/wiki/RepRapMicron">RepRapMicron - RepRap GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ... RepRapMicron: an open-source microscale RepRap… · AGI Hunt RepRapMicron – Hackaday The Latest From RepRapMicron – Nail Gel, First Objects, And ... RepRap: Blog Shrinking the Factory: Meet RepRapMicron, the Open-Source ...</a></li>
<li><a href="https://github.com/VikOlliver/RepRapMicron">GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ...</a></li>
<li><a href="https://www.4additive.com/en/reprap-micron-3dbenchy-smallest/">RepRap Micron : the smallest 3DBenchy is 0.650 mm - 4Additive</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者反应热烈，有人将其与 18 世纪 90 年代末的精密工程相类比，举出 Ramsden 的分度机、Maudslay 的螺纹车床和 Wilkinson 的镗床，视其为手艺转化为可靠批量生产的范例。其他人则开玩笑说终有一天能打印自己的内存条，或畅想芯片设计可以廉价且可持续地打印出来；不过也有评论者质疑，造出仅为自身千分之一尺寸的机器是否现实。

**标签**: `#RepRap`, `#3D printing`, `#microfabrication`, `#open hardware`, `#DIY manufacturing`

---

<a id="item-3"></a>
## [DeepSeek 推出托管网页搜索与抓取 API，每千次请求 0.75 美元](https://api-docs.deepseek.com/guides/search/) ⭐️ 6.0/10

DeepSeek 发布了托管网页搜索与页面抓取 API 的文档，定价为每 1000 次成功请求 0.75 美元。该服务让开发者无需自建爬虫或另行签约搜索供应商，就能为 LLM 应用接入实时网页检索能力。 这一价格远低于 Brave（约每千次 5 美元）和 Kagi（约每千次 12 美元）等成熟搜索 API，有望显著降低需要网页依据的智能体开发者的成本。它也加剧了这一市场的竞争——该市场的存在很大程度上是因为谷歌不向第三方开发者提供付费搜索 API。 计费按“成功请求”而非调用次数计算，失败或空结果的抓取不计费，不过文档尚未详细说明速率限制与抓取覆盖范围。讨论中提到的替代方案包括基于 SearXNG 的自托管工具，可免费抓取搜索结果，对个人爱好者和低用量场景仍是可行选择。

hackernews · fagnerbrack · 10月18日 06:50 · [社区讨论](https://news.ycombinator.com/item?id=50138531)

**背景**: LLM 智能体（agent）是把模型核心与工具、记忆和规划模块结合起来、能够执行联网查询等动作的 AI 系统。由于模型训练数据存在时间截止点，智能体通常在推理时调用搜索 API 获取最新网页，为其回答提供依据。DeepSeek 是一家总部位于杭州的 AI 公司，由对冲基金幻方量化（High-Flyer）出资支持，以 DeepSeek-R1 等开放权重模型闻名；推出付费检索 API 意味着它正从单纯的模型供应商向完整的智能体基础设施延伸。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.migramatters.com/llm-agents-ai-automation/">Everything About LLM Agents : The Future of AI... - MigraMatters</a></li>
<li><a href="https://developer.nvidia.com/blog/building-your-first-llm-agent-application/">Building Your First LLM Agent Application | NVIDIA Technical Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论主要围绕经济性与激励机制：不少人指出该价格远低于 Brave 和 Kagi，也有人认为这类服务之所以存在，正是因为谷歌拒绝提供付费搜索 API。还有人预测，随着智能体驱动的搜索增长，搜索 API 价格未来甚至可能变为负值，因为供应商在争夺对网络影响力的控制权；另有评论者表示自建 SearXNG 抓取对个人使用仍然免费，并建议 DeepSeek 采用“来源感知训练”，让模型能标注哪些事实来自哪个来源。

**标签**: `#search-api`, `#deepseek`, `#llm-agents`, `#api-pricing`, `#seo`

---