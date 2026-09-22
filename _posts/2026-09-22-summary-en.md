---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 17 items, 4 important content pieces were selected

---

1. [Xiaomi releases MiMo v2.6 open-weights MoE model family](#item-1) ⭐️ 8.0/10
2. [NASA Cancels Its Mars Sample Return Mission](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill&\#x27;s Retrospective: What Sun Microsystems Got Wrong](#item-3) ⭐️ 8.0/10
4. [Essay Argues Attention Is Computing&\#x27;s Scarcest Resource](#item-4) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Xiaomi releases MiMo v2.6 open-weights MoE model family](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

Xiaomi has released MiMo v2.6, a large open-weights Mixture-of-Experts model family, with MiMo v2.6 Pro at 1.02T total / 42B activated parameters and MiMo v2.6 Flash at 309B total / 15B activated parameters. The release ships with a detailed technical report and a realtime reinforcement-learning training dashboard, and the weights are published on Hugging Face as MiMo-V2.6-Pro-RL and MiMo-V2.6-Flash-RL. This is a frontier-scale open-weights release from a Chinese consumer-hardware company, continuing the pattern of Chinese labs \(DeepSeek, Alibaba&\#x27;s Qwen, Moonshot, Z.ai\) publishing permissively licensed large models while most leading US labs keep their largest models proprietary. The unusually transparent training methodology and public RL dashboard give researchers and hobbyists a rare look inside how a trillion-parameter model is actually trained, and the community reaction suggests affordability and openness are becoming key competitive factors. Because it is a Mixture-of-Experts architecture, only a small slice of the total parameters \(42B of 1.02T for Pro, 15B of 309B for Flash\) is activated per token, which keeps inference and training compute far lower than a dense model of comparable total size. The released checkpoints carry an &quot;-RL&quot; suffix, indicating they are the reinforcement-learning-tuned variants, and the tech report is described as unusually comprehensive about methodology.

hackernews · volf\_ · Sep 21, 20:12 · [Discussion](https://news.ycombinator.com/item?id=49792730)

**Background**: Mixture-of-Experts \(MoE\) is a machine-learning technique that splits a model into many specialized sub-networks, or &quot;experts,&quot; plus a router that selects only the relevant experts for each input; this lets a model scale to a huge total parameter count while spending compute on just a fraction of it per token. &quot;Open weights&quot; means the trained parameters of a model are publicly downloadable, allowing others to run, fine-tune or redistribute the model, though this is not the same as fully open-source AI, which would also include training code, data and intermediate checkpoints. The term is politically loaded: Chinese labs have generally favored open-weights releases under permissive licenses such as Apache or MIT, while major US labs tend to keep their largest models proprietary.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open_weights">Open weights</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>

</ul>
</details>

**Discussion**: Commenters broadly praised Xiaomi&\#x27;s transparency, with one calling the realtime RL training dashboard &quot;an incredible learning and teaching tool&quot; and the tech report unusually comprehensive. Several users said they are now more excited about Chinese models than American ones, citing affordability as the decisive factor, while others dug into the model&\#x27;s quirks, such as its fondness for the &quot;01 - UPPERCASE TEXT&quot; design motif and the standard pelican SVG rendering test.

**Tags**: `#LLM`, `#open-weights`, `#Xiaomi`, `#Mixture-of-Experts`, `#model-release`

---

<a id="item-2"></a>
## [NASA Cancels Its Mars Sample Return Mission](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

NASA has cancelled the Mars Sample Return \(MSR\) campaign, the multi-mission NASA-ESA effort that was supposed to retrieve the rock, soil and atmosphere samples that the Perseverance rover has been caching on Mars since 2021. The decision effectively ends a flagship planetary science program that had been in planning for years and was formally approved in 2022. MSR was widely regarded as the highest-priority goal in planetary science, and its cancellation leaves China&\#x27;s Tianwen-3 — planned to launch in 2028 and return samples around 2031 — potentially as the first successful Mars sample return, a prospect some observers call a possible &quot;Sputnik moment&quot; for the United States. The decision also reshapes JPL&\#x27;s mission portfolio and the NASA-ESA partnership around Mars exploration. The program&\#x27;s cost estimate had ballooned from roughly $4 billion to between $8 billion and $11 billion, with sample delivery slipping to around 2040, and the architecture was designed around ESA&\#x27;s Earth Return Orbiter and legacy launchers such as Ariane 64 rather than newer heavy-lift vehicles. For scale, the Apollo astronauts brought back 842 pounds \(about 382 kg\) of Moon rocks, whereas the Perseverance cache contains on the order of a few hundred grams of Martian material.

hackernews · Muhammad523 · Sep 21, 19:14 · [Discussion](https://news.ycombinator.com/item?id=49791939)

**Background**: A Mars sample-return mission aims to robotically collect Martian rock, soil and atmospheric material and bring it to Earth, where laboratories with far more sensitive instruments can analyze it — particularly for biosignatures that might indicate past life on Mars. NASA&\#x27;s Perseverance rover, built and operated by the Jet Propulsion Laboratory \(JPL\), has been sealing those samples in tubes on the Martian surface in anticipation of a later retrieval mission. The risk of back-contamination of Earth&\#x27;s biosphere from returned Martian samples has been raised by researchers but is generally considered low by space agencies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tianwen-3">Tianwen-3 - Wikipedia</a></li>
<li><a href="https://www.space.com/astronomy/mars/china-on-track-to-launch-mars-sample-return-mission-in-2028-if-accurate-this-represents-a-sputnik-moment">China on track to launch Mars sample-return mission in 2028: &#x27;If accurate, this represents a Sputnik moment&#x27; | Space</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed the cancellation was driven by financial unfeasibility and JPL mismanagement, pointing to the $11 billion price tag and the 2040 sample-return date, with some arguing the mission should have been designed around cheaper commercial heavy-lift rockets such as Starship or New Glenn. Several readers pushed back on the article&\#x27;s framing, calling it self-pitying advocacy from institutions that benefited from the old NASA funding model, while others highlighted China&\#x27;s parallel Tianwen-3 program and shared personal experience of repeated delays, such as on the ExoMars Rosalind Franklin rover.

**Tags**: `#NASA`, `#Mars Sample Return`, `#space exploration`, `#policy`, `#JPL`

---

<a id="item-3"></a>
## [Bryan Cantrill&\#x27;s Retrospective: What Sun Microsystems Got Wrong](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill, a former Sun Microsystems engineer and co-creator of DTrace, published an essay titled &quot;What Sun got wrong&quot; on his blog at bcantrill.dtrace.org, analyzing the strategic and cultural mistakes that led to the company&\#x27;s decline. The post generated a substantial Hacker News discussion with 283 comments from practitioners sharing firsthand experiences of Sun&\#x27;s sales culture and product decisions. The piece is a case study in how a company can lead on technology yet lose on business execution, a pattern still visible in today&\#x27;s infrastructure, AI and hardware startups. For engineers and technical leaders, it offers concrete historical lessons about sales models, platform lock-in and missed partnerships that shaped the modern Unix and server landscape. The analysis draws on Cantrill&\#x27;s own tenure as a Sun engineer, and the community discussion adds specific decisions such as Sun briefly cancelling Solaris on x86 in 2002 — which convinced many customers they would be locked into SPARC — and failing to strike a deal with Google in 2002 because Sun demanded to know how many servers Google operated. Commenters also highlight Sun&\#x27;s costly sales process, where buyers faced live sales meetings and endless quote revisions, sometimes paying more for server rails and power cords than an entire delivered Dell server.

hackernews · chmaynard · Sep 21, 14:03 · [Discussion](https://news.ycombinator.com/item?id=49787436)

**Background**: Sun Microsystems was a pioneering Silicon Valley company whose SPARC workstations and servers running the Solaris Unix operating system powered much of the dot-com era; Sun engineers originated influential technologies such as DTrace and ZFS. Solaris superseded SunOS in 1993 and became known for scalability on SPARC hardware, with most of its code open-sourced as OpenSolaris in 2005. After years of losses following the dot-com crash, Sun was acquired by Oracle in 2010, OpenSolaris was discontinued, and the code was later forked into Illumos.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://en.wikipedia.org/wiki/Oracle_Solaris">Oracle Solaris - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree with the critique while debating its emphasis: several recall Sun&\#x27;s sales process as far more painful than Dell&\#x27;s, with one noting Alpha server rails and power cords costing more than a delivered Dell machine. Others list concrete blunders — killing Solaris on x86 in 2002 and mishandling the Google deal — while one commenter argues Sun was never really interested in running a business at all, only in building great technology, and another connects the episode to today&\#x27;s stretched AI-era valuations.

**Tags**: `#Sun Microsystems`, `#systems history`, `#engineering culture`, `#Solaris`, `#tech industry`

---

<a id="item-4"></a>
## [Essay Argues Attention Is Computing&\#x27;s Scarcest Resource](https://alicegg.tech/2026/09/21/attention) ⭐️ 7.0/10

An essay published at alicegg.tech on September 21, 2026 titled &quot;Attention is all you have&quot; argues that attention — not compute, storage, or information — is the genuinely scarce resource in modern computing, and that intentionally designed distraction has become a default property of digital products. The post reached 572 points and roughly 170 comments on Hacker News, making it one of the day&\#x27;s most discussed non-technical submissions. The essay reframes attention as an economic and design problem rather than a matter of personal willpower, pushing software practitioners to think about the ethics of engagement-driven product design. Its traction reflects a broader shift in the industry, where developers increasingly question metrics that reward time-on-site at the expense of users&\#x27; focus. The piece is a reflective essay rather than a technical report, so it offers no benchmarks or datasets; its substance lies in the argument and the ensuing debate. Commenters extended it with concrete examples, including the claim that the 1993 Mosaic browser had full-text history search while later bookmark systems regressed, and complaints that Firefox dropped RSS support while adding social-style UI elements.

hackernews · zer0tonin · Sep 21, 14:26 · [Discussion](https://news.ycombinator.com/item?id=49787726)

**Background**: The title is a playful echo of &quot;Attention Is All You Need,&quot; the 2017 paper that introduced the Transformer architecture, but the essay is about human attention rather than neural-network attention. The core concept invoked is the attention economy, an idea from information management and economics that treats human attention as a scarce commodity and studies how advertising-driven companies compete to maximize the time users spend on their products. Familiar examples include social media feeds, YouTube recommendations, and push notifications, all engineered to trigger the compulsive browsing behavior commonly called doomscrolling.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Attention_economy">Attention economy - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Attention_Is_All_You_Need">Attention Is All You Need - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Sentiment was broadly sympathetic: several commenters described cutting social media or switching to more &quot;intentional&quot; media use, and others admitted to hours of doomscrolling Hacker News and half-watched YouTube videos, with some proposing pre-written task lists or strict single-tasking as fixes. The sharpest critique came from user econ, who argued that organizing the web has been actively degraded — Mosaic&\#x27;s full-text history search gave way to poor bookmark systems, and RSS was replaced by social widgets — because there was no revenue in helping users curate their own browsing.

**Tags**: `#attention-economy`, `#social-media`, `#digital-wellbeing`, `#hacker-news-discussion`, `#product-design`

---