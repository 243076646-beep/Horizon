---
layout: default
title: "Horizon Summary: 2026-10-05 (EN)"
date: 2026-10-05
lang: en
---

> From 4 items, 2 important content pieces were selected

---

1. [Strata Runs 125B Qwen3.8-Flash-Next on a Single RTX 4090 at ~124 Tokens/s](#item-1) ⭐️ 7.0/10
2. [GitHub script strips Apple Intelligence from macOS 27 to reclaim disk space](#item-2) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Strata Runs 125B Qwen3.8-Flash-Next on a Single RTX 4090 at ~124 Tokens/s](https://github.com/Niko1221/Strata) ⭐️ 7.0/10

A GitHub project called Strata \(Niko1221/Strata\) claims to run the 125B-parameter Qwen3.8-Flash-Next model on consumer hardware, with a one-click installer for Windows and Linux, a local OpenAI/Anthropic-compatible API, and optional image input. A Hacker News commenter reported getting 124 tokens/sec on an RTX 4090 with 128GB DDR5 and a Ryzen 7950X3D, confirming the headline throughput claim on at least one machine. Running a 125B-class model locally at over 100 tokens/sec on a single consumer GPU would meaningfully change what hobbyists and small teams can self-host without renting datacenter hardware. It also fuels the broader debate over whether aggressive sub-4-bit quantization is a genuine capability unlock or just trades hidden accuracy loss for impressive speed numbers. Independent testing posted in the Hacker News thread found that Strata produced substantially worse vision accuracy than llama.cpp when running the exact same GGUF weights and vision adapter on a 50-image coordinate-localization task — a median error of 154.8 pixels versus 46.5 pixels. The GitHub project describes itself as a Strata inference engine for Qwen3.8-Flash-Next with an OpenAI/Anthropic API served on localhost, but the accuracy claim remains a single-repo result without published methodology.

hackernews · snehesht · Oct 4, 12:51 · [Discussion](https://news.ycombinator.com/item?id=49953495)

**Background**: Quantization compresses a model&\#x27;s weights into fewer bits so it fits in limited GPU memory; production schemes such as GPTQ, AWQ and GGUF K-quants typically use 4-bit blocks of 32–128 weights sharing scale factors. Below 4 bits, uniform quantization starts to degrade noticeably, and advanced rotation-based or non-uniform bit-allocation methods are usually required to keep accuracy acceptable. Because a 125B-parameter model in 16-bit would need roughly 250GB of memory, running it on a 24GB RTX 4090 necessarily depends on extremely aggressive compression plus offloading parts of the model to system RAM.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata">GitHub - Niko1221/Strata: Qwen3.8-Flash-Next on any consumer ...</a></li>
<li><a href="https://arxiv.org/html/2402.16775v1">A Comprehensive Evaluation of Quantization Strategiesfor ...</a></li>
<li><a href="https://picovoice.ai/blog/sub-4-bit-llm-quantization/">Sub-4-Bit LLM Quantization: Enterprise Guide to Methods ...</a></li>

</ul>
</details>

**Discussion**: Sentiment is split: one commenter confirmed 124 tokens/sec on a 4090 and called it &quot;surprisingly well,&quot; while another independently benchmarked Strata against llama.cpp on a vision task and found dramatically higher error \(median 154.8px vs 46.5px\). Others were skeptical of going below 4-bit quants for quality reasons and shared alternative stacks \(llama.cpp, ds4\) that they consider more reliable, and at least one commenter complained that LLM forums are being spammed with Strata links ahead of any verified results.

**Tags**: `#llm-inference`, `#quantization`, `#local-llm`, `#gpu-optimization`, `#qwen`

---

<a id="item-2"></a>
## [GitHub script strips Apple Intelligence from macOS 27 to reclaim disk space](https://github.com/omlahore/RemoveMacAI) ⭐️ 7.0/10

A GitHub project called RemoveMacAI \(by user omlahore\) publishes a script that disables and removes Apple Intelligence from macOS 27 so users can reclaim the disk space its local AI assets occupy. The utility attracted substantial attention, scoring 360 points with 222 comments debating Apple&\#x27;s growing footprint and privacy tradeoffs. It signals that macOS users now feel they need third-party debloat scripts to regain control of system resources, a chore long associated with Windows. It also fuels a broader debate about whether Apple&\#x27;s bundled AI features — and the inability to fully switch them off with a simple toggle — represent sensible product strategy or unwanted bloatware. The script targets the on-device Apple Intelligence model files that ship with the OS and consume storage even when the feature appears disabled in System Settings. Community members note the models are relatively small and run entirely on-device rather than in the cloud, and that OS updates may simply re-download the removed assets.

hackernews · privacyisntdead · Oct 4, 19:42 · [Discussion](https://news.ycombinator.com/item?id=49957116)

**Background**: Apple Intelligence is Apple&\#x27;s collection of AI features announced on June 10, 2024, at WWDC, built into iOS 18, iPadOS 18 and macOS Sequoia, and it relies on a combination of on-device processing and server-side models. Because part of it runs locally, its model files remain on disk regardless of whether the user has opted in. Debloat utilities have long been common on Windows, with tools such as O&amp;O ShutUp10 removing telemetry and unwanted components, and this project suggests a similar culture is forming around macOS.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://discussions.apple.com/thread/255927866">How to completely remove Apple Intelligen… - Apple Community</a></li>
<li><a href="https://www.techradar.com/computing/artificial-intelligence/apple-intelligence-features-explained-everything-you-need-to-know-about-apple-ai-and-when-you-can-use-it">Apple Intelligence features explained - everything you need ...</a></li>

</ul>
</details>

**Discussion**: Sentiment was mixed and critical: some compared the situation to the de-crufting rituals Windows users have always performed, and others complained that iOS offers no simple global AI toggle unlike Microsoft and Firefox. A notable counterargument came from commenters who questioned why anyone would delete well-balanced, relatively small on-device inference models that never touch the cloud, while others drew parallels to O&amp;O ShutUp10 and wondered how Apple weighs disk-usage costs against feature benefits.

**Tags**: `#macOS`, `#Apple Intelligence`, `#privacy`, `#bloatware-removal`, `#debloat-tools`

---