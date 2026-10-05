---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 4 条内容中筛选出 2 条重要资讯。

---

1. [Strata 在单张 RTX 4090 上以约 124 tokens/秒运行 125B 的 Qwen3.8-Flash-Next](#item-1) ⭐️ 7.0/10
2. [GitHub 脚本可在 macOS 27 上移除 Apple Intelligence 并回收磁盘空间](#item-2) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Strata 在单张 RTX 4090 上以约 124 tokens/秒运行 125B 的 Qwen3.8-Flash-Next](https://github.com/Niko1221/Strata) ⭐️ 7.0/10

一个名为 Strata（Niko1221/Strata）的 GitHub 项目声称可以在消费级硬件上运行 125B 参数的 Qwen3.8-Flash-Next 模型，提供 Windows/Linux 一键安装、本地 OpenAI/Anthropic 兼容 API 以及可选的图像输入。一位 Hacker News 评论者报告称，在配备 128GB DDR5 和 Ryzen 7950X3D 的 RTX 4090 上实测达到 124 tokens/秒，至少在某一台机器上复现了标题中的吞吐量。 在单张消费级 GPU 上以每秒 100 多个 token 的速度本地运行 125B 级别的模型，将显著改变个人开发者和小团队无需租用数据中心硬件就能自托管的能力边界。这也加剧了更广泛的争论：激进的 4-bit 以下量化究竟是真正的能力突破，还是用隐性精度损失换取了漂亮的吞吐数字。 Hacker News 讨论串中的独立测试发现，在同样使用同一份 GGUF 权重和视觉适配器、执行 50 张图片的坐标定位任务时，Strata 的视觉精度明显差于 llama.cpp——中位误差为 154.8 像素，而后者为 46.5 像素。该项目自称是面向 Qwen3.8-Flash-Next 的 Strata 推理引擎，并在 localhost 上提供 OpenAI/Anthropic 接口，但其精度主张仍只是单一仓库的结果，缺乏公开的评测方法。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: 量化是把模型权重压缩成更少的比特，以便塞进有限的显存；GPTQ、AWQ、GGUF K-quants 等生产级方案通常以 32–128 个权重为一个 4-bit 块共享缩放因子。一旦低于 4 bit，均匀量化就会出现明显退化，通常需要基于旋转或非均匀比特分配等高级方法才能维持可接受的精度。由于 125B 参数模型以 16-bit 存储大约需要 250GB 内存，要在 24GB 显存的 RTX 4090 上运行，必然依赖极其激进的压缩并把部分模型卸载到系统内存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata">GitHub - Niko1221/Strata: Qwen3.8-Flash-Next on any consumer ...</a></li>
<li><a href="https://arxiv.org/html/2402.16775v1">A Comprehensive Evaluation of Quantization Strategiesfor ...</a></li>
<li><a href="https://picovoice.ai/blog/sub-4-bit-llm-quantization/">Sub-4-Bit LLM Quantization: Enterprise Guide to Methods ...</a></li>

</ul>
</details>

**社区讨论**: 社区意见分化：有评论者在 4090 上确认达到 124 tokens/秒，称其“出人意料地好用”；但也有人用视觉任务将 Strata 与 llama.cpp 独立对比，发现误差大幅上升（中位数 154.8 像素对 46.5 像素）。其他人出于质量考虑对低于 4-bit 的量化持怀疑态度，并分享了他们认为更可靠的替代方案（llama.cpp、ds4）；还有评论者抱怨 LLM 论坛在被 Strata 链接刷屏，而结果尚未得到验证。

**标签**: `#llm-inference`, `#quantization`, `#local-llm`, `#gpu-optimization`, `#qwen`

---

<a id="item-2"></a>
## [GitHub 脚本可在 macOS 27 上移除 Apple Intelligence 并回收磁盘空间](https://github.com/omlahore/RemoveMacAI) ⭐️ 7.0/10

GitHub 上的 RemoveMacAI 项目（作者 omlahore）发布了一款脚本，用于在 macOS 27 上禁用并移除 Apple Intelligence，从而回收其本地 AI 资源占用的磁盘空间。该工具获得了 360 分和 222 条评论，引发了关于苹果系统体积膨胀与隐私取舍的激烈讨论。 这表明 macOS 用户如今也认为自己需要第三方去臃肿脚本来夺回对系统资源的控制权，而这原本是 Windows 用户长期抱怨的麻烦事。它也引发了更广泛的争论：苹果预装的 AI 功能、以及无法用简单开关彻底关闭它们，究竟属于合理的产品策略还是不受欢迎的臃肿软件。 该脚本针对的是随系统预装的 Apple Intelligence 端侧模型文件，即便在系统设置中显示为已关闭，这些文件仍会占用存储空间。社区成员指出，这些模型体积相对较小且完全在本地运行而非云端，同时系统更新可能会把被删除的资源重新下载回来。

hackernews · privacyisntdead · 10月4日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=49957116)

**背景**: Apple Intelligence 是苹果在 2024 年 6 月 10 日 WWDC 上发布的一套 AI 功能，内置于 iOS 18、iPadOS 18 和 macOS Sequoia，依赖设备端处理与服务器端模型的结合。由于其中一部分在本地运行，其模型文件无论用户是否启用都会留在磁盘上。Windows 上早就有 O&amp;O ShutUp10 这类去除遥测与多余组件的去臃肿工具，而这个项目表明 macOS 周边也在形成类似的做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://discussions.apple.com/thread/255927866">How to completely remove Apple Intelligen… - Apple Community</a></li>
<li><a href="https://www.techradar.com/computing/artificial-intelligence/apple-intelligence-features-explained-everything-you-need-to-know-about-apple-ai-and-when-you-can-use-it">Apple Intelligence features explained - everything you need ...</a></li>

</ul>
</details>

**社区讨论**: 评论整体偏向批判且意见分化：有人把这一情况比作 Windows 用户一直以来不得不做的“去冗余”仪式，也有人抱怨 iOS 不像微软和 Firefox 那样提供一键关闭 AI 的全局开关。一个值得注意的反方观点质疑，为什么要删除体积相对小巧、完全离线运行且表现均衡的本地推理模型；还有人将其与 O&amp;O ShutUp10 相类比，并好奇苹果究竟如何权衡磁盘占用成本与功能收益。

**标签**: `#macOS`, `#Apple Intelligence`, `#privacy`, `#bloatware-removal`, `#debloat-tools`

---