---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 23 条内容中筛选出 5 条重要资讯。

---

1. [新色彩空间与算法生成多样化且合理的肤色](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash 在单块 AMD MI300X 上跑出 150+ tokens/s](#item-2) ⭐️ 8.0/10
3. [欧盟 AI 法案执法阶段启动](#item-3) ⭐️ 8.0/10
4. [Mistral 发布 Shieldstral：3B 开源权重多模态审核模型](#item-4) ⭐️ 7.0/10
5. [欧盟人工智能法案：对您的组织意味着什么](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [新色彩空间与算法生成多样化且合理的肤色](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

作者提出了一种新的色彩空间和程序化生成算法，用于轻松创建多样化且合理的肤色，并附有交互式演示和深入讲解。该项目包含基于该色彩空间的取色器和程序化生成系统。 这对数字艺术家和游戏开发者意义重大，他们常常需要手动挑选合理的肤色。它也有助于更广泛的 AI 公平性讨论，因为大型多模态模型在准确识别和生成肤色方面仍然面临挑战。 该色彩空间通过采样真实肤色并手动拟合函数构建，而非使用 PCA 或 Oklab 等标准色彩空间。项目页面包含许多 JavaScript 演示，并在“未来工作”部分讨论了局限性和可能的改进。

hackernews · automatoney · 8月4日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=49170165)

**背景**: 色彩空间是一种用数字表示颜色的系统，例如 RGB 或 Oklab；肤色在这些空间中占据一个很小的新月形区域。要使单个色彩空间自然地捕捉人类肤色的全部多样性是很困难的，因为颜色感知取决于光照和许多其他因素。近期研究也表明，最先进的模型在准确识别和生成肤色方面仍然困难重重，因此这也是 AI 公平性中的一个活跃领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>
<li><a href="https://arxiv.org/html/2509.10980">TrueSkin: Towards Fair and Accurate Skin Tone Recognition and ...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持正面态度，称赞优雅的曲线拟合方法和交互式演示。一些人指出了与现有工作的联系，如 Pantone 肤色标准和基于 Oklab 的粉底色号分析；另一些人则质疑该模型是否覆盖了全部肤色范围，有评论者注意到生成的色块中出现了绿色、蓝色和紫色色调。

**标签**: `#color-space`, `#procedural-generation`, `#digital-art`, `#skin-tones`, `#algorithm`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 在单块 AMD MI300X 上跑出 150+ tokens/s](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

一个新的 GitHub 项目展示了在单块 AMD MI300X GPU 上运行 DeepSeek V4 Flash，在将上下文窗口缩减到 256k 的情况下实现了每秒超过 150 tokens 的生成速度。该仓库记录了具体实现，并公开讨论了所涉及的取舍。 在单个加速器上运行 284B 参数的 MoE 模型，使大模型推理变得更容易获得且更具成本效益，尤其是在 Nvidia 生态之外。这表明通过量化与上下文窗口的取舍，AMD 硬件同样能实现高 token 吞吐，打破了必须使用多卡或 Nvidia 方案的固有认知。 DeepSeek V4 Flash 总参数量为 284B、激活参数 13B，原生支持 100 万 token 的上下文，而该项目将其缩减至 256k。AMD MI300X 拥有 192GB HBM3 显存和 5.3TB/s 带宽，模型原生的 MXFP4 量化也使其能够放入单卡显存。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 是一个混合专家（MoE）大语言模型系列，包含 1.6T 参数的 Pro 版本和 284B 参数、面向快速高吞吐推理优化的 Flash 版本。AMD MI300X 是一款面向生成式 AI 与 HPC 负载的数据中心加速器，直接与 Nvidia 的数据中心 GPU 竞争。通常运行这种规模的模型需要多卡集群，而这个项目展示了通过接受上下文长度与性能权衡，单卡也能获得可用的效果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amd_MI300X">Amd MI300X</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上对该成果表示赞赏，指出 MI300X 的高 HBM 带宽非常适合此类工作负载，并引用了 HotAisle 快速入门和一篇 2xMI300X 博客等先前工作。也有人提出了实际注意事项：MI300X 是 OAM 模块而非 PCIe 卡，像 144GB 的 MI350P 等替代品也可能容纳该模型；还有用户提到 DwarfStar 可以在更小显存中运行同一模型。另一位评论者强调，把上下文从 100 万降到 256k 是非常实用的取舍，与 Codex 等模型处于同一水平。

**标签**: `#DeepSeek`, `#AMD MI300X`, `#LLM inference`, `#quantization`, `#hardware optimization`

---

<a id="item-3"></a>
## [欧盟 AI 法案执法阶段启动](https://news.google.com/rss/articles/CBMifEFVX3lxTE5TczVSWlJhQnJMWHBhXzROV1g2V1E5ZTRRcXdPQTNoTUlBbXotTmRvTklJWlYwTW5DUmFuWGR4UkJ4VzlfM2c4SmJNSm9LTXk0dXpHWGctbzFUY05TRVdzakdVU2FlRmdVY2ZzUnd3MUJOVktuMFVURE0xLXo?oc=5) ⭐️ 8.0/10

欧盟已开始执行《人工智能法案》，新的透明度和执法规则于 8 月 2 日生效。AI 开发者和部署者现在必须遵守这些新义务。 这标志着欧盟对 AI 开发和部署的监管进入重大里程碑，影响在欧盟运营或使用 AI 系统的公司。企业需落实合规措施，否则可能面临处罚，为全球 AI 治理树立先例。 该执法阶段涵盖 AI 系统的透明度要求，包括通用 AI 模型的义务，而高风险 AI 应用的更严格监管制度已被推迟至较晚日期。欧盟委员会于 8 月 2 日启动执法和监督活动。

rss · GoogleNews-欧盟监管 · 8月4日 07:30

**背景**: 欧盟《人工智能法案》是一项全面的 AI 监管法规，旨在确保 AI 系统安全并尊重基本权利。它采用基于风险的方法，根据 AI 系统带来的风险水平施加不同的义务。该法案分阶段实施，透明度要求现已生效，高风险规则尚未全面适用。

**标签**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#policy`

---

<a id="item-4"></a>
## [Mistral 发布 Shieldstral：3B 开源权重多模态审核模型](https://mistral.ai/news/shieldstral/) ⭐️ 7.0/10

Mistral 发布了 Shieldstral，一个紧凑的 3B 参数开源权重多模态审核模型。它可以对文本和图像输入进行提示词审核、响应审核、提示-响应对分类、拒答检测和安全过滤，并声称其性能优于高达其规模 7 倍的模型。 这为开发者提供了一种可行的、可自托管的替代方案，替代封闭的审核 API，降低了用户生成内容平台的成本和数据隐私门槛。这也反映了 Mistral 发布更小巧、经过微调的模型作为实用工具、而非与前沿模型正面竞争的策略。 Shieldstral 使用自然语言策略问题并返回是/否分类，因此可以在不重新训练的情况下调整策略。它可在 Hugging Face 上的 mistralai/Shieldstral-1.0-3B 获取，专为跨文本和图像的多模态审核而设计。

hackernews · riadsila · 8月4日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=49171268)

**背景**: 多模态内容审核是一种自动分析文本、图像、音频和视频以检测并移除违规内容的系统。开放权重模型公开提供模型权重，开发者可以自行部署和微调，而不必完全依赖付费 API。Mistral 一直发布像 Shieldstral 这样的专用模型，并通过 Hugging Face 向社区开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/shieldstral/">Introducing Shieldstral. | Mistral AI</a></li>
<li><a href="https://docs.mistral.ai/models/model-cards/shieldstral-1-0">Shieldstral 1.0 - docs.mistral.ai</a></li>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open - Weights Model ? | AI 21</a></li>

</ul>
</details>

**社区讨论**: HN 评论者对这个模型的灵活性很好奇，质疑它是否支持任意审核规则集，还是只能使用大型科技平台那种预设风格，并询问在不重新训练的情况下可调空间有多大。另一些人赞赏 Mistral 转向更小、更精细微调模型的方向，并认为该发布是一个成本效益高的第一道审核防线，可结合人工复核。评论中还与 OpenAI 的 omni-moderation API 进行了比较，并分享了 Hugging Face 链接。

**标签**: `#AI`, `#content moderation`, `#open-weights`, `#Mistral`, `#multimodal`

---

<a id="item-5"></a>
## [欧盟人工智能法案：对您的组织意味着什么](https://news.google.com/rss/articles/CBMikwFBVV95cUxPemo3U0xJYW51M2xBaFpDN1JLY3JkRThMaHFpSlZxQm5SU19zYmtsMlBtNTFqYmljVlg2WFJMTl9KWTJ1R3NySU9WbXdaNHJ5VkZ6U3NpdUZKZ1djdDU2QWhvNFZ2MjdiSFdzdG9ISEo1VGpRVVQ1b3hYeTAwNHhmdWNRYmk3QTg4c0NyODdoOTMzT00?oc=5) ⭐️ 6.0/10

欧盟人工智能法案已于 2024 年 8 月 1 日正式生效，information-age.com 的这篇文章探讨了其分阶段义务对使用或部署人工智能系统的组织意味着什么。 该法案是世界上第一部全面的 AI 监管法规，对 AI 提供者和专业使用者施加基于风险的义务，并具有域外效力。在欧盟运营的组织必须了解其合规义务，从对不可接受风险应用的全面禁止到有限风险系统的透明度要求。 该法案将 AI 应用分为四个风险等级——不可接受、高风险、有限风险、最小风险——另加一个通用 AI 类别。高风险系统需要合规性评估，各项规定在生效后的 6 至 36 个月内逐步实施。

rss · GoogleNews-欧盟监管 · 8月4日 15:03

**背景**: 欧盟人工智能法案是一部产品监管类法律，不创设个人权利，而是对提供者和专业使用者施加义务。该法案由欧盟委员会于 2021 年 4 月提出，受 ChatGPT 等生成式 AI 系统兴起的影响，并于 2024 年获批。它覆盖大多数行业，但豁免军事、国家安全、研究及非专业用途，并设立欧洲人工智能委员会以促进国家合作与合规。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://artificialintelligenceact.eu/high-level-summary/">High-level summary of the AI Act | EU Artificial Intelligence Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe&#x27;s digital future - European Union</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#policy`, `#technology law`

---