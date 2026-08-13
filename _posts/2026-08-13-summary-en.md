---
layout: default
title: "Horizon Summary: 2026-08-13 (EN)"
date: 2026-08-13
lang: en
---

> From 17 items, 6 important content pieces were selected

---

1. [OpenAI and Cerebras Unveil GPT-5.6 Sol Ultrafast with 7x Faster Inference](#item-1) ⭐️ 9.0/10
2. [Spaghettifying DRAM: Tool Unlocks CPU Protected Memory via Scrambling](#item-2) ⭐️ 9.0/10
3. [Google Introduces Gemini 3.7 Flash, Its Cost-Effective Workhorse AI Model](#item-3) ⭐️ 8.0/10
4. [DeepSeek Releases Open-Source Agent Harness with Session Traceability](#item-4) ⭐️ 8.0/10
5. [EU AI Act Requires Chatbots to Disclose They Are Not Human](#item-5) ⭐️ 7.0/10
6. [Test Shopify Checkout Tracking Before Aug 26 Upgrade](#item-6) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI and Cerebras Unveil GPT-5.6 Sol Ultrafast with 7x Faster Inference](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 9.0/10

OpenAI and Cerebras announced GPT-5.6 Sol Ultrafast, a new service tier running OpenAI&\#x27;s reasoning model on Cerebras wafer-scale hardware. It answered all 2,500 HLE benchmark questions in 11 hours 11 minutes — nearly 7x faster than Claude Fable 5&\#x27;s 78 hours 27 minutes — and delivers up to 14x speedup over Standard processing in the OpenAI API. This marks a major milestone in frontier AI inference speed: economically valuable knowledge work such as legal briefs, financial models, and engineering reports can now be completed in hours rather than days without sacrificing accuracy. It demonstrates that specialized silicon like Cerebras&\#x27; wafer-scale engine can meaningfully change the cost and latency calculus for the most demanding reasoning models. On GDP-Val, a benchmark for economically valuable knowledge work, Ultrafast delivered a 5.6x end-to-end speedup with no quality degradation. The service launches first in the OpenAI API; pricing and general availability have not yet been announced, and some community members note that OpenAI and Cerebras have not explicitly confirmed that Ultrafast produces identical outputs to standard GPT-5.6 Sol.

hackernews · pr337h4m · Aug 13, 18:10 · [Discussion](https://news.ycombinator.com/item?id=49289844)

**Background**: Cerebras builds the Wafer-Scale Engine \(WSE-3\), the world&\#x27;s largest AI processor — a single chip with 4 trillion transistors, 900,000 AI-optimized cores, and 44GB of on-chip SRAM delivering over 21 PB/s of memory bandwidth. HLE and GDP-Val are frontier reasoning benchmarks that measure models against expert-level, open-ended knowledge work, where even the best models often score low. This announcement follows the GPT-5.6 release in July 2026 and highlights how specialized inference hardware is becoming an increasingly important part of the LLM ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai">Accelerating GPT-5.6 Sol Ultrafast with OpenAI</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode: GPT-5.6 Sol at up to 14X the speed | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community reaction is broadly enthusiastic — commenters call the 7x speedup &\#x27;amazing&\#x27; and hope for broader availability and consumer hardware — but there is meaningful skepticism. Some, like Topfi, point out that neither OpenAI nor Cerebras firmly states that Ultrafast achieves identical quality to standard GPT-5.6 Sol, and csallen argues speed itself improves thinking quality by enabling iterative revision, while GodelNumbering notes the absence of pricing information in the OpenAI announcement.

**Tags**: `#AI`, `#LLM`, `#OpenAI`, `#Cerebras`, `#Performance`

---

<a id="item-2"></a>
## [Spaghettifying DRAM: Tool Unlocks CPU Protected Memory via Scrambling](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Security researcher Christopher Domas released &\#x27;skitter-creek-bath-salts&\#x27;, a hardware security tool that exploits DRAM addressing and row semantics to reverse the undocumented address scrambling on AMD Jaguar \(AMD16h\) CPUs. Using the z3 solver, it generates &\#x27;spaghettified&\#x27; alias addresses that reach protected memory including PSP private memory, SMRAM, and the C6 idle-state. This matters because it turns ring-0 access into a way to bypass the platform&\#x27;s elaborate memory fences and security checks, exposing areas that are normally hidden even from privileged software. It challenges the assumption that DRAM address scrambling can be used as an obscurity-based security boundary, with potential implications for consoles and other AMD-based systems. The current proof of concept targets the AMD16h \(Jaguar\) family from 2013; Zen 3 is noted to use a different base address for memory controller registers, so the exploit does not directly carry over. The tool uses z3 to turn any coherent-view address into an alias in the scrambled view, bypassing locks and fences without triggering platform security checks.

hackernews · matt\_d · Aug 13, 14:17 · [Discussion](https://news.ycombinator.com/item?id=49286341)

**Background**: DRAM is organized into rows and columns, and modern memory controllers apply undocumented &\#x27;scrambling&\#x27; functions that obfuscate how physical addresses map to actual DRAM cells \(row, column, bank, bank-group\). This scrambling is normally invisible to software, and platforms rely on it as part of their security posture. The project&\#x27;s name plays on &\#x27;spaghettification&\#x27; in astrophysics, but here it refers to turning the normal coherent memory view into a twisted, scrambled one. Once the scrambling transform is solved, a protected target address can be reached from an uncontrolled alias, unlocking everything from PSP private memory to SMRAM.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49286341">Spaghettifying DRAM | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spaghettification">Spaghettification - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters are highly enthusiastic, praising the research and eagerly awaiting the Black Hat talk, with several recommending Christopher Domas&\#x27;s earlier talks. Others note that DRAM has become so complex that a huge attack surface is unsurprising, and that Xbox/PlayStation security teams should be worried. A few users ask which modern CPUs are actually affected, pointing out that AMD Jaguar is from 2013 and Zen 3 has a different memory controller base address.

**Tags**: `#DRAM`, `#hardware security`, `#reverse engineering`, `#exploit`, `#security research`

---

<a id="item-3"></a>
## [Google Introduces Gemini 3.7 Flash, Its Cost-Effective Workhorse AI Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

Google announced Gemini 3.7 Flash, a new cost-efficient model in its Flash lineup, built on Gemini 3.6 Flash and described as its &\#x27;most intelligent workhorse model.&\#x27; Starting today, it powers Gemini Spark, available to Google AI Pro and Ultra subscribers in more than 160 countries. The release strengthens Google&\#x27;s competitive position in the fast-moving AI model market by targeting low-cost, high-throughput workloads. Developers and businesses weighing price and performance against rivals such as OpenAI&\#x27;s GPT-5.6 Luna and Anthropic&\#x27;s Opus will be directly affected. The model carries &\#x27;introductory pricing&\#x27; that is scheduled to double at the end of 2026; starting January 1, 2027, input tokens will cost $1.50 per million and output tokens $7.50 per million. Community tests note strong vision-to-HTML performance but also point out the rapid cadence of Flash updates, with 3.6 Flash arriving just three weeks earlier.

hackernews · thisisauserid · Aug 13, 17:23 · [Discussion](https://news.ycombinator.com/item?id=49289112)

**Background**: Gemini is Google DeepMind&\#x27;s family of multimodal large language models, first announced on December 6, 2023, and the underlying technology for the Gemini chatbot. The Flash line is designed to be a smaller, faster and cheaper tier for high-volume, text-heavy and agentic use cases, complementing larger flagship models. Google says Gemini 3.7 Flash improves on its predecessor, Gemini 3.6 Flash, which the model card lists as its base.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3 . 7 Flash : our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3 . 7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_2.5_Flash_Image">Gemini 2.5 Flash Image</a></li>

</ul>
</details>

**Discussion**: Community reactions are mixed: some praise the model&\#x27;s vision-to-HTML quality and value, with one tester saying Opus remains class-leading but Gemini 3.7 performs well &\#x27;vs a more comparable LLM price wise.&\#x27; Others criticize the pricing plan and the speed of Flash releases, and several argue that OpenAI&\#x27;s GPT-5.6 Luna is cheaper and stronger on benchmarks like DeepSWE 1.1, undercutting the need for Flash.

**Tags**: `#AI`, `#Gemini`, `#Google`, `#Machine Learning`, `#Model Release`

---

<a id="item-4"></a>
## [DeepSeek Releases Open-Source Agent Harness with Session Traceability](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek released DeepSeek Harness as an early open-source developer preview under the MIT license. It provides full session traceability through append-only session logs, replay, fork, search, and plugin capabilities. This release gives developers a transparent, traceable agent harness that records everything the model sees, which is rare among proprietary US models that encrypt or obfuscate traces. The open-source MIT license and plugin architecture could accelerate community-driven development of AI agent tooling. The harness uses an everything-as-a-plugin architecture built on Cordis v4, enabling hot-reload and dynamic enable/dispose of plugins, including UI components and side-effect cleanup. The Trajectory view lets you inspect records by source, and resume, fork, search, and replay all operate on the same event stream.

hackernews · bjin · Aug 13, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49285244)

**Background**: An agent harness is the software infrastructure surrounding an LLM that enables it to act as an AI agent, managing tool use, memory, state persistence, and feedback loops. Because LLMs are stateless and produce only text, the harness is essential for multi-step, tool-oriented, or long-running tasks. Session traceability and replay are key observability features that help developers debug and evaluate agent behavior; tools like LangSmith and Telerik emphasize tracing and replaying complete agent sessions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness</a></li>
<li><a href="https://www.truefoundry.com/blog/ai-agent-observability-tools">AI Agent Observability: Monitoring and Debugging Agent Workflows</a></li>

</ul>
</details>

**Discussion**: Community reaction is mostly positive, with one author \(tianyicui\) welcoming feedback and noting the MIT-licensed preview will have rough edges. SwellJoe praised the traceability feature as a &quot;killer feature&quot; that US models don&\#x27;t allow due to encrypted traces, while lxdlam provided a more measured read of the paper&\#x27;s value. Others expressed plugin fatigue and skepticism about the everything-is-a-plugin architecture, and ef2k highlighted the underlying Cordis v4 hot-reload capabilities.

**Tags**: `#DeepSeek`, `#AI agents`, `#open-source`, `#traceability`, `#developer tools`

---

<a id="item-5"></a>
## [EU AI Act Requires Chatbots to Disclose They Are Not Human](https://news.google.com/rss/articles/CBMilgFBVV95cUxQdnd1MFV1VkVBQTg0YTFfUTNNTzZ5NGRVSmpnOHZwcnphTXRqR1BpSnNObG9COXhvb0N1R0hleEJhQTdYRWFVcHFNNS1yYmo3TExNVmZUZVZyVUYtZmFZdHp5emFzVmdpRURsb09JNVo2bHlWckU0MV9GdUlZTTVvWWEyRC1WSGpwcHNYa1lOLVpmYXRyZXc?oc=5) ⭐️ 7.0/10

The EU AI Act&\#x27;s transparency obligations under Article 50 now require providers and deployers of chatbots to clearly inform users when they are interacting with an AI system rather than a human. The rules take effect in August 2026, while the Act itself entered into force on 1 August 2024. This mandates explicit disclosure for virtually all customer-facing chatbots in the EU, affecting developers and companies worldwide if they serve EU users. It establishes a compliance obligation that may set a global precedent for AI transparency. Article 50 transparency obligations apply to limited-risk AI systems, not only high-risk ones, so even a customer-facing chatbot triggers the disclosure duty. The rules take effect in August 2026, giving organizations time to adapt.

rss · GoogleNews-欧盟监管 · Aug 13, 00:35

**Background**: The EU AI Act is a comprehensive regulation for artificial intelligence that entered into force on 1 August 2024 and will apply gradually over the following 6 to 36 months. It classifies AI systems by risk level: unacceptable, high, limited, and minimal, with limited-risk systems like chatbots subject only to transparency obligations, not full conformity assessments. The Act can also apply extraterritorially to providers outside the EU if they have users within the EU.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://artificialintelligenceact.eu/transparency-rules-article-50/">The EU AI Act’s Transparency Rules: A Practical Guide to Article 50 | EU Artificial Intelligence Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe&#x27;s digital future - European Union</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#regulation`, `#chatbot`, `#transparency`, `#AI policy`

---

<a id="item-6"></a>
## [Test Shopify Checkout Tracking Before Aug 26 Upgrade](https://www.reddit.com/r/ecommerce/comments/1vnllmz/before_shopifys_aug_26_checkout_upgrade_test_one/) ⭐️ 7.0/10

Shopify merchants on non-Plus stores are being urged to run a documented test order before the August 26 upgrade to the Thank you and Order status pages, to verify that purchase events are correctly received by conversion platforms like Meta, GA4, and Google Ads. The upgrade could silently break conversion tracking, leaving advertisers blind to which ads drive sales and undermining campaign optimization. Testing now gives merchants time to fix issues and avoid revenue loss after the switch. The test involves placing a test order, watching the purchase request in the browser Network tab or in server logs, and confirming the event in Meta&\#x27;s Test Events or GA4&\#x27;s DebugView. Merchants should record the event&\#x27;s value, currency, timestamp, and order/event ID, then repeat the test after the upgrade.

reddit · r/ecommerce · /u/BTWigley · Aug 13, 20:00

**Background**: Shopify&\#x27;s Thank you and Order status pages are where purchase confirmation and tracking scripts run. Conversion platforms rely on these pages to fire purchase events, either client-side through pixels or server-side via APIs. GA4 DebugView and Meta Test Events are tools that allow marketers to see real-time events as received by the platforms, helping verify tracking accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jonloomer.com/how-to-test-meta-conversion-events/">How to Test Meta Conversion Events - Jon Loomer Digital</a></li>
<li><a href="https://www.conversios.io/blog/how-to-use-debugview-in-ga4/">How to Use DebugView in GA 4 : Step-by-Step Guide</a></li>
<li><a href="https://dev.to/codesphere/introduction-to-server-side-tracking-2pjc">Introduction to Server Side tracking - DEV Community</a></li>

</ul>
</details>

**Tags**: `#Shopify`, `#E-commerce`, `#Conversion Tracking`, `#Analytics`, `#Checkout`

---