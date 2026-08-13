---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 17 条内容中筛选出 6 条重要资讯。

---

1. [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，推理速度提升近 7 倍](#item-1) ⭐️ 9.0/10
2. [DRAM 加扰漏洞：新型工具可解锁 CPU 受保护内存](#item-2) ⭐️ 9.0/10
3. [谷歌推出 Gemini 3.7 Flash，一款经济高效的主力 AI 模型](#item-3) ⭐️ 8.0/10
4. [DeepSeek 发布开源智能体运行框架，支持会话追踪](#item-4) ⭐️ 8.0/10
5. [欧盟 AI 法案要求聊天机器人披露非人类身份](#item-5) ⭐️ 7.0/10
6. [8 月 26 日 Shopify 结账升级前请测试转化跟踪](#item-6) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，推理速度提升近 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 9.0/10

OpenAI 与 Cerebras 联合发布 GPT-5.6 Sol Ultrafast，这是运行在 Cerebras 晶圆级硬件上的新服务层级。它在 11 小时 11 分钟内回答了全部 2500 道 HLE 基准题，比 Claude Fable 5 的 78 小时 27 分钟快了近 7 倍；在 OpenAI API 中最高可比标准处理快 14 倍。 这标志着前沿 AI 推理速度的一个重要里程碑：法律文书、金融建模、工程报告等具有经济价值的知识工作现在可以在数小时而非数天内完成，且不牺牲准确性。这表明像 Cerebras 晶圆级引擎这样的专用芯片能够切实改变最严苛推理模型在成本与延迟上的权衡。 在经济价值知识工作基准 GDP-Val 上，Ultrafast 实现了 5.6 倍的端到端加速且无质量下降。该服务首先在 OpenAI API 中推出；定价和全面开放时间尚未公布，部分社区成员指出 OpenAI 与 Cerebras 并未明确确认 Ultrafast 的输出与标准 GPT-5.6 Sol 完全一致。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Cerebras 制造晶圆级引擎（WSE-3），这是全球最大的 AI 处理器——单芯片包含 4 万亿个晶体管、90 万个面向 AI 优化的核心以及 44GB 片上 SRAM，可提供超过 21 PB/s 的内存带宽。HLE 和 GDP-Val 是前沿推理基准，用于评测模型在专家级、开放式知识工作上的表现，即便是最好的模型也往往得分很低。此次发布紧随 2026 年 7 月 GPT-5.6 的发布，凸显专用推理硬件正成为大语言模型生态中越来越重要的一环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai">Accelerating GPT-5.6 Sol Ultrafast with OpenAI</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode: GPT-5.6 Sol at up to 14X the speed | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体热烈——有评论者称 7 倍加速“令人惊叹”，并希望它能尽快向公众开放、未来能在消费级硬件上本地运行；但也存在明显的质疑。例如 Topfi 指出 OpenAI 和 Cerebras 都没有明确表态 Ultrafast 与标准 GPT-5.6 Sol 质量完全一致；csallen 认为速度本身就会提升思考质量，因为更快的推理能支持类似人类的反复迭代与修改；GodelNumbering 则注意到 OpenAI 公告中缺少定价信息。

**标签**: `#AI`, `#LLM`, `#OpenAI`, `#Cerebras`, `#Performance`

---

<a id="item-2"></a>
## [DRAM 加扰漏洞：新型工具可解锁 CPU 受保护内存](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

安全研究员 Christopher Domas 发布了工具 &\#x27;skitter-creek-bath-salts&\#x27;，它利用 DRAM 寻址和行语义，逆向工程 AMD Jaguar（AMD16h）CPU 上未公开的地址加扰机制。通过 z3 求解器，它生成“意大利面化”的别名地址，从而访问 PSP 私有内存、SMRAM 和 C6 空闲状态等受保护内存。 这件事很重要，因为它将 ring-0 权限转化为绕过平台精心构建的内存栅栏与安全检查的能力，暴露了通常连特权软件都看不到的区域。它挑战了“DRAM 地址加扰可以作为基于模糊性的安全边界”这一假设，对游戏主机及其他 AMD 系统可能产生重大影响。 目前的概念验证针对 2013 年的 AMD16h（Jaguar）家族；README 指出 Zen 3 的内存控制器寄存器基地址不同，因此该攻击无法直接迁移。该工具利用 z3 将相干视图中的任意地址转换为加扰视图中的别名地址，从而绕过锁和栅栏而不触发平台安全检查。

hackernews · matt\_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 以行（row）和列（column）组织，而现代内存控制器会应用未公开的“加扰”函数，隐藏物理地址到实际 DRAM 单元（行、列、Bank、Bank Group）的映射。这种加扰通常对软件不可见，平台还将其作为安全机制的一部分。项目名称借用了天体物理学中的“意大利面化”（spaghettification），但这里指的是把正常的相干内存视图扭曲成加扰后的视图。一旦加扰变换被解开，就可以通过一个不受控的别名地址访问受保护的目标地址，从而解锁从 PSP 私有内存到 SMRAM 的各类区域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49286341">Spaghettifying DRAM | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spaghettification">Spaghettification - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区反响热烈，许多用户赞赏这项研究并期待 Black Hat 演讲，还有人推荐 Christopher Domas 以往的演讲。有评论指出，DRAM 已经变得如此复杂，存在巨大攻击面并不令人意外，Xbox 和 PlayStation 的安全团队应当感到紧张。也有用户追问该攻击实际影响哪些较新的 CPU，并指出 AMD Jaguar 是 2013 年的架构，Zen 3 的内存控制器基地址已经不同。

**标签**: `#DRAM`, `#hardware security`, `#reverse engineering`, `#exploit`, `#security research`

---

<a id="item-3"></a>
## [谷歌推出 Gemini 3.7 Flash，一款经济高效的主力 AI 模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

谷歌发布了 Gemini 3.7 Flash，这是其 Flash 系列中一款新的高性价比模型，基于 Gemini 3.6 Flash 构建，并被描述为“最智能的主力模型”。从今天起，它将为 Gemini Spark 提供支持，供 Google AI Pro 和 Ultra 订阅者在超过 160 个国家和地区使用。 此次发布通过瞄准低成本、高吞吐量工作负载，增强了谷歌在快速发展的 AI 模型市场中的竞争力。开发者和企业在将价格和性能与 OpenAI 的 GPT-5.6 Luna 以及 Anthropic 的 Opus 等竞品进行比较时，将直接受到影响。 该模型采用“首发定价”，计划在 2026 年底上调一倍；从 2027 年 1 月 1 日起，输入 token 价格为每百万个 1.50 美元，输出 token 价格为每百万个 7.50 美元。社区测试显示其视觉转 HTML 能力出色，但也指出 Flash 系列更新节奏过快——3.6 Flash 仅在三周前发布。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**背景**: Gemini 是 Google DeepMind 开发的多模态大语言模型系列，于 2023 年 12 月 6 日首次发布，也是 Gemini 聊天机器人的底层技术。Flash 系列旨在提供更小、更快、更便宜的一档模型，适用于高吞吐、以文本为主和智能体场景，与更大的旗舰模型形成互补。谷歌表示，Gemini 3.7 Flash 在其前代 3.6 Flash 的基础上有所改进，模型卡也将 3.6 Flash 列为其基础模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3 . 7 Flash : our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3 . 7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_2.5_Flash_Image">Gemini 2.5 Flash Image</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人称赞该模型的视觉转 HTML 质量和性价比，一位测试者称 Opus 仍是同类最佳，但 Gemini 3.7“在与价格相近的 LLM 对比中”表现出色。另一些人则批评定价方案和 Flash 的更新速度，并认为 OpenAI 的 GPT-5.6 Luna 在 DeepSWE 1.1 等基准测试中更便宜、更强，削弱了 Flash 的存在价值。

**标签**: `#AI`, `#Gemini`, `#Google`, `#Machine Learning`, `#Model Release`

---

<a id="item-4"></a>
## [DeepSeek 发布开源智能体运行框架，支持会话追踪](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek Harness 的早期开源开发者预览版，采用 MIT 许可证。它提供完整的会话追踪能力，包括追加式会话日志、回放、分叉、搜索和插件功能。 该版本为开发者提供了一个透明、可追踪的智能体运行框架，记录模型所看到的一切，这在加密或混淆追踪记录的美国专有模型中非常少见。开源 MIT 许可证和插件架构有望加速社区驱动的 AI 智能体工具发展。 该框架采用“一切皆插件”的架构，基于 Cordis v4，支持热重载以及插件的动态启用/销毁，包括 UI 组件和副作用清理。Trajectory 视图允许按来源检查记录，恢复、分叉、搜索和回放都基于同一事件流。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: 智能体运行框架（agent harness）是围绕大语言模型（LLM）的软件基础设施，使其能够作为智能体运行，管理工具使用、记忆、状态持久化以及反馈循环。由于 LLM 是无状态的且只输出文本，因此该框架对于多步骤、面向工具或长期运行的任务至关重要。会话追踪和回放是关键的观测能力，可帮助开发者调试和评估智能体行为；LangSmith 和 Telerik 等工具都强调追踪和回放完整智能体会话。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness</a></li>
<li><a href="https://www.truefoundry.com/blog/ai-agent-observability-tools">AI Agent Observability: Monitoring and Debugging Agent Workflows</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，作者之一 tianyicui 欢迎反馈并指出 MIT 许可的预览版会比较粗糙。SwellJoe 称赞追踪功能是“杀手级功能”，认为美国模型因加密追踪而不允许这样做；lxdlam 则对论文的价值给出较克制的评价。还有人表达了对“一切皆插件”架构的插件疲劳和怀疑，ef2k 则强调了底层 Cordis v4 的热重载能力。

**标签**: `#DeepSeek`, `#AI agents`, `#open-source`, `#traceability`, `#developer tools`

---

<a id="item-5"></a>
## [欧盟 AI 法案要求聊天机器人披露非人类身份](https://news.google.com/rss/articles/CBMilgFBVV95cUxQdnd1MFV1VkVBQTg0YTFfUTNNTzZ5NGRVSmpnOHZwcnphTXRqR1BpSnNObG9COXhvb0N1R0hleEJhQTdYRWFVcHFNNS1yYmo3TExNVmZUZVZyVUYtZmFZdHp5emFzVmdpRURsb09JNVo2bHlWckU0MV9GdUlZTTVvWWEyRC1WSGpwcHNYa1lOLVpmYXRyZXc?oc=5) ⭐️ 7.0/10

欧盟《人工智能法案》第 50 条的透明度义务要求聊天机器人的提供者和部署者明确告知用户他们正在与 AI 系统而非人类交互。该规则于 2026 年 8 月生效，而法案本身自 2024 年 8 月 1 日起已施行。 该规定几乎对所有面向欧盟客户的聊天机器人提出明确披露要求，影响全球范围内服务欧盟用户的开发者和企业。它为 AI 透明度设立了合规义务，可能在全球树立监管先例。 第 50 条的透明度义务适用于有限风险 AI 系统，而不仅限于高风险系统，因此即使仅面向客户的聊天机器人也会触发披露义务。该规则于 2026 年 8 月生效，为组织留出适应时间。

rss · GoogleNews-欧盟监管 · 8月13日 00:35

**背景**: 欧盟《人工智能法案》是一部综合性 AI 监管法规，于 2024 年 8 月 1 日生效，并将在后续 6 至 36 个月内逐步适用。该法案按风险等级对 AI 系统分类：不可接受、高风险、有限风险和最小风险，其中聊天机器人等有限风险系统仅需满足透明度义务，无需进行全面合格评定。该法案还具有域外效力，适用于在欧盟境内有用户的欧盟以外提供商。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://artificialintelligenceact.eu/transparency-rules-article-50/">The EU AI Act’s Transparency Rules: A Practical Guide to Article 50 | EU Artificial Intelligence Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe&#x27;s digital future - European Union</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#regulation`, `#chatbot`, `#transparency`, `#AI policy`

---

<a id="item-6"></a>
## [8 月 26 日 Shopify 结账升级前请测试转化跟踪](https://www.reddit.com/r/ecommerce/comments/1vnllmz/before_shopifys_aug_26_checkout_upgrade_test_one/) ⭐️ 7.0/10

Shopify 提醒非 Plus 商店的商家在 8 月 26 日感谢页和订单状态页升级前，进行一次完整的测试订单，以确认 Meta、GA4、Google Ads 等转化平台能正确收到购买事件。 这次升级可能悄无声息地破坏转化跟踪，导致广告主无法了解哪些广告带来了销售，影响广告优化。现在测试让商家有时间解决问题，避免升级后收入损失。 测试包括下测试订单、在浏览器 Network 标签或服务器日志中观察购买请求，并在 Meta 的 Test Events 或 GA4 的 DebugView 中确认事件。商家应记录事件的价值、货币、时间戳和订单/事件 ID，并在升级后再次测试。

reddit · r/ecommerce · /u/BTWigley · 8月13日 20:00

**背景**: Shopify 的感谢页和订单状态页是购买确认和跟踪脚本运行的地方。转化平台依靠这些页面触发购买事件，可以是客户端像素或服务端 API。GA4 的 DebugView 和 Meta 的 Test Events 是让营销人员实时查看平台收到事件的工具，有助于验证跟踪的准确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.jonloomer.com/how-to-test-meta-conversion-events/">How to Test Meta Conversion Events - Jon Loomer Digital</a></li>
<li><a href="https://www.conversios.io/blog/how-to-use-debugview-in-ga4/">How to Use DebugView in GA 4 : Step-by-Step Guide</a></li>
<li><a href="https://dev.to/codesphere/introduction-to-server-side-tracking-2pjc">Introduction to Server Side tracking - DEV Community</a></li>

</ul>
</details>

**标签**: `#Shopify`, `#E-commerce`, `#Conversion Tracking`, `#Analytics`, `#Checkout`

---