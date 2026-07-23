---
layout: default
title: "Horizon Summary: 2026-07-23 (ZH)"
date: 2026-07-23
lang: zh
---

> 从 24 条内容中筛选出 11 条重要资讯。

---

1. [陶哲轩用 ChatGPT 探索雅可比猜想反例](#item-1) ⭐️ 9.0/10
2. [GigaToken：语言模型分词速度提升约 1000 倍](#item-2) ⭐️ 8.0/10
3. [Bento 将整个 PPT 打包成一个离线的单一 HTML 文件](#item-3) ⭐️ 8.0/10
4. [AI 实验室 SVG 生成偏见：自行车上的鹈鹕总朝右](#item-4) ⭐️ 8.0/10
5. [科技记者约翰·C·德沃夏克去世，享年 78 岁](#item-5) ⭐️ 7.0/10
6. [使用 LLM 算不算&\#x27;创造&\#x27;？](#item-6) ⭐️ 7.0/10
7. [初创公司的 PostgreSQL 生存指南](#item-7) ⭐️ 7.0/10
8. [欧盟 AI 法案 2026：主要变更与部署者义务](#item-8) ⭐️ 7.0/10
9. [欧盟人工智能法案第 50 条合规检查表现已发布](#item-9) ⭐️ 7.0/10
10. [法国禁止 15 岁以下未成年人使用社交媒体但削弱执法机制](#item-10) ⭐️ 6.0/10
11. [欧盟 AI 透明度规则于 8 月 2 日对德国企业生效](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [陶哲轩用 ChatGPT 探索雅可比猜想反例](https://chatgpt.com/share/6a5fdc7a-d6f8-83e8-bbea-8deb42cfed56) ⭐️ 9.0/10

著名数学家陶哲轩发布了一段与 ChatGPT 的对话，在其中他协作探索了雅可比猜想的一个最新反例，利用 AI 分析多项式映射并验证相关性质。 这表明顶尖数学家可以利用大语言模型作为主动研究助手，可能加速纯数学中的发现与验证过程。 该反例最初由数学家 Levent Alpöge 于 2026 年 7 月 19 日使用 Anthropic 的 Claude Fable 5 模型发现并展示；陶哲轩的对话侧重于理解这一三维空间显式反例的结构与含义。

hackernews · gmays · 7月22日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=49010345)

**背景**: 雅可比猜想是代数几何中长期未决的问题，认为具有非零常数雅可比行列式的多项式映射必然有多项式逆。该猜想已悬而未决超过一个世纪，期间出现大量错误证明。最近的反例推翻了维度大于 2 时的猜想，但二维情况仍未解决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jacobian_conjecture">Jacobian conjecture</a></li>

</ul>
</details>

**社区讨论**: 评论者们对陶哲轩精准提问如何从 ChatGPT 中提取深层见解感到着迷，指出没有他的专业知识，相同提示无法产生如此结果。一些人强调这与他们自己使用 AI 的模式相似，另一些人则欣赏对话的结构化递进。

**标签**: `#AI`, `#mathematics`, `#LLM`, `#research`, `#Jacobian conjecture`

---

<a id="item-2"></a>
## [GigaToken：语言模型分词速度提升约 1000 倍](https://github.com/marcelroed/gigatoken/) ⭐️ 8.0/10

GigaToken 是一个新的分词库，通过利用 SIMD 指令和优化的预分词映射缓存，实现了相比传统分词器约 1000 倍的速度提升。 这一加速显著降低了大型语言模型离线数据准备和预训练的时间和成本，在处理 TB 级文本时能实现更快的迭代周期。 GigaToken 支持广泛的 CPU 硬件（现代 x86 和 ARM）以及几乎所有常用的分词器，其优化重点在于通常由正则引擎处理的预分词阶段。

hackernews · syrusakbary · 7月22日 17:20 · [社区讨论](https://news.ycombinator.com/item?id=49010167)

**背景**: 分词是将文本转换为语言模型可以处理的子词单元（token）的过程。在推理时间中通常只占很小比例（低于 0.1%），但在预处理大型训练数据集时可能成为显著瓶颈。SIMD（单指令多数据流）是一种并行计算技术，允许处理器同时对多个数据点执行相同操作，GigaToken 利用它来加速基于正则表达式的预分词步骤。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/marcelroed/gigatoken">marcelroed/gigatoken: Language model tokenization at GB/s - GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49010167">GigaToken: ~1000x faster Language model tokenization | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区对其性能声称印象深刻，有评论称其“令人难以置信”。但也有观点指出分词在推理中占比很小，因此该工具的价值更多体现在离线数据准备上。作者澄清优化在不同 CPU 和分词器上表现一致，并非针对特定配置过度优化。

**标签**: `#tokenization`, `#performance`, `#LLM`, `#SIMD`, `#optimization`

---

<a id="item-3"></a>
## [Bento 将整个 PPT 打包成一个离线的单一 HTML 文件](https://bento.page/slides/) ⭐️ 8.0/10

Bento 是一款新工具，它将完整的演示文稿编辑器、查看器、数据和协作功能打包成一个自包含的 HTML 文件，完全离线工作，无需服务器或云登录。 这种方法消除了对云依赖和互联网连接的需求，使演示文稿的分享、编辑和协作变得简单——只需发送一个文件。这与重视简洁和离线优先工具的开发者产生共鸣。 默认幻灯片约 560KB，使用 reveal.js 和自研库；应用逻辑存储在一个 base64 blob 中，通过浏览器的 DecompressionStream 解压。协作通过加密的盲中继实现，该中继无法看到数据。

hackernews · starfallg · 7月22日 15:19 · [社区讨论](https://news.ycombinator.com/item?id=49008211)

**背景**: 传统的演示工具如 PowerPoint 或 Google Slides 需要安装或云连接。单文件 Web 应用将整个应用打包到一个 HTML 文件中，使其能在任何浏览器中离线运行。Reveal.js 是一个流行的 HTML 演示框架，盲中继技术则实现端到端加密数据传输，中继无法访问内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blinding_%28cryptography%29">Blinding (cryptography) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 创建者解释了文件结构（JSON 数据加 base64 编码的应用逻辑），许多评论者赞赏这一概念，部分人指出在高并发编辑时可能出现性能问题，例如在留言簿演示中 M1 Mac 出现卡顿。

**标签**: `#web tool`, `#presentation`, `#single-file app`, `#collaboration`, `#offline`

---

<a id="item-4"></a>
## [AI 实验室 SVG 生成偏见：自行车上的鹈鹕总朝右](https://dylancastillo.co/posts/pelicanmaxxing.html) ⭐️ 8.0/10

Dylan Castillo 在 7 个 AI 实验室和 48 种动物-交通工具组合中系统生成了 1008 张 SVG，发现所有 21 张自行车上的鹈鹕图像均朝右，这一独特偏见在其他组合中未出现。 这种偏见暗示了潜在的训练数据污染或系统性策划，引发了对 AI 基准测试可靠性及模型评估完整性的担忧。 分析涵盖 OpenAI、Google 和 Anthropic 等 7 个实验室，共生成 1008 张 SVG，其中 60%的图像朝右，但只有鹈鹕自行车组合在所有实验室中 100%朝右。

hackernews · dcastm · 7月22日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=49010129)

**背景**: 训练数据污染是指评估数据泄露到训练集中，导致性能指标虚高。AI 模型通过文本提示生成 SVG 矢量图形。本研究通过测试不寻常的组合，检测模型是否针对某些概念进行了专门训练。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.holisticai.com/blog/overview-of-data-contamination">An Overview of Data Contamination: The Causes, Risks, Signs, and Defenses</a></li>
<li><a href="https://www.svggenie.com/blog/ai-svg-generator-comparison-2025">Best AI SVG Generators in 2026: 7 Tools Tested Head-to-Head</a></li>

</ul>
</details>

**社区讨论**: 评论强调了方法论的严谨性，并讨论了实验室在特定基准测试上作弊的可能性。用户还注意到其他偏见，如海獭被正确描绘在飞机上，这可能表明针对热门示例进行了定向训练。

**标签**: `#AI`, `#image generation`, `#SVGs`, `#training data`, `#ML`

---

<a id="item-5"></a>
## [科技记者约翰·C·德沃夏克去世，享年 78 岁](https://twitter.com/na_announce/status/2079952538040672302) ⭐️ 7.0/10

著名科技记者约翰·C·德沃夏克去世，他以其尖锐的专栏文章在《个人电脑杂志》长期任职以及频繁参与 TWiT 播客而闻名。消息于 2026 年 3 月 8 日通过社交媒体和社区论坛发布。 德沃夏克是科技新闻界的标志性人物，影响了数代读者和评论员。他的去世标志着计算媒体一个时代的终结，促使人们反思科技报道的演变。 德沃夏克是德沃夏克键盘布局发明者奥古斯特·德沃夏克的侄子。他曾为《信息世界》和《MacUser》等刊物撰稿，并经常参与播客《No Agenda》和《本周科技》（TWiT），直到与主持人 Leo Laporte 关系破裂。

hackernews · coleca · 7月22日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49012070)

**背景**: 约翰·C·德沃夏克（1946-2026）是一位资深科技记者，职业生涯从 1980 年代持续到 2020 年代。他以对科技行业的逆向思考和幽默评论而闻名。他在《个人电脑杂志》等媒体的专栏广受欢迎，后来成为播客界的常客，与 Adam Curry 共同主持《No Agenda》等节目。尽管存在争议和分歧，他始终是科技评论界受人尊敬的声音。

**社区讨论**: 社区表达了深深的敬意和怀旧之情，许多人回忆起德沃夏克的大胆观点以及 80、90 年代阅读他专栏的乐趣。评论者强调了他从软件包装盒猜功能的技巧，以及与 Leo Laporte 的幽默互动。有人提到他与 Laporte 的分歧以及 Adam Curry 的宗教转向，但总体语气是对他持久影响的赞赏。

**标签**: `#John C. Dvorak`, `#tech journalism`, `#obituary`, `#PC Magazine`, `#TWiT`

---

<a id="item-6"></a>
## [使用 LLM 算不算&\#x27;创造&\#x27;？](https://beej.us/blog/data/ai-making/) ⭐️ 7.0/10

Beej 在其网站上发布了一篇博客文章，思考使用大语言模型（LLM）生成作品是否算作&\#x27;创造&\#x27;，这篇帖子在 Hacker News 上引发了超过 250 个点赞和 100 条评论的热烈讨论。 这场辩论触及了关于创造力、作者身份以及人类努力价值的核心问题——在 AI 能生成代码、艺术和文本的时代尤为重要。它迫使软件工程师、艺术家以及所有使用 AI 工具进行创作的人重新思考什么才算是真正的创造。 作者将使用 LLM 比作聘请园艺师：即使你没有亲自动手，你仍然为结果感到自豪。一位评论者区分了&\#x27;创造&\#x27;的标准，即一个人能在多大程度上推理输入变化如何影响输出，从而划清了&\#x27;做&\#x27;与&\#x27;要求别人做&\#x27;的界限。

hackernews · erikschoster · 7月22日 15:33 · [社区讨论](https://news.ycombinator.com/item?id=49008440)

**背景**: 大语言模型（LLM）如 GPT-4 是经过大量文本数据训练的人工智能系统，能够理解和生成人类语言。它们可以生成代码、文章和创意作品，这引发了长期存在的哲学问题：机器是否具有创造力，以及 AI 生成的输出能否被视为原创或真正的创造性作品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What Are Large Language Models (LLMs)? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人对借助 LLM 的创作感到自豪，视其为普通工具；而另一些人则怀念亲手创造的乐趣，担心失去人类智慧。一个引人注目的观点是，因果推理能力区分了真正的创造与仅仅通过提示生成。

**标签**: `#AI`, `#LLM`, `#software engineering`, `#philosophy of making`, `#creativity`

---

<a id="item-7"></a>
## [初创公司的 PostgreSQL 生存指南](https://hatchet.run/blog/postgres-survival-guide) ⭐️ 7.0/10

一篇题为《初创公司的 PostgreSQL 生存指南》的实用博文在 Hatchet 上发布，涵盖了初创公司使用 PostgreSQL 的常见陷阱和最佳实践。 该指南针对索引、清理和 ORM 使用等常见问题，对初创公司尤其重要，可提升数据库性能与可靠性。 指南强调使用 UUIDv7 而非 UUIDv4、避免 ORM、采用仅追加模式等实践，但社区指出其未提及备份策略。

hackernews · abelanger · 7月22日 12:36 · [社区讨论](https://news.ycombinator.com/item?id=49005787)

**背景**: PostgreSQL 是一个功能强大的开源关系型数据库，常被初创公司使用。常见挑战包括通过索引和清理进行性能调优，以及避免死锁和表膨胀等陷阱。正确的索引策略和定期自动清理配置对维持性能至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mydbops.com/blog/postgresql-indexing-best-practices-guide">PostgreSQL Index Best Practices for Faster Queries | Mydbops</a></li>
<li><a href="https://www.enterprisedb.com/blog/postgresql-vacuum-and-analyze-best-practice-tips">PostgreSQL VACUUM Guide and Best Practices | EDB</a></li>

</ul>
</details>

**社区讨论**: 评论者建议补充备份策略、使用 UUIDv7、避免 ORM。有人警告不要使用级联删除，并建议确定性锁排序。整体情绪积极，但提出了实用修正。

**标签**: `#PostgreSQL`, `#startup`, `#database`, `#best-practices`

---

<a id="item-8"></a>
## [欧盟 AI 法案 2026：主要变更与部署者义务](https://news.google.com/rss/articles/CBMixAFBVV95cUxQZVJ1NDNlbXIyWDBLeUVRSDFSVXkyMWlhZ0FSV1NwR1cxWlJDZExVakp0TzhsTXhhZ3RhV0MzaHpKOTA4cWU2c3lXRDM5RlNLcHlhcy05WjZUd2NCWUhYSWJNUEMzQkc2MnZteVkzaFM4aFF0RmJCc0JPSE1xTTZoXzI1UHRaa2NPR0toWk9SUVdhUUF1c1MzSTNEUEltUERXLXY3Q1dPYVBqYXZsWEd6T3N6alA3WkhkT2k4Tkg2ZFJURU5K0gHEAUFVX3lxTFBlUnU0M2VtcjJYMEt5RVFIMVJVeTIxaWFnQVJXU3BHVzFaUkNkTFVqSnRPOGxNeGFndGFXQzNoeko5MDhxZTZzeVdEMzlGU0tweWFzLTlaNlR3Y0JZSFhJYk1QQzNCRzYydm15WTNoUzhoUXRGYkJzQk9ITXFNNmhfMjVQdFprY09HS2haT1JRV2FRQXVzUzNJM0RQSW1QRFctdjdDV09hUGphdmxYR3pPc3pqUDdaSGRPaThOSDZkUlRFTko?oc=5) ⭐️ 7.0/10

Process Excellence Network 发表的一篇文章概述了 2026 年生效的欧盟 AI 法案的主要变化，并总结了高风险 AI 系统部署者仍需履行的义务。 这一更新对在欧盟部署 AI 的组织至关重要，因为它明确了不断变化的合规要求，并强调部署者仍需遵守人工监督和数据保护义务。 高风险 AI 系统的部署者必须利用提供者提供的信息进行数据保护影响评估并实施人工监督措施，且这些义务不影响其他国家法律的要求。

rss · GoogleNews-欧盟监管 · 7月22日 10:17

**背景**: 欧盟 AI 法案是一个全面的法律框架，根据风险级别对 AI 系统进行监管。高风险 AI 系统（如用于关键基础设施或就业的系统）面临严格的要求，包括透明度、准确性和人工监督。部署者是指以专业身份使用此类系统的实体，负责遵守特定的运营义务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-26">AI Act Service Desk - Article 26: Obligations of deployers of ...</a></li>
<li><a href="https://artificialintelligenceact.eu/article/26/">Article 26: Obligations of Deployers of High-Risk AI Systems</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#deployers`

---

<a id="item-9"></a>
## [欧盟人工智能法案第 50 条合规检查表现已发布](https://news.google.com/rss/articles/CBMipgFBVV95cUxPUVlzdHc5cC1ZM1VHeXNIbWJWMEMtbVdBamE4cnRjUmpWY2dzR2lVX2V1el9ORGFhVnhtR1dJSEx6ZzhPTHhqdjFUWjlFLWJkdGRMZXRwaG9sMHljMmxPZVNWb2pLdmZic1Y0WFFQSXRfeU9WcTlNS09YOWtiVnBPemwwZjZLblNfTnlPa1RzZzYwWE9EVko1UFl4RHJDQUsySGJJWDhB?oc=5) ⭐️ 7.0/10

Resemble AI 发布了针对欧盟人工智能法案第 50 条的合规检查表，面向提供者和部署者。该检查表详细说明了与人类互动或生成合成内容的人工智能系统的透明度义务。 该检查表帮助人工智能相关方为 2026 年 8 月 2 日生效的第 50 条做好准备，避免高达 1500 万欧元或全球年营业额 3%的罚款。它还明确了提供者和部署者在欧盟人工智能法案下的不同责任。 第 50 条的透明度义务将于 2026 年 8 月 2 日生效，实施守则预计于 2026 年 6 月完成。根据法案第 99 条第 4 款\(g\)项，不遵守规定可能导致重大经济处罚。

rss · GoogleNews-欧盟监管 · 7月22日 18:01

**背景**: 欧盟人工智能法案于 2024 年 8 月 1 日生效，并分阶段实施。第 50 条对与人类互动、生成合成内容或使用情感识别的人工智能系统提出了透明度要求。提供者负责设计人工智能系统，承担最重的合规负担，而部署者（使用者）的义务较少。该检查表是帮助双方满足这些要求的实用工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gdprlocal.com/eu-ai-act-article-50/">EU AI Act Article 50 : Transparency Rules for Businesses - GDPR Local</a></li>
<li><a href="https://humantext.pro/blog/eu-ai-act-article-50-explained">EU AI Act Article 50 Explained: Practical Compliance</a></li>
<li><a href="https://www.aoshearman.com/en/insights/ao-shearman-on-tech/zooming-in-on-ai-4-what-is-the-interplay-between-deployers-and-providers-in-the-eu-ai-act">EU AI Act: roles of providers and deployers explained</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#compliance`, `#regulation`, `#AI governance`

---

<a id="item-10"></a>
## [法国禁止 15 岁以下未成年人使用社交媒体但削弱执法机制](https://news.google.com/rss/articles/CBMitgFBVV95cUxNTlByMm9GLXdMaXRaQXdGXzY5R25tUDlld3YyUk1uZkFrODhEdXZIcGV3Znp0dlNKVTlyM1hyVlo3Ymo1QWw5dDFUVEM3SWxqTGhfSG15cEVBdjFJSVB0NkVLTDRFbFFVSVpJc1gwUi1KekdtMEdJb0swejNvY3RmeEQxV3doMDVHcXdBczNfeEtLcHdpaHFucmhHeFphRFlpQW5RYWc1T0JNd0lpRjlNOTJuT1ZMdw?oc=5) ⭐️ 6.0/10

法国通过了一项法律，禁止 15 岁以下儿童使用社交媒体，但执法机制被大幅削弱，降低了该法律的直接影响。 这项法律是儿童在线安全领域的重要监管举措，但缺乏强有力的执法可能为其他考虑类似措施的国家树立先例。 该法律要求社交媒体平台验证用户年龄并为 15 岁以下未成年人获取家长同意，但执法机制（如罚款或技术检查）被删除，使得合规在很大程度上成为自愿行为。

rss · GoogleNews-欧盟监管 · 7月22日 18:18

**背景**: 法国一直积极监管数字平台以保护未成年人，之前的提案包括强制年龄验证和家长控制。这项法律是欧洲更严格的在线安全监管趋势的一部分，但实际执法挑战常导致妥协。削弱执法机制反映了儿童保护目标与行业可行性担忧之间的紧张关系。

**标签**: `#social media`, `#regulation`, `#France`, `#online safety`, `#policy`

---

<a id="item-11"></a>
## [欧盟 AI 透明度规则于 8 月 2 日对德国企业生效](https://news.google.com/rss/articles/CBMiyAFBVV95cUxQaTlRMnl5Tm1ob0NxelctSTdhcGdIRElFaUZMNmRmcWlJWHNUUFlGLWlFRFptd3lvRmRTUVVQRHJJSmVvY09nS2M4cDJpSFJYR1M5dWpjMlNPWFZmOFVLbHhKclZoaE1od2xRYTJnLVpWRUtWb0hlUDJOZWN2enA1X0duUmZPNC1yTXhlU2JxNWV0ajdjQUJ0T1pDQWZ3bHFJQlhuUGZFZG1wWXFUbTJlME9xQnVhd3p4eGc0ZVBrNHVoc3Q4MnEzOA?oc=5) ⭐️ 6.0/10

德国企业必须在 2026 年 8 月 2 日前遵守新的欧盟 AI 透明度规则，因为《欧盟 AI 法案》第 50 条对新的 AI 系统生效。 这一截止日期标志着《欧盟 AI 法案》下首批可执行的透明度义务，要求公司标注 AI 生成内容并告知用户何时与 AI 系统互动，影响广泛的企业。 在 8 月 2 日之前发布的系统可在 2026 年 12 月 2 日前合规，这些义务广泛适用于与人类互动、生成深度伪造或提供情绪识别的 AI 系统。

rss · GoogleNews-欧盟监管 · 7月22日 18:43

**背景**: 《欧盟 AI 法案》于 2024 年 8 月颁布，是首部全面的 AI 法规。第 50 条要求对低风险 AI 系统（如聊天机器人和内容生成器）进行透明度标注，而高风险系统则有更严格的要求。8 月 2 日的截止日期专门针对在该日期之后投放市场的新系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialintelligenceact.eu/transparency-rules-article-50/">The EU AI Act’s Transparency Rules: A Practical Guide to ...</a></li>
<li><a href="https://www.theregister.com/ai-and-ml/2026/07/20/eus-ai-labeling-rules-take-effect-next-month/5274917">EU &#x27;s AI labeling rules take effect next month</a></li>
<li><a href="https://www.euractiv.com/news/how-eu-ai-transparency-rules-will-change-what-you-see-online/">How EU AI transparency rules will change what you see... | Euractiv</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#AI transparency`, `#compliance`, `#Germany`

---