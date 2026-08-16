---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 9 条内容中筛选出 3 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词，供公众分析](#item-1) ⭐️ 8.0/10
2. [发展中国家嵌入式工程师为 RISC-V 低成本优势辩护](#item-2) ⭐️ 7.0/10
3. [Firefox for iOS 加入原生广告拦截器](#item-3) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词，供公众分析](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 已发布 Claude 系统提示词的官方版本说明，记录了 Opus 4.8 和 Opus 5 等模型中使用的确切提示词。该文档首次让公众得以追踪这些提示词在不同版本间的演变。 这种透明度使研究人员和开发者能够分析 Anthropic 如何塑造 Claude 的行为，可能为 AI 安全和治理讨论提供参考。Simon Willison 在社区中创建的 Git 历史进一步简化了对比分析。 版本说明涵盖了多个 Claude 版本的系统提示词，Simon Willison 将其重建为 Git 提交历史以便对比。值得注意的新增内容包括指示 Claude 自行检查上传图片的提示词，以及如何处理用户情绪危机的指引。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词（System Prompts）是引导大型语言模型行为的预定义指令，优先级高于用户输入，用于确保响应的一致性。Anthropic 公开这些提示词是前沿 AI 模型中罕见的透明度举措；随着监管者和企业要求可审计的 AI 输出，提示词版本管理正成为治理关注点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.21091">[2505.21091] Position is Power: System Prompts as a Mechanism of Bias in Large Language Models (LLMs)</a></li>
<li><a href="https://promptengineering.org/system-prompts-in-large-language-models/">System Prompts in Large Language Models</a></li>
<li><a href="https://webflow2.decagon.ai/glossary/what-is-prompt-versioning">What is prompt versioning ? | Decagon glossary | Decagon</a></li>

</ul>
</details>

**社区讨论**: 评论大体呈正面，Simon Willison 分享了他的 Git 提交历史以追踪提示词变化。部分用户对平台删除批评 AI 的报道表示担忧，另一些用户则分析具体提示词，质疑 Anthropic 自身的系统提示词是否意味着对模型推理能力的不信任。

**标签**: `#AI`, `#Claude`, `#LLM`, `#System Prompts`, `#Anthropic`

---

<a id="item-2"></a>
## [发展中国家嵌入式工程师为 RISC-V 低成本优势辩护](https://rvembedded.com/blog_post/12/) ⭐️ 7.0/10

一位来自发展中国家的嵌入式工程师发表了一篇题为《一位第三世界嵌入式工程师回应“RISC-V 他们本应更了解”》的博客文章，主张 RISC-V 开放、模块化的指令集架构（ISA）对低成本、可及的硬件至关重要。这篇文章直接反驳了 RISC-V 的设计选择会将其应用限制在高端计算场景的说法。 这为典型的硅谷中心叙事提供了有价值的反视角，强调了发展中国家的成本与可及性如何影响架构的采用。它将 RISC-V 的讨论从性能基准扩展到嵌入式系统开发中的经济和地缘现实。 作者认为，对于尼日利亚、孟加拉国等国家的学生和企业来说，10 美分器件与 1 美元器件之间的差别并非四舍五入即可忽略的小事，而且 RISC-V 允许本地生产定制芯片，无需支付外国 IP 授权费。然而，评论者指出其中存在逻辑矛盾：如果运送 1 美元的芯片到他所在位置就要花费 60 至 200 美元，那么所谓 RISC-V 器件到货价为 10 美分的说法似乎自相矛盾，除非这些芯片的运费完全不同。

hackernews · Narishma · 8月16日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=49321717)

**背景**: RISC-V 是一种开放标准的指令集架构（ISA），任何人无需支付授权费即可使用、修改和扩展，这与 ARM 等专有 ISA 不同。它的模块化结构允许设计者为特定应用定制处理器，这使得它对嵌入式系统、初创公司和学术研究尤其有吸引力。该讨论将 RISC-V 在高性能计算领域的前景与其在低成本、低功耗嵌入式设备中的实际优势进行了对比，尤其关注发达市场之外的开发者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RISC-V">RISC-V - Wikipedia</a></li>
<li><a href="https://www.wevolver.com/article/risc-v-vs-arm">RISC-V vs ARM: A Comprehensive Comparison of Processor Architectures</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏这种新鲜视角，但质疑文章的逻辑一致性。kelnos 和 vlovich123 都质疑：既然运送 1 美元的芯片到他所在位置就要花费 60 至 200 美元，作者又如何声称 RISC-V 器件的到货价为 10 美分。HawtAds 则指出到尼日利亚和孟加拉国的运输成本并没有那么高，并称赞这篇文章相对于硅谷中心的观点是“一股清新的空气”。

**标签**: `#RISC-V`, `#Embedded Systems`, `#Open Hardware`, `#Cost Analysis`, `#Developing Countries`

---

<a id="item-3"></a>
## [Firefox for iOS 加入原生广告拦截器](https://support.mozilla.org/en-US/kb/block-ads-firefox-ios) ⭐️ 6.0/10

Firefox for iOS 现已内置广告拦截功能，用户无需安装单独扩展，直接在浏览器设置中即可拦截广告。该功能简化了苹果移动平台上的广告屏蔽体验。 这很重要，因为 iOS 上的浏览器必须使用 WebKit，无法像桌面版那样安装传统扩展；原生广告拦截器让 Firefox iOS 用户能更简单、更方便地获得隐私保护。它也有助于 Firefox 与 Safari 等自带或易用内容拦截功能的浏览器竞争。 该广告拦截器依赖 iOS 的内容拦截机制（如 Content Blocker API 和 WKContentRuleList），而不是 Mozilla 自己的 Gecko 引擎。社区用户指出，它可能仍会在搜索引擎结果页面显示广告，而 uBlock Origin Lite for Safari 等更强大的替代方案依然存在。

hackernews · pentagrama · 8月16日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49319633)

**背景**: 根据苹果 App Store 的规定，iOS 上的所有浏览器（包括 Firefox）都必须使用 WebKit 渲染引擎，因此 Firefox 无法在 iOS 上使用 Gecko 引擎，也无法支持完整的 Firefox 扩展生态。iOS 上的广告拦截通常通过 Safari Content Blocker API 实现，该 API 允许应用向 Safari 及基于 WebKit 的浏览器提供内容拦截规则。Mozilla 之前推出的隐私浏览器 Firefox Focus 已内置广告拦截器，并可通过 iOS 内容拦截器在系统范围内生效；因此 Firefox 这次加入内置拦截功能主要是减少操作步骤。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/safariservices/sfcontentblockermanager">A class that your app uses to interact with a content blocker extension.</a></li>
<li><a href="https://github.com/WebKit/webkit/blob/main/Source/WebKit/UIProcess/API/Cocoa/WKContentRuleListStore.h">WebKit/Source/WebKit/UIProcess/API/Cocoa/WKContentRuleListStore.h at main · WebKit/WebKit</a></li>
<li><a href="https://www.simplymac.com/apps/best-ad-blocker-for-iphone">Best Ad Blocker for iPhone (2026) - SimplyMac</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上欢迎这一功能，但也指出它并非新事：Firefox Focus 早已通过 iOS 内容拦截器提供广告屏蔽。有用户指出 uBlock Origin Lite for Safari 更强大；有人抱怨 iOS 不支持扩展；还有人希望 Firefox 未来能在 iOS 上使用 Gecko 引擎。

**标签**: `#Firefox`, `#iOS`, `#adblocking`, `#browser`

---