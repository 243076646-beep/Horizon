---
layout: default
title: "Horizon Summary: 2026-10-19 (EN)"
date: 2026-10-19
lang: en
---

> From 13 items, 3 important content pieces were selected

---

1. [Essay argues human intent and taste remain software&\#x27;s durable value in the AI era](#item-1) ⭐️ 7.0/10
2. [RepRapMicron Brings Open-Source 3D Printing Down to Micron Scale](#item-2) ⭐️ 7.0/10
3. [DeepSeek launches hosted web search and fetch API at $0.75 per 1,000 requests](#item-3) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Essay argues human intent and taste remain software&\#x27;s durable value in the AI era](https://karrisaarinen.com/posts/someone-behind-the-software/) ⭐️ 7.0/10

Karri Saarinen \(co-founder and CEO of Linear\) published an essay titled &quot;Someone behind the software&quot; arguing that as AI takes over coding and even architectural decisions, the durable source of product value shifts to the human behind it: their intent, taste, values, and judgment about what to build and what not to build. The post resonated widely, reaching 304 points and 122 comments on Hacker News. The essay gives a vocabulary to a question many builders are now facing: if AI can write code better and faster than most engineers, what is a software professional actually being paid for? Its answer — product vision, taste, and a coherent point of view — reframes AI as a force that raises rather than erases the value of human judgment, which affects how teams organize work, hire, and evaluate product decisions. A central observation in the essay is that most product changes are additive rather than improvements to the core problem, because adding a capability is far easier than rethinking an existing one — so products drift into collections of abilities with no unified point of view. The argument is qualitative industry commentary rather than a technical claim, and notably its author leads a product company, so it doubles as a statement about how design-led software teams intend to position themselves against AI tooling.

hackernews · tosh · Oct 18, 16:32 · [Discussion](https://news.ycombinator.com/item?id=50142573)

**Background**: Large language model coding assistants and agentic tools have advanced quickly, and it is now routine for AI to generate substantial amounts of production code and to propose software architecture. That has triggered an ongoing debate in the software industry about which human skills remain scarce and valuable. The essay references Dorothy Sayers&\#x27; book &quot;The Mind of the Maker&quot;, which Fred Brooks cited in &quot;The Mythical Man-Month&quot; to divide creative work into the idea, the implementation, and the interaction — a framing several commenters picked up on.

**Discussion**: Commenters largely agreed with the thesis, with one SaaS developer saying the value now lies not in code or even architecture — where AI is catching up — but in deciding what to build and what not to build. Others extended the argument by noting that AI has no values, intent, or taste of its own, and one reader connected it to Dorothy Sayers&\#x27; three-stage model of creation \(idea, implementation, interaction\) cited by Fred Brooks; a recurring concern was that agent-based workflows encourage additive, vision-less product changes.

**Tags**: `#AI`, `#software-engineering`, `#product-design`, `#human-judgment`, `#industry-commentary`

---

<a id="item-2"></a>
## [RepRapMicron Brings Open-Source 3D Printing Down to Micron Scale](https://github.com/VikOlliver/RepRapMicron/wiki) ⭐️ 7.0/10

RepRapMicron \(μRepRap\), an open-source project led by RepRap community developer Vik Olliver, is extending the self-replicating RepRap 3D printer concept to micron-scale fabrication, with its wiki documenting custom hardware designs, toolheads, and control software. The project has already demonstrated a 3DBenchy printed at just 0.650 mm, marking tangible progress toward its stated goal of producing features down to roughly 10 microns or less. If micron-scale additive manufacturing becomes cheap and widely accessible, it could shift microchip and micro-device prototyping out of expensive cleanrooms and into the hands of hobbyists and small labs, much as RepRap once democratized desktop 3D printing. That prospect has prompted speculation about DIY chip fabrication and a new wave of open hardware innovation. The project&\#x27;s wiki details practical microfabrication workarounds, such as releasing printed parts from Krapton tape in a droplet of isopropyl alcohol and experimenting with nail gel as a material, while the team acknowledges that print quality for larger objects remains a challenge. The effort is still early-stage and evolving rather than a verified industrial breakthrough.

hackernews · RobotToaster · Oct 18, 13:48 · [Discussion](https://news.ycombinator.com/item?id=50141076)

**Background**: RepRap is a long-running open-source project that created self-replicating 3D printers, aiming to put FDM-style fabrication in anyone&\#x27;s hands at low cost. Standard desktop printers typically resolve features around 0.1–0.4 mm, whereas micron-scale fabrication \(features measured in thousandths of a millimeter\) has historically required photolithography and semiconductor-style cleanroom equipment. RepRapMicron aims to shrink the same open, hackable printer philosophy to that scale.

<details><summary>References</summary>
<ul>
<li><a href="https://reprap.org/wiki/RepRapMicron">RepRapMicron - RepRap GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ... RepRapMicron: an open-source microscale RepRap… · AGI Hunt RepRapMicron – Hackaday The Latest From RepRapMicron – Nail Gel, First Objects, And ... RepRap: Blog Shrinking the Factory: Meet RepRapMicron, the Open-Source ...</a></li>
<li><a href="https://github.com/VikOlliver/RepRapMicron">GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ...</a></li>
<li><a href="https://www.4additive.com/en/reprap-micron-3dbenchy-smallest/">RepRap Micron : the smallest 3DBenchy is 0.650 mm - 4Additive</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were enthusiastic, with one drawing parallels to late-1790s precision engineering—Ramsden&\#x27;s dividing engine, Maudslay&\#x27;s thread-cutting lathe, and Wilkinson&\#x27;s boring machine—as examples of craft becoming reliable mass production. Others joked about eventually printing their own RAM or imagined a future where chip designs could be printed cheaply and sustainably, though one commenter questioned the practicality of ever building a 1/1000-scale version of the machine itself.

**Tags**: `#RepRap`, `#3D printing`, `#microfabrication`, `#open hardware`, `#DIY manufacturing`

---

<a id="item-3"></a>
## [DeepSeek launches hosted web search and fetch API at $0.75 per 1,000 requests](https://api-docs.deepseek.com/guides/search/) ⭐️ 6.0/10

DeepSeek has published documentation for a hosted web search and page-fetch API priced at $0.75 per 1,000 successful requests. The service lets developers give LLM applications live web retrieval without building their own crawler or signing up with a separate search vendor. The price undercuts established search APIs such as Brave \(about $5 per 1,000\) and Kagi \(about $12 per 1,000\) by a wide margin, which could lower costs for agent builders who need web grounding. It also intensifies competition in a market that exists largely because Google does not offer a paid search API for third-party developers. Billing is per successful request rather than per call, so failed or empty fetches are not charged, though the documentation does not detail rate limits or crawl coverage. Competitors noted in the discussion include self-hosted SearXNG-based tools that scrape results for free, which remain an option for hobbyist and low-volume use.

hackernews · fagnerbrack · Oct 18, 06:50 · [Discussion](https://news.ycombinator.com/item?id=50138531)

**Background**: LLM agents are AI systems that combine a model core with tools, memory and planning so they can take actions such as looking things up on the web. Because model training data has a cutoff date, agents typically call a search API at inference time to retrieve current pages and ground their answers. DeepSeek is a Hangzhou-based AI company backed by the hedge fund High-Flyer, known for open-weights models such as DeepSeek-R1; offering a paid retrieval API extends it from model provider toward full agent infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.migramatters.com/llm-agents-ai-automation/">Everything About LLM Agents : The Future of AI... - MigraMatters</a></li>
<li><a href="https://developer.nvidia.com/blog/building-your-first-llm-agent-application/">Building Your First LLM Agent Application | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely focused on economics and incentives: several noted the price is far below Brave and Kagi, while one argued these services only exist because Google refuses to offer a paid search API. Others predicted that as agent-driven search grows, search API prices could eventually go negative as providers compete for control over what influences the web, and one commenter suggested self-hosted SearXNG scraping is still free for personal use and urged DeepSeek to adopt source-aware training so models can cite which facts came from which source.

**Tags**: `#search-api`, `#deepseek`, `#llm-agents`, `#api-pricing`, `#seo`

---