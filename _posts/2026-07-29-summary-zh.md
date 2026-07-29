---
layout: default
title: "Horizon Summary: 2026-07-29 (ZH)"
date: 2026-07-29
lang: zh
---

> 从 20 条内容中筛选出 4 条重要资讯。

---

1. [Substack 作者应建个人网站](#item-1) ⭐️ 8.0/10
2. [Sebastian Raschka 分析 Kimi K3 的 NoPE 与 KDA 架构](#item-2) ⭐️ 8.0/10
3. [OpenAI 开源 Codex Security 命令行安全扫描器](#item-3) ⭐️ 7.0/10
4. [欧盟人工智能法案合规检查清单发布](#item-4) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Substack 作者应建个人网站](https://elizabethtai.com/2026/06/10/substack-writers-you-need-a-website/) ⭐️ 8.0/10

一篇文章指出，Substack 作者应自建网站以保持对内容和读者的控制，避免平台锁定。Hacker News 社区对此进行了广泛讨论，获得 379 分和 195 条评论。 这场辩论凸显了利用平台分发与保持内容所有权之间的日益紧张的矛盾。如果 Substack 改变政策或关闭，作者将面临失去读者和内容的风险，因此自建网站是重要的长期策略。 评论者提出了实用策略，例如使用自定义域名（如 subdomain.website.com）的 Substack，或先在个人博客发布，再复制到 Substack 进行邮件分发。Simon Willison 的博客转新闻稿脚本等工具促进了这种混合方法。

hackernews · speckx · 7月28日 16:58 · [社区讨论](https://news.ycombinator.com/item?id=49086788)

**背景**: Substack 是一个让作者发布新闻通讯并通过订阅变现的平台。然而，完全依赖 Substack 意味着作者的内容和订阅者名单都与平台绑定，一旦平台更改条款或停止运营，就会带来风险。拥有个人网站可以确保作者拥有完全控制权，并能轻松迁移到其他地方。

**社区讨论**: 评论者中出现了分歧：一方重视 Substack 的分发和易用性，另一方则优先考虑所有权和独立性。Simon Sarris 使用子域名方法保持控制，而 simonw 则采取混合发布方式，同时在个人博客和 Substack 上发表。Skippyfish 反驳说，自建网站缺乏触达读者的推送机制，认为 Substack 的邮件分发至关重要。

**标签**: `#Substack`, `#indie web`, `#content ownership`, `#blogging`, `#platform risk`

---

<a id="item-2"></a>
## [Sebastian Raschka 分析 Kimi K3 的 NoPE 与 KDA 架构](https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html) ⭐️ 8.0/10

Sebastian Raschka 发布了关于 Kimi K3 架构创新的详细分析，该模型移除了所有旋转位置嵌入（RoPE），转而采用无位置嵌入（NoPE），并引入了键值设计注意力（KDA）。 这项分析意义重大，因为 Kimi K3 的新颖方法挑战了位置嵌入对语言模型必要的传统观念，而 KDA 的线性注意力与细粒度门控可能实现更长的上下文窗口和更高的效率。 KDA 是一种门控线性注意力变体，通过逐通道衰减改进了 Gated DeltaNet，并以 3:1 的比例与全注意力层交错，最高可减少 75% 的 KV 缓存使用。

hackernews · ModelForge · 7月28日 15:48 · [社区讨论](https://news.ycombinator.com/item?id=49085698)

**背景**: NoPE 是一种完全省略位置嵌入的方法，依靠模型从上下文中推断令牌位置。Kimi K3 由 Moonshot AI 开发，是一个开放权重的 LLM，具有 100 万 token 的上下文长度。KDA（Kimi Delta Attention）是一种为高效长上下文处理而设计的线性注意力机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/andrewdalpino/NoPE-GPT">GitHub - andrewdalpino/NoPE-GPT: A GPT-style small language model (SLM) with no positional embeddings (NoPE). · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2510.26692">[2510.26692] Kimi Linear: An Expressive, Efficient Attention ... Kimi Delta Attention (KDA): algorithm, pseudocode, flow ... Kimi K3 Technical Advancements Explained - nextbigfuture.com Kimi Linear: Expressive &amp; Efficient Attention KDA (Kimi Delta Attention) | fla-org/flash-linear-attention ...</a></li>
<li><a href="https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html">Kimi K 3 Architecture Notes | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**社区讨论**: 社区评论积极且充满好奇：一些人对 NoPE 的有效性表示惊讶，而另一些人则称赞 Raschka 的详细分析，并指出 Kimi K3 的新颖架构驳斥了其仅仅是蒸馏攻击的说法。

**标签**: `#LLM architecture`, `#NoPE`, `#Kimi K3`, `#deep learning`, `#positional embeddings`

---

<a id="item-3"></a>
## [OpenAI 开源 Codex Security 命令行安全扫描器](https://github.com/openai/codex-security) ⭐️ 7.0/10

OpenAI 已将 Codex Security 开源，这是一个基于命令行的安全扫描器，利用人工智能识别和修复代码仓库中的漏洞。该工具之前作为插件可用，现已在 GitHub 上公开发布。 此次发布使 AI 驱动的安全扫描工具得以更广泛地使用，但早期用户反馈的长运行时间和高 API 使用量引发了实际担忧。同时也凸显了关于 AI 公司提供安全工具潜在利益冲突的持续争论。 用户报告称，即使扫描小型代码仓库也可能耗时近一个小时，并消耗 Pro 计划一半的周 API 配额。该工具依赖英文的“技能定义”来指导大语言模型，而 OpenAI 拥有优化这些提示的计算资源。

hackernews · bakigul · 7月28日 20:52 · [社区讨论](https://news.ycombinator.com/item?id=49089755)

**背景**: Codex 是 OpenAI 于 2025 年 4 月发布的 AI 编程代理，用于协助编写和修复代码等软件工程任务。Codex Security 于 2026 年 3 月推出，是一个应用安全代理，通过构建威胁模型和扫描仓库历史来识别并修复漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Codex_Security">Codex Security</a></li>
<li><a href="https://help.openai.com/en/articles/20001107-codex-security">Codex Security | OpenAI Help Center</a></li>

</ul>
</details>

**社区讨论**: 社区反馈褒贬不一：一些用户报告运行时间极长且 API 成本高，另一些用户则指出开源技能定义的价值。也存在怀疑声音，有评论者将 AI 安全工具比作‘纵火犯管理的消防队’。

**标签**: `#security`, `#open-source`, `#AI tools`, `#code analysis`, `#OpenAI`

---

<a id="item-4"></a>
## [欧盟人工智能法案合规检查清单发布](https://news.google.com/rss/articles/CBMipwFBVV95cUxNczhEdzFiM3ExdEdzOU1YZXFJbnNNUnNPMC1KRVdCS3dwV1htcVRad2NROTN1bGxybHdjam4xZUk4dWlNaHN0bjhHa2l3X0tJWlozWlU4X0JTT0pseGx0NFJ6eFpwNzZRTEZ5YzlfSGZqQkJFVVpBbmNDcWpxalFUbjNvZXlETmE5TXBmTlFmTjNXNFdGbWlxU29iRkt3RnpvS0w0TWN5MA?oc=5) ⭐️ 7.0/10

Security Boulevard 发布了一份包含 10 个步骤的合规检查清单，旨在帮助组织避免因违反《欧盟人工智能法案》而遭受高额处罚。 该清单为企业提供了应对《欧盟人工智能法案》复杂要求的实用指南，有助于避免巨额罚款和法律后果。 该清单涵盖了风险分类、透明度义务和治理结构等关键合规领域，与法案基于风险的框架保持一致。

rss · GoogleNews-欧盟监管 · 7月28日 08:02

**背景**: 《欧盟人工智能法案》于 2024 年 8 月 1 日生效，是全球首部全面的人工智能法规，根据风险等级（不可接受、高风险、有限风险、最小风险）对 AI 系统进行分类。该法案对提供者和使用者施加义务，违规将受到处罚，并且具有域外效力，适用于拥有欧盟用户的实体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe ’s digital future</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#AI governance`

---