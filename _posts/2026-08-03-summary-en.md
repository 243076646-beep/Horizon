---
layout: default
title: "Horizon Summary: 2026-08-03 (EN)"
date: 2026-08-03
lang: en
---

> From 10 items, 1 important content pieces were selected

---

1. [Karpathy’s ‘Pelican’ Benchmark Sparks Debate on AI Physical-World Understanding](#item-1) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Karpathy’s ‘Pelican’ Benchmark Sparks Debate on AI Physical-World Understanding](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 7.0/10

Andrej Karpathy drew attention to “Pelican,” a benchmark — commonly framed as a 3D generation test — that asks AI models to create a pelican riding a bicycle. The resulting Hacker News thread debated whether this benchmark meaningfully measures models’ understanding of the physical world. This matters because benchmarks channel research effort: if “Pelican” gains traction, model developers will optimize for spatial reasoning and world modeling rather than just conversational text or polished visuals. The debate also reflects the wider community’s uncertainty about how to evaluate models once basic language and image-generation skills are no longer the bottleneck. In practice, the public version of the benchmark is usually phrased as “Generate an SVG of a pelican riding a bicycle,” and Hugging Face plus Simon Willison’s GitHub repository provide side-by-side model outputs at different sampling temperatures. Commenters noted that results are still largely qualitative and subjective; one argued Anthropic models may be specifically tuned for three.js code generation, so those outputs are not strong evidence of general physical understanding.

hackernews · delichon · Aug 2, 04:05 · [Discussion](https://news.ycombinator.com/item?id=49140998)

**Background**: The “Pelican” benchmark is most associated with Simon Willison’s playful but revealing prompt: asking a language model to create an SVG of a pelican riding a bicycle forces it to combine instruction following, code generation, and spatial reasoning in one artifact. SVG is a text-based vector image format, which makes the task easy to evaluate and compare across models. Andrej Karpathy, a prominent AI researcher and former Tesla AI director, frequently shares such observations, and his posts often spark broader conversations about how to measure model capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/spaces/victor/pelican-benchmark">Pelican Benchmark - a Hugging Face Space by victor</a></li>
<li><a href="https://github.com/simonw/pelican-bicycle">GitHub - simonw/pelican-bicycle: LLM benchmark: Generate an ...</a></li>
<li><a href="https://tributary.cc/pelicanbench/">Pelican Bench — Tributary</a></li>

</ul>
</details>

**Discussion**: Discussion was split: some argued that even janky outputs are valuable because “Pelican” exposes how well a model grasps physical-world structure, not just image quality. Others worried that models may be benchmark-hacked by tuning for three.js or similar libraries, and that calling the problem solved after seeing “a very janky pelican” signals lowered quality expectations. Several commenters offered alternative directions, including more interactive LLM-chat benchmarks, while one shared a hands-on project using an LLM to create 3D animations.

**Tags**: `#AI`, `#machine-learning`, `#benchmarks`, `#3D-generation`, `#LLM`

---