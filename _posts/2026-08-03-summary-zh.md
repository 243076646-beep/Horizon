---
layout: default
title: "Horizon Summary: 2026-08-03 (ZH)"
date: 2026-08-03
lang: zh
---

> 从 10 条内容中筛选出 1 条重要资讯。

---

1. [卡帕西的“鹈鹕”基准测试引发 AI 物理世界理解之争](#item-1) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [卡帕西的“鹈鹕”基准测试引发 AI 物理世界理解之争](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 7.0/10

安德烈·卡帕西（Andrej Karpathy）发帖指出，“鹈鹕”基准——常被描述为一种 3D 生成测试——要求 AI 模型生成一只骑自行车的鹈鹕。由 Hacker News 帖子引发的讨论，集中在该基准能否有效衡量模型对物理世界的理解。 这之所以重要，是因为基准会引导研究投入：如果“鹈鹕”基准流行起来，模型开发者就会把重点转向空间推理和世界建模，而不只是对话文本或精致画面。这场争论也反映出，在基础语言和图像生成能力不再是最主要瓶颈后，社区对如何评估模型普遍缺乏共识。 实际上，该基准的公开版本通常使用提示词“生成一只骑自行车的鹈鹕的 SVG”，Hugging Face 和 Simon Willison 的 GitHub 仓库提供了不同采样温度下的并排输出对比。评论者指出结果在很大程度上仍是主观、定性的；还有人认为 Anthropic 的模型可能专门针对 three.js 代码生成做了调优，因此这类输出并不能有力证明模型具备通用物理世界理解。

hackernews · delichon · 8月2日 04:05 · [社区讨论](https://news.ycombinator.com/item?id=49140998)

**背景**: “鹈鹕”基准主要与 Simon Willison 那个看似有趣但很有揭示性的提示词相关：让语言模型生成一个“骑自行车的鹈鹕”的 SVG，这迫使模型把指令理解、代码生成和空间推理结合在同一项输出中。SVG 是一种基于文本的矢量图片格式，因此这个任务很容易比较不同模型的输出。安德烈·卡帕西是著名 AI 研究者、特斯拉前 AI 总监，他经常分享这类观察，他的帖子也常引发关于如何衡量模型能力的广泛讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/victor/pelican-benchmark">Pelican Benchmark - a Hugging Face Space by victor</a></li>
<li><a href="https://github.com/simonw/pelican-bicycle">GitHub - simonw/pelican-bicycle: LLM benchmark: Generate an ...</a></li>
<li><a href="https://tributary.cc/pelicanbench/">Pelican Bench — Tributary</a></li>

</ul>
</details>

**社区讨论**: 评论区观点分歧：有人认为即使输出粗糙也有价值，因为“鹈鹕”能暴露模型对物理世界结构的把握，而不只是图像质量。另一些人担心模型可能针对 three.js 等库调优来“刷基准”，仅凭“一只很粗糙的鹈鹕”就宣布问题解决说明质量标准在降低。另有评论提出替代方向，如更具互动性的 LLM 聊天基准，也有人分享用 LLM 制作 3D 动画的实践经验。

**标签**: `#AI`, `#machine-learning`, `#benchmarks`, `#3D-generation`, `#LLM`

---