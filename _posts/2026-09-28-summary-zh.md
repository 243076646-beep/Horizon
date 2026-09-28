---
layout: default
title: "Horizon Summary: 2026-09-28 (ZH)"
date: 2026-09-28
lang: zh
---

> 从 7 条内容中筛选出 3 条重要资讯。

---

1. [博客质疑 Google 搜索日益怪异的 AI 结果](#item-1) ⭐️ 7.0/10
2. [Fireworks AI 发布首个自研推理模型 Ember-1，基于 Kimi K3 构建](#item-2) ⭐️ 7.0/10
3. [Meta Muse 购物智能体或危及亚马逊 500 亿美元核心业务](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [博客质疑 Google 搜索日益怪异的 AI 结果](https://sancho.bearblog.dev/google-weird/) ⭐️ 7.0/10

一篇题为《Google 什么时候变得这么奇怪了？》的批评性博客文章在 Hacker News 上引发了大规模讨论（751 分、401 条评论），话题聚焦 Google 搜索由 AI 生成的摘要以及愈发对话化的结果如何改变了搜索体验。评论者分享了 AI 答案与现实公然矛盾的亲身经历，例如有用户询问 Halifax Wanderers 队是否还有机会进入季后赛，AI 却自信而错误地声称该队已经锁定季后赛席位。 这场争论正处在数十亿人获取信息方式发生重大转变的核心：Google、微软等公司正在用大语言模型生成的答案取代链接列表。它引发了关于信任、事实可靠性以及广告驱动的搜索引擎激励机制等尖锐问题——搜索引擎如今以自己的口吻直接作答，而不再把用户引向信息源。 核心抱怨并不是 AI 答案毫无用处，而是它们可能自信地给出错误内容，用户必须越过摘要往下翻并手动核实来源才能得到正确答案。评论者还指出，Google 将向对话式助手的转变包装成一种改进，而批评者则认为这实质上是在变现用户注意力，并削弱用户查阅原始信源的习惯。

hackernews · sancho-panza · 9月27日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=49870367)

**背景**: 大语言模型是一类 AI 系统，通常基于 Transformer 架构的神经网络，通过海量文本训练来预测和生成语言；它们是 ChatGPT、Gemini、Claude 等聊天机器人背后的技术，如今也越来越多地用于 AI 搜索摘要。由于其输出是从训练数据中按概率生成的，带有偏见或不准确的数据会使其结果不可靠，这也是业界会针对推理能力、事实准确性和安全性进行基准评测的原因。Google 的 AI Overviews 正是把这类生成文本放在搜索结果的最顶部，排在传统排序链接之前。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model</a></li>

</ul>
</details>

**社区讨论**: 评论情绪明显分裂。一些评论者认为普通用户一直想要一个“电脑里能对话的小人”，因此这对 Google 而言是实打实的产品胜利；另一些人则称其“令人不安”，指责科技行业利用 AI 带来的恐惧来提升自身可信度。还有一个颇具代表性的观点认为，更深层的问题是普遍存在的孤独感，人们宁愿与软件建立准社会关系，也不去询问现实中的朋友。

**标签**: `#google`, `#search`, `#ai`, `#llm`, `#user-experience`

---

<a id="item-2"></a>
## [Fireworks AI 发布首个自研推理模型 Ember-1，基于 Kimi K3 构建](https://fireworks.ai/blog/ember-1) ⭐️ 7.0/10

Fireworks AI 宣布推出 Ember-1，这是其首个以 Fireworks 品牌命名的模型，一个基于 Kimi K3 构建的专用推理模型，目标是在保持相近质量的同时显著缩短推理过程，据称可减少约 40% 的 token 消耗。该模型已在 Fireworks 的无服务器 API 上线（按 token 计费，兼容 OpenAI 客户端），支持文本与图像输入、工具调用和结构化输出，并提供 100 万 token 的上下文窗口。 此次发布标志着 Fireworks 从单纯托管其他实验室开源权重模型的推理服务商，转变为同时自研模型的开发者，这可能改变客户对其中立性和供应商锁定风险的看法。token 效率的提升也直接影响智能体（agent）类工作负载，因为冗长的推理过程往往是延迟和成本的主要来源。 Ember-1 是 Kimi K3 经过后训练（post-training）得到的衍生模型，定价与基座模型相同，均为每百万 token 输入 3 美元、输出 15 美元，因此成本节省完全来自更少的 token 输出，而非更低的单价；有第三方分析称在某些 A/B 测试中推理 token 最多可减少 71%，但同时提醒对部分任务而言保留原始 K3 可能仍然更优。Fireworks 表示，他们最初是将该模型作为面向垂直领域继续后训练的起点检查点，后来才意识到许多用户可以直接受益于更简洁、更少啰嗦的推理输出。

hackernews · gmays · 9月27日 17:31 · [社区讨论](https://news.ycombinator.com/item?id=49868830)

**背景**: Fireworks AI 是一家推理平台，专注于快速、可扩展地部署开源权重 AI 模型，它批量采购 GPU 算力并在多个云之间调度，让客户无需自行管理基础设施。Kimi K3 是一款大型开源权重推理模型，Fireworks 同样提供其服务；所谓“推理”模型，是指在给出最终答案前会先生成一长串中间思考 token 的模型。后训练（post-training）则是指在模型初始预训练之后追加的训练，通常用于特化模型行为——在这里就是让推理过程在质量相近的前提下变得更短。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fireworks.ai/blog/ember-1">Introducing Ember-1 - fireworks.ai</a></li>
<li><a href="https://www.explainx.ai/blog/fireworks-ember-1-kimi-k3-reasoning-tokens-2026">Ember-1: 71% Fewer Reasoning Tokens at K3 Price (2026 ...</a></li>
<li><a href="https://nano-gpt.com/models/text/fireworks/ember-1">Ember 1 model | NanoGPT</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反应褒贬不一：多位评论者（tukHelix、tangled）质疑以推理服务商身份著称的 Fireworks 涉足模型自研，是否会让那些用它来部署其他实验室模型的客户产生信任或依赖方面的顾虑；而 jamienk 则认为开源模型的进步速度往往快于闭源模型，并以 Linux 和 Wikipedia 为例。GodelNumbering 感叹这是“模型训练的黄金时代”，描述自己用生成的 14 万多条样本、花约两天时间微调 Qwen 3 0.6B 基座模型，做出了效果出乎意料的英译 Bash 模型；netvarun 则跑题指出，随着 Sol 降价，Kimi K3 的性价比优势正在减弱。

**标签**: `#LLM`, `#Fireworks AI`, `#open-source models`, `#model training`, `#AI inference`

---

<a id="item-3"></a>
## [Meta Muse 购物智能体或危及亚马逊 500 亿美元核心业务](https://www.reddit.com/r/ecommerce/comments/1ws0hu4/meta_muse_may_cost_amazon_50b/) ⭐️ 7.0/10

r/ecommerce 上一篇引发热议的分析指出，Meta 新推出的个人 AI 智能体 Muse 可以代替用户购物，可能让亚马逊约 500 亿美元的收入面临风险；而亚马逊几乎在 Muse 上线后立刻阻止其在自家平台购物。作者认为，封禁的表面理由是安全与使用条款，实质是亚马逊在捍卫自己对购物入口的掌控权。 如果 AI 智能体成为购物的“正门”，亚马逊的店面、搜索结果和赞助商品位将大幅失去影响力，因为做比较和决定购买的是智能体而不是人。在这三块受影响业务中，广告最为脆弱——因为没人看到的赞助商品位等于没有价值。 作者给出的数字是：亚马逊 2025 财年自营在线商店 2690 亿美元、第三方卖家服务 1720 亿美元、广告 690 亿美元，合计约 5100 亿美元，约占亚马逊整体的 70%；这意味着只要购物意图转移 10%，就有 500 亿美元“暴露”出来——是“暴露”，并非一夜之间损失。亚马逊封禁的官方理由预计是安全、未授权访问和使用条款，原文也承认亚马逊仍握有 Prime、物流和信任优势。

reddit · r/ecommerce · /u/MustIReadIt · 9月28日 00:40

**背景**: Meta 于 2026 年 9 月推出 Muse，它是一个个人 AI 智能体，可以直接在 WhatsApp 对话中浏览网页、填写表单、议价并完成购买，这属于“代理式商务”（agentic commerce）的大趋势——由 AI 智能体在用户授权下代为调研、谈判和下单。在传统电商模式下，亚马逊这类平台靠用户搜索、浏览和比价的这一时刻变现，因为广告和各类费用都发生在这个环节；如果智能体跳过了这个页面，变现也就被绕开了。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for...</a></li>
<li><a href="https://www.stateofaimarketing.co/news/meta-muse-shopping-agent/">Meta Muse turns WhatsApp into a shopping agent</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-commerce">What is agentic commerce? - IBM</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#e-commerce`, `#Amazon`, `#Meta`, `#platform economics`

---