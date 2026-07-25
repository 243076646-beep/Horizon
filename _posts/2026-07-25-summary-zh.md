---
layout: default
title: "Horizon Summary: 2026-07-25 (ZH)"
date: 2026-07-25
lang: zh
---

> 从 16 条内容中筛选出 5 条重要资讯。

---

1. [Anthropic 发布无数据保留要求的 Claude Opus 5](#item-1) ⭐️ 9.0/10
2. [安全摄像头在登录页面泄露 GitHub 管理员令牌](#item-2) ⭐️ 9.0/10
3. [编码进步为何软件质量反而下降](#item-3) ⭐️ 8.0/10
4. [谷歌签署欧盟 AI 法案透明度准则，设定合规标杆](#item-4) ⭐️ 6.0/10
5. [欧盟警告 TikTok 因违反儿童安全规定可能面临罚款](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic 发布无数据保留要求的 Claude Opus 5](https://www.anthropic.com/news/claude-opus-5) ⭐️ 9.0/10

Anthropic 发布了 Claude Opus 5，这是一款最先进的 AI 模型，其智能水平接近 Claude Fable 5，但价格只有后者的一半。值得注意的是，它没有一般访问的数据保留要求，这与需要 30 天数据保留的 Fable 5 不同。 此次发布为组织提供了一个无需数据保留的强大 AI 模型，解决了重大的隐私和合规问题。它也为性价比高的前沿 AI 设立了新基准，可能加速在敏感行业中的采用。 Claude Opus 5 在大多数基准测试中与 Fable 5 持平，但价格只有后者的一半。它延续了前代 Opus 4.8 的许多“Claude 风格”，表明风格上的一致性。

hackernews · alvis · 7月24日 16:57 · [社区讨论](https://news.ycombinator.com/item?id=49038433)

**背景**: Anthropic 是一家 AI 安全公司，开发 Claude 系列模型。&\#x27;Opus&\#x27; 模型是高能力模型，而 &\#x27;Fable&\#x27; 模型代表前沿智能。数据保留政策对处理敏感数据的组织至关重要，因为某些模型需要保留提示和输出以运行安全分类器。Claude Opus 5 在零数据保留政策下发布，使其适用于隐私敏感的使用场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-5">Introducing Claude Opus 5 \ Anthropic</a></li>
<li><a href="https://glitchwire.com/news/claude-opus-5-matches-fable-5-on-most-benchmarks-at-half-the-price/">Claude Opus 5 Matches Fable 5 on Most Benchmarks at... — Glitchwire</a></li>
<li><a href="https://coursiv.io/blog/claude-opus-5">Claude Opus 5 : Release Date, What We Know &amp; Model... | Coursiv Blog</a></li>

</ul>
</details>

**社区讨论**: 社区成员强调零数据保留政策是相对于 Fable 5 的关键优势。有用户报告称，Opus 5 在图片转 HTML 方面表现优于 Fable 5，更准确地遵循设计源。另一评论指出，随着公司发布众多模型变体，模型路由的复杂性正在增加。

**标签**: `#AI`, `#LLM`, `#Claude`, `#Anthropic`, `#model release`

---

<a id="item-2"></a>
## [安全摄像头在登录页面泄露 GitHub 管理员令牌](https://hhh.hn/hanwha-github-token/) ⭐️ 9.0/10

发现一款韩华（Hanwha）安全摄像头在其登录页面源码中硬编码了 GitHub 管理员令牌，暴露了对 GitHub 仓库的管理员访问权限。 此事件凸显了物联网设备中严重的安全缺陷，硬编码的凭证可能导致制造商基础设施和客户数据遭受广泛入侵。 该令牌是一个管理员级别的 GitHub 个人访问令牌（PAT），嵌入在摄像头的网络界面中，可用于访问私有仓库和管理组织。

hackernews · hhh · 7月24日 11:54 · [社区讨论](https://news.ycombinator.com/item?id=49034292)

**背景**: GitHub 个人访问令牌（PAT）是一种无需密码即可通过 GitHub API 进行身份验证的方法，其权限由作用域定义。公开暴露此类令牌会使任何获得令牌的人拥有与令牌所有者相同的访问权限。物联网设备通常缺乏适当的安全实践，硬编码凭证是一种已知漏洞，可通过设备固件或网络界面被利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens">Managing your personal access tokens - GitHub Docs</a></li>
<li><a href="https://csrc.nist.gov/pubs/sp/1800/36/final">SP 1800-36, Trusted Internet of Things (IoT) Device Network ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对物联网安全的不满，指出许多供应商发货的设备带有硬编码凭证和安全缺陷。一位用户建议将摄像头放在没有互联网访问权限的独立 VLAN 中作为缓解措施。另一位评论者指出固件中还嵌入了美国战争部的 IP 地址，引发了进一步的担忧。

**标签**: `#security`, `#IoT`, `#vulnerability`, `#GitHub`, `#camera`

---

<a id="item-3"></a>
## [编码进步为何软件质量反而下降](https://ptrchm.com/posts/nothing-works-and-everyone-is-euphoric/) ⭐️ 8.0/10

一篇文章指出，软件质量下降的原因是技术外行决策者、对更新的恐惧以及 AI 生成代码的权衡，在工程师社区引发广泛讨论。 这一批评挑战了关于 AI 辅助开发的普遍乐观情绪，揭示了影响数百万用户的技术公司系统性问题。它引起了许多对用户体验下降感到沮丧的工程师的共鸣。 文章特别提到 Slack 在 macOS 上抢夺焦点以及普遍的对更新恐惧作为体验恶化的例子。还指出 AI 代码生成大幅改变了‘快’的定义，但并未提高对代码正确性的信心。

hackernews · pchm · 7月24日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=49033004)

**背景**: 对更新的恐惧（update dread）指用户被迫安装可能引入回归或非期望变更的更新时产生的焦虑。像 GitHub Copilot 这样的 AI 代码生成工具可以加速开发，但通常会产生需要仔细审查的代码，如果管理不当会引入技术债务。文章称非技术决策者优先考虑新奇而非质量，这是软件工程批评中反复出现的主题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aha.io/engineering/articles/the-architectural-trade-offs-of-ai-code-generation">The architectural trade-offs of AI code generation - Aha!</a></li>
<li><a href="https://waqas.ragnorx.com/blog/trade-offs-ai-code-generation">The Trade-Offs of Relying on AI for Code | Waqas Ahmad</a></li>

</ul>
</details>

**社区讨论**: 社区评论基本同意这一批评。一位用户指出非技术‘冒牌者’控制产品决策，另一位分享了个人对更新的恐惧经历。第三位强调了 AI 辅助编码中速度与正确性之间的权衡，指出工程师仍需投入时间确保质量。

**标签**: `#software quality`, `#tech industry`, `#UX`, `#AI code generation`, `#engineering culture`

---

<a id="item-4"></a>
## [谷歌签署欧盟 AI 法案透明度准则，设定合规标杆](https://news.google.com/rss/articles/CBMimAFBVV95cUxOWjlwUDIzUnZFZlpTdjdQQ0F3VmthdW5qb3NmUFBiMjBVVVl5aDh6Qld4T3kybHQyYTNEb0V1OWR3UGVNVXpKQ3ZoRVBpaU9oVmE3ME81ckZMMXduUkhfdF9TV3dMTlN5T1BWX3lZWnA5Q0szZ1hFRkY4Y2ZFODN2Z3U1UUtPYXQtUndBT2wtWHlZZjg1NW9NeA?oc=5) ⭐️ 6.0/10

谷歌已签署欧盟《人工智能法案》透明度准则，成为首批正式承诺遵守这一自愿性行为准则的大型科技公司之一，该准则涉及 AI 生成内容的标记和标注。 此举为其他 AI 开发者设定了高合规标准，表明谷歌对 AI 监管的积极态度，可能影响行业标准并塑造《人工智能法案》未来的执行方式。 该透明度准则是一个自愿框架，旨在支持遵守《人工智能法案》第 50 条，专注于对 AI 生成内容进行一致且适度的标记。签署方承诺采取明确的标签和透明度措施，但不会取代该法案的法律义务。

rss · GoogleNews-欧盟监管 · 7月24日 14:46

**背景**: 欧盟《人工智能法案》是一项具有里程碑意义的法规，根据风险对 AI 系统进行分类并施加包括透明度在内的要求。第 50 条特别规定 AI 生成内容必须明确标注。AI 生成内容透明度行为准则为签署方提供了一个实用的、覆盖全欧盟的框架，以证明其遵守这些透明度义务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialintelligenceact.eu/article/50/">Article 50: Transparency Obligations for Providers and ...</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content">Code of Practice on Transparency of AI-Generated Content</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#EU AI Act`, `#Google`, `#compliance`, `#tech policy`

---

<a id="item-5"></a>
## [欧盟警告 TikTok 因违反儿童安全规定可能面临罚款](https://news.google.com/rss/articles/CBMi5AFBVV95cUxPTjhHLTMzTmpmcjByZldrT2hvbTNxMkF4YmxlOERrM1g3WHlWODRqRGFIbnp4aGFremdieXZBelR0am5oT2JsaWFJNG5TcEpZV2hSYnh6Q01fVlVfRXdFZWhlMnZJelhsamQ5ZzZSQ1BpYm5NdkpZY0ZLM1pFMHFicEw3UkdoOTh0SEl6cXN6Qk54cllsVVNsTWl6Y24xbHFRWlZlS09MTVdYbDBHdzRZV0RfeEpsc3JDZ2hUbk1VQ2FUa1VBYWxHaDNXX2xWOFhNN3AwSWJkUGhlTGpTUUpBMUNYYkrSAeoBQVVfeXFMT2ZkaWVaV1lUTHQzUFBwMWNxLWJXV2JtdU5FNnV1UGZwTV9qSkFGTFVxaEtqa01QY0F2Q0NkZDVBbEJUNmhGNXkxeFVNY1hyT0tRZi0yVVVtQTIwX1J1Y0paY0xsSUhNYlZDVURVbWRaLXZmVzdBTHpHM2ZrRk9aeTVGZVlQRTl1ZncxaDZrNEFJdmphYzNEckJSb0RnZ3EzODBwZkpaNVI2OEVWUGVNUGg4UDkybUdEV3huS3lOTTAzVmxMY2JvWUpOdmFZekNCc0hCQVRqZW0xa0ZlYl95a0Q4d2w1R09YUERR?oc=5) ⭐️ 6.0/10

欧盟已正式警告 TikTok，因其未能充分保护平台上的儿童安全，可能面临罚款，此举援引了《数字服务法案》中的潜在违规行为。 这一执法行动凸显了欧盟依据《数字服务法案》追究大型平台责任的决心，为整个科技行业的儿童安全监管树立了先例。 该警告是依据《数字服务法案》开展的持续调查的一部分，该法案对 TikTok 等超大型在线平台施加了严格义务，包括针对未成年人的风险评估和缓解措施。

rss · GoogleNews-欧盟监管 · 7月24日 12:19

**背景**: 《数字服务法案》（DSA）是欧盟于 2022 年生效的法规，为数字服务建立了全面的规则，包括内容审核和平台透明度。该法案适用于所有在线中介机构，对服务超过 4500 万欧盟用户的超大型在线平台（VLOP）有更严格的要求。TikTok 于 2023 年 4 月被指定为 VLOP，因此需承担 DSA 下的增强义务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act">Digital Services Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/digital-services-act">The Digital Services Act | Shaping Europe’s digital future</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#TikTok`, `#Digital Services Act`, `#child safety`, `#platform governance`

---