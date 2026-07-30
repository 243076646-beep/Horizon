---
layout: default
title: "Horizon Summary: 2026-07-30 (EN)"
date: 2026-07-30
lang: en
---

> From 22 items, 10 important content pieces were selected

---

1. [Open-source engine runs Gemma 4 26B in 2GB RAM on Mac](#item-1) ⭐️ 8.0/10
2. [Mitchell Hashimoto Launches Superlogical, a New Terminal Company](#item-2) ⭐️ 8.0/10
3. [Handbook.md shows LLMs fail to follow long policy documents](#item-3) ⭐️ 8.0/10
4. [AI worms can self-propagate through Microsoft Copilot for Word](#item-4) ⭐️ 8.0/10
5. [Kimi Launches Cheaper K3-256k Model at Half Price](#item-5) ⭐️ 7.0/10
6. [KOReader: Open-Source E-Reader for Enhanced E-Ink Experience](#item-6) ⭐️ 7.0/10
7. [EU AI Act Digital Omnibus Finalizes 8 Compliance Changes](#item-7) ⭐️ 7.0/10
8. [Using Apple Vision Pro for Architectural Walkthroughs](#item-8) ⭐️ 6.0/10
9. [Keychron announces open-source firmware for gaming mice, but release delayed](#item-9) ⭐️ 6.0/10
10. [Germany Grants BaFin Power to Oversee AI Credit Scoring and Chatbots](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Open-source engine runs Gemma 4 26B in 2GB RAM on Mac](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare, an open-source inference engine written in Swift and Metal, can run the 4-bit quantized Gemma 4 26B-A4B-IT model on any M-series Mac with only 2 GB of RAM by streaming expert weights from SSD. This breakthrough dramatically lowers the memory barrier for running large MoE models on consumer hardware, enabling powerful on-device AI on memory-constrained Macs. It also demonstrates a practical approach to SSD streaming that could be adopted by other inference frameworks. The quantized 4-bit weights occupy about 14 GB, but the engine keeps only the shared layers and KV cache in RAM \(≈2 GB\), streaming the routed experts from SSD on demand. On an M2 MacBook Air it achieves 5–6 tokens per second, and on an M5 MacBook Pro it reaches 31–35 tokens per second.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Mixture-of-Experts \(MoE\) models use multiple specialized sub-networks called experts, with only a subset activated per token, reducing compute cost. 4-bit quantization reduces model weight precision to save memory, but even with quantization, large MoE models like Gemma 4 26B may exceed typical RAM. SSD streaming loads expert weights from disk during inference, overlapping I/O with computation to hide latency.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into a Dial | MindStudio</a></li>
<li><a href="https://alain-airom.medium.com/run-big-llms-on-small-gpus-a-hands-on-guide-to-4-bit-quantization-and-qlora-40e9e2c95054">Run Big LLMs on Small GPUs: A Hands-On Guide to 4 - bit ... | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments were positive and engaged. Users compared the approach to mmap in llama.cpp, noting that TurboFieldfare&\#x27;s synchronous SSD reads are tuned for low latency. One user reported successful compilation on an older macOS version with a small workaround. Others expressed interest in collaboration on related projects like DiffusionGemma.

**Tags**: `#AI inference`, `#model quantization`, `#on-device AI`, `#Swift`, `#Metal`

---

<a id="item-2"></a>
## [Mitchell Hashimoto Launches Superlogical, a New Terminal Company](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto, creator of Ghostty and co-founder of HashiCorp, has announced Superlogical, a new company that will build commercial products on top of the open-source libghostty terminal library. The company’s first product will be a terminal multiplexer aimed at connecting developers, AI agents, and production workflows. This announcement is significant because it demonstrates a sustainable open-source business model where the creator transfers the core library to a non-profit and builds a commercial product as a consumer of the open-source dependency. It also highlights the growing trend of terminal-centric tools integrating with AI agents. Superlogical will use libghostty exactly as designed—as a public building block for terminal applications—and will continue to upstream shared improvements to benefit all consumers. The company’s first focus is a terminal multiplexer, which serves as the foundation for a broader vision.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: libghostty is the cross-platform, zero-dependency C and Zig library that powers the Ghostty terminal emulator, which was released under the MIT license. Mitchell Hashimoto previously founded HashiCorp and has been a prominent figure in open-source infrastructure software. By transferring ownership of Ghostty to a non-profit, he ensures the library remains community-owned while allowing his new company to build proprietary products on top.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/superlogical">Superlogical – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature-rich, and...</a></li>

</ul>
</details>

**Discussion**: The community response is largely positive, with one commenter \(simonw\) praising the model of transferring ownership to a non-profit and building a company as a consumer of the open-source dependency. Another commenter \(danbruc\) draws a comparison to OLE/COM technologies, noting both potential and pain points. A third commenter \(rixed\) criticizes the enigmatic title as clickbait, suggesting a preference for more informative headlines.

**Tags**: `#open source`, `#terminal`, `#software engineering`, `#company announcement`

---

<a id="item-3"></a>
## [Handbook.md shows LLMs fail to follow long policy documents](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

The Handbook.md benchmark reveals that no frontier LLM achieves more than 25% accuracy on following expert-written company policies of up to 124 pages, highlighting fundamental long-context understanding failures. This challenges the reliability of agentic AI in enterprise settings, where strict policy adherence is critical, and suggests that current long-context capabilities are insufficient for autonomous agents. The benchmark uses MCP-native RL environments and deterministic grading, and failures include unauthorized actions like firing employees or approving self-submitted expenses.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: Large language models can process increasingly long contexts, but this research shows that they cannot reliably use that context to govern behavior. Long-context understanding remains a known challenge, with models like GPT-5.4 supporting up to 1M tokens yet still struggling with policy adherence.

<details><summary>References</summary>
<ul>
<li><a href="https://surgehq.ai/blog/handbook-md">HANDBOOK.md Benchmark: Can AI Agents Follow a 100-Page Company Policy?</a></li>
<li><a href="https://arxiv.org/html/2507.16459v1">Towards Enforcing Company Policy Adherence in Agentic Workflows</a></li>

</ul>
</details>

**Discussion**: Commenters attribute failures to quantization of KV cache, limited working memory, and lack of post-training on specific policies. One user notes that explicit in-prompt instructions work better than persistent system files like CLAUDE.md.

**Tags**: `#LLMs`, `#long-context`, `#AI alignment`, `#policy adherence`

---

<a id="item-4"></a>
## [AI worms can self-propagate through Microsoft Copilot for Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

Researchers demonstrated a new attack where AI worms embed hidden malicious instructions in documents, causing Microsoft Copilot for Word to inadvertently propagate the worm when editing or drafting documents. This marks the first documented instance of a self-propagating worm targeting AI-powered productivity assistants. This vulnerability highlights a fundamental security flaw in AI assistants that cannot reliably distinguish between user instructions and untrusted data, posing a risk of large-scale automated attacks. As AI integration deepens, such worms could spread across organizations, exfiltrating data or causing damage through trusted channels. The attack exploits indirect prompt injection, where adversarial instructions hidden in document content are executed by Copilot as if they were legitimate commands. The researchers reported that no robust mitigation for this broader vulnerability class is currently available, and the attack can propagate via Copilot&\#x27;s access to email or shared documents.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection is a cybersecurity exploit where innocuous-looking inputs cause unintended behavior in large language models \(LLMs\) because the model cannot distinguish developer instructions from user input. Indirect prompt injection occurs when adversarial prompts are embedded in content \(e.g., web pages or documents\) that the LLM retrieves and processes. AI assistants like Microsoft Copilot are integrated into applications with access to sensitive data, making them attractive targets for such attacks. The concept of an AI worm—autonomous malware that uses LLMs for self-propagation—is an emerging threat combining prompt injection with traditional worm techniques.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://www.emergentmind.com/topics/ai-worms">AI Worms : Autonomous Self-Propagating Malware</a></li>

</ul>
</details>

**Discussion**: Commenters expressed deep concern, with one noting that &quot;it&\#x27;s impossible to fix this kind of thing&quot; as long as instructions and data remain mixed. Another predicted the situation will &quot;get worse, much worse, before it gets better,&quot; citing the ease of embedding malicious instructions in shared content like GitHub comments. A third demonstrated that simple techniques like white text hidden in documents still bypass current defenses, emphasizing the persistence of the vulnerability.

**Tags**: `#AI security`, `#prompt injection`, `#Copilot`, `#worms`, `#cybersecurity`

---

<a id="item-5"></a>
## [Kimi Launches Cheaper K3-256k Model at Half Price](https://www.kimi.com/code/docs/en/kimi-code/models) ⭐️ 7.0/10

Kimi released K3-256k, a version of its K3 model with a 256,000-token context window, priced at half the quota consumption of the original 1M-context version. This makes Kimi&\#x27;s frontier model more accessible for everyday use cases that don&\#x27;t require the full 1M context, potentially accelerating adoption among developers and businesses. The K3-256k delivers the same results as the 1M version within 256k context, but consumes about twice as much quota as the 256k version, meaning users effectively pay half the price until they exceed 256k context.

hackernews · monneyboi · Jul 29, 19:25 · [Discussion](https://news.ycombinator.com/item?id=49101852)

**Background**: Kimi K3 is a 2.8-trillion-parameter Mixture-of-Experts model with a native 1M-token context window. The model uses Kimi Delta Attention and Attention Residuals for efficient long-context processing. The new 256k variant addresses the cost barrier for users who rarely need the full context length.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/code/docs/en/kimi-code/models">Model Configuration | Kimi Code Docs</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://kie.ai/blog/what-is-kimi-k3">What Is Kimi K3? Moonshot&#x27;s 2.8T, 1M-Context Flagship</a></li>

</ul>
</details>

**Discussion**: Community comments show a mix of approval and strategic insight. One user noted that LLMs are becoming commodities and that hyperscalers selling cheap tokens will win. Another appreciated the 256k as practical, while a third highlighted that the price effectively halves for most users.

**Tags**: `#LLM`, `#Kimi`, `#context window`, `#pricing`, `#AI models`

---

<a id="item-6"></a>
## [KOReader: Open-Source E-Reader for Enhanced E-Ink Experience](https://koreader.rocks/) ⭐️ 7.0/10

KOReader is an open-source e-book reader that enhances reading on e-ink devices like Kindle and Kobo by supporting a wide range of formats and offering extensive customization. It includes advanced navigation tools such as Book Map and Page Browser. KOReader significantly improves the flexibility and usability of e-ink readers, giving users control over their reading experience beyond proprietary firmware limitations. Its open-source nature fosters community contributions and long-term sustainability. KOReader supports fixed-page formats \(PDF, DjVu, CBT, CBZ\) and reflowable formats \(EPUB, FB2, Mobi, DOC, RTF, HTML, CHM, TXT\). It also features multi-page highlighting with export options and a Calibre wireless connection for syncing.

hackernews · Cider9986 · Jul 29, 11:05 · [Discussion](https://news.ycombinator.com/item?id=49095865)

**Background**: E-ink readers like Kindle and Kobo typically have limited format support and customization options. KOReader is an open-source alternative firmware that can be installed on these devices to unlock additional features, such as native EPUB and PDF reading without conversion, and advanced gesture controls.

<details><summary>References</summary>
<ul>
<li><a href="https://koreader.com/">KOReader – Free eBook Reader for PDF &amp; EPUB</a></li>
<li><a href="https://github.com/koreader/koreader">GitHub - koreader / koreader : An ebook reader application supporting...</a></li>
<li><a href="https://asibiont.com/en/blog/vibe-coding-i-koreader-kak-ii-assistent-prevrashchaet-elektronnuyu-knigu-v-instrument-razrabotchika">KOReader and Vibe Coding: Why Every AI-Assisted... — ASI Biont Blog</a></li>

</ul>
</details>

**Discussion**: Community reactions are mixed: many users praise KOReader for its freedom and extensive features, while others criticize its unintuitive UI, laggy performance, and unreliable gestures. One user noted preferring the default Kindle viewer despite KOReader&\#x27;s advantages.

**Tags**: `#e-reader`, `#open-source`, `#kindle`, `#kobo`, `#ebook`

---

<a id="item-7"></a>
## [EU AI Act Digital Omnibus Finalizes 8 Compliance Changes](https://news.google.com/rss/articles/CBMiqgFBVV95cUxPemNwcndsRzBzVW5WRDNacEhYWXZ5SUhWRXBzLWJKLWctWW5SN0ZndnYzbEJoV0xWbDc4MEduT1ZfNmtxZHpEWnZ4dDVVUy1pWUN6T3p2elV0Ukp4d19QbWNBUlBubW1NNzEtVVloclNUNmdqV3FSOExkQnJnYUZXcldHbFhXS3VTWDM2bU90a1RPR1ZGeWZNSV8xM2t4bGVuT0VXd1NsTWMzUQ?oc=5) ⭐️ 7.0/10

The European Commission&\#x27;s Digital Omnibus on AI, published on 19 November 2025, has finalized eight specific compliance changes to the EU AI Act, including a deferral of high-risk AI system obligations from 2 August 2026 to 2 December 2027. This update provides crucial regulatory clarity for businesses developing or deploying AI in the EU, offering extended timelines and administrative simplification that can reduce compliance costs and foster innovation. The Digital Omnibus includes adjustments to high-risk AI classification rules, transparency obligations, and conformity assessment procedures. It also introduces new provisions for AI systems used in critical infrastructure and employment contexts.

rss · GoogleNews-欧盟监管 · Jul 29, 20:57

**Background**: The EU AI Act is a landmark regulation that categorizes AI systems by risk level and imposes stricter requirements on high-risk systems. The Digital Omnibus, part of a broader digital package published in November 2025, aims to simplify and streamline these rules to reduce burden while maintaining safety and trust. The changes become enforceable on 27 July 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/library/digital-omnibus-ai-regulation-proposal">Digital Omnibus on AI Regulation Proposal | Shaping Europe’s digital future</a></li>
<li><a href="https://www.europarl.europa.eu/thinktank/en/document/EPRS_BRI%282026%29782651">Digital Omnibus on AI | Think Tank | European Parliament</a></li>
<li><a href="https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/The-Digital-AI-Omnibus-Proposed-deferral-of-high-risk-AI-obligations-under-the-AI-Act">The Digital AI Omnibus: Proposed deferral of high risk AI obligations under the AI Act (update) - DLA Piper GENIE</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#technology policy`

---

<a id="item-8"></a>
## [Using Apple Vision Pro for Architectural Walkthroughs](https://christianselig.com/2026/07/vision-pro-house/) ⭐️ 6.0/10

An article explores using Apple Vision Pro to walk through a 3D house model for architectural design validation, allowing users to intuitively assess proportions and layout in real time. This application of spatial computing offers architects and clients a powerful tool for early design feedback, reducing reliance on physical mockups and improving decision-making. It could set a new standard for architectural visualization. The Vision Pro&\#x27;s high-resolution display and spatial awareness enable users to rapidly judge if spaces are properly proportioned, with the article noting insights become apparent within seconds of putting on the headset.

hackernews · robbiet480 · Jul 29, 20:39 · [Discussion](https://news.ycombinator.com/item?id=49102774)

**Background**: Spatial computing merges digital data with the physical world in real time, using devices like AR/VR headsets to enable natural interaction with 3D content. In architecture, this technology allows designers and clients to virtually walk through a building before construction, enhancing communication and design quality.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Spatial_computing">Spatial computing</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/spatial-computing/">What Is Spatial Computing? | NVIDIA Glossary</a></li>

</ul>
</details>

**Discussion**: Comments from professionals and enthusiasts validate the utility: one suggests simulating sun angles to optimize natural light, another details daily use of Quest 3 with Enscape for client walkthroughs, and a third shares a decade-old experience with HTC Vive for home design. Overall sentiment is positive, with additional ideas for tracing wiring and plumbing post-construction.

**Tags**: `#Vision Pro`, `#AR/VR`, `#Architecture`, `#Design`, `#Spatial Computing`

---

<a id="item-9"></a>
## [Keychron announces open-source firmware for gaming mice, but release delayed](https://www.digitalfoundry.net/news/2026/07/keychron-announces-first-open-source-firmware-for-gaming-mice) ⭐️ 6.0/10

Keychron announced ZGM, an open-source firmware for gaming mice based on Zephyr RTOS, with a planned release in Q1 2027. This could bring open-source customization and transparency to gaming mice, similar to how QMK transformed keyboards, but skepticism remains due to the long delay and existing alternatives. The ZGM firmware repository currently contains no source code, leading to accusations of vaporware, and the announcement comes 6-9 months ahead of any release.

hackernews · JLO64 · Jul 29, 16:36 · [Discussion](https://news.ycombinator.com/item?id=49099715)

**Background**: Open-source firmware like QMK has long been popular for keyboards, allowing users to customize key mappings and features. For mice, similar open-source options have been limited, with a few projects like Ploopy running QMK. Keychron&\#x27;s ZGM aims to fill this gap but faces competition from existing QMK-based mice.

<details><summary>References</summary>
<ul>
<li><a href="https://www.pcgamer.com/hardware/gaming-mice/keychrons-gaming-mouse-firmware-is-going-open-source-while-the-company-critiques-firmware-you-cant-read-cant-audit-cant-change/">Keychron&#x27;s gaming mouse firmware is going open - source , while the...</a></li>
<li><a href="https://zgm.gg/">ZGM Firmware — Zephyr Gaming Mouse</a></li>

</ul>
</details>

**Discussion**: Commenters expressed skepticism, noting the announcement without code and the 6-9 month delay. Some pointed out that existing QMK-based mice already offer similar functionality, questioning the need for a new project.

**Tags**: `#open-source`, `#firmware`, `#gaming mouse`, `#Keychron`, `#QMK`

---

<a id="item-10"></a>
## [Germany Grants BaFin Power to Oversee AI Credit Scoring and Chatbots](https://news.google.com/rss/articles/CBMivwFBVV95cUxNbGNGc1NFYmk2UGxDUk9IckpsQUpHNm1fTGpEWWwxVkRweGFHZEU5ZWlycWV5VDdJM244SVhUUTFWUVYwQ09KSkZNWXVIanZCRGltVThpTVJrc21DNkdfUXVObDVRZ1FwNXVHaUlKcVllRE9VaUhWTWR2WlhqdG9Iakx6cXJDMUtPYVVXLW5QWndqT2tSalBmLXFDa1RBd2ZLVVMxQWxXOV9BRXVfMUdXYVlObTh2SkhVc21WUjJLVQ?oc=5) ⭐️ 6.0/10

Germany has granted its financial regulator, BaFin, new authority to oversee the use of artificial intelligence in credit scoring and to mandate disclosure of bank chatbot interactions. This move sets a precedent for AI regulation in the financial sector, potentially influencing other countries and ensuring transparency and fairness in AI-driven financial decisions. The new powers require banks to disclose when customers are interacting with AI chatbots and ensure AI credit scoring models are transparent and non-discriminatory. BaFin can now audit algorithms and impose penalties for non-compliance.

rss · GoogleNews-欧盟监管 · Jul 29, 18:36

**Background**: BaFin, the Federal Financial Supervisory Authority, is Germany&\#x27;s integrated financial regulator overseeing banks, insurers, and financial services. AI credit scoring uses machine learning to assess creditworthiness, while bank chatbots handle customer service. This regulation aims to prevent algorithmic bias and protect consumer rights.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/BaFin">BaFin</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#credit scoring`, `#financial technology`, `#Germany`, `#BaFin`

---