---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 17 items, 6 important content pieces were selected

---

1. [Claude Uncovers NIST Elliptic Curve Seeds&\#x27; lrand48 Origins](#item-1) ⭐️ 9.0/10
2. [Tesla Roadster demo adds cold-gas thrusters and rocket propulsion modes](#item-2) ⭐️ 8.0/10
3. [Mercor: 90% of US work hours lack solid AI benchmark coverage](#item-3) ⭐️ 8.0/10
4. [Waymo Announces Expansion Into Toronto](#item-4) ⭐️ 7.0/10
5. [Apple MLX Runs ~1T-Parameter Muse Spark Open on Four Mac Studios](#item-5) ⭐️ 7.0/10
6. [Sciences Po Analyzes Advanced AI Regulation Under the EU AI Act](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude Uncovers NIST Elliptic Curve Seeds&\#x27; lrand48 Origins](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic&\#x27;s Claude discovered that the seeds behind the NIST P-192, P-224, P-256, P-384 and P-521 elliptic curves were not produced by any hash function at all, but were the direct output of the C library&\#x27;s lrand48 pseudo-random number generator seeded with a Unix timestamp. The finding resolves a mystery that had stood for roughly a quarter century since the curves were published in FIPS 186-2 in 2000. The provenance of the NIST curve seeds had long been a source of distrust, since the NSA supplied them and critics feared they might hide a secret backdoor of the sort later found in the Dual\_EC\_DRBG random number generator. Showing that the seeds are plain lrand48 output reduces \(though does not eliminate\) suspicion about deliberate parameter manipulation in widely deployed cryptographic standards. Even with the generation method confirmed, one cannot see which candidate seeds were generated and discarded, so the curves could in principle still have been selected for a specific property by searching over timestamps fed to the generator. A fifth binary-field seed, B-163, does not match any method Claude tried and remains unexplained, with a likely mundane explanation being a typo introduced when the value was published.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**Background**: Elliptic curve cryptography derives its security from curves and generator points whose parameters must be chosen carefully; standards like ANSI X9.62 specify generating them &quot;verifiably at random&quot; by hashing an arbitrary seed with SHA-1 so that nobody can secretly rig the parameters. NIST published its P-192 through P-521 curves in FIPS 186-2 in 2000 with seeds supplied by the NSA, but the original seed values were never disclosed, prompting a $12,000 bounty from cryptographer Filippo Valsorda to recover them. lrand48 is a classic System V C library random number generator that uses a linear congruential algorithm and 48-bit integer arithmetic, and is easily seeded with predictable values such as the current time. Separately, concerns over possible backdoors in elliptic curve standards were famously raised by the Dual\_EC\_DRBG scandal.

<details><summary>References</summary>
<ul>
<li><a href="https://words.filippo.io/dispatches/seeds-bounty/">Announcing the $12k NIST Elliptic Curves Seeds Bounty</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/bounty-offered-for-secret-nsa-seeds-behind-nist-elliptic-curves-algo/">Bounty offered for secret NSA seeds behind NIST elliptic curves algo</a></li>
<li><a href="https://www.schneier.com/blog/archives/2023/10/bounty-to-recover-nists-elliptic-curve-seeds.html">Bounty to Recover NIST &#x27;s Elliptic Curve Seeds - Schneier on Security</a></li>

</ul>
</details>

**Discussion**: Commenters largely celebrated the discovery as the end of &quot;13 years of tinfoil hats,&quot; with one joking that it is devastating news for an entire generation of NIST cryptography conspiracy theories. A more cautious thread, echoed by the linked analysis, notes that confirming the generation method says nothing definitive about selection, since discarded candidates are invisible and one could still have searched timestamps for curves with desired properties. Another commenter suggests B-163&\#x27;s mismatch may simply be a publication typo rather than evidence of a different method.

**Tags**: `#cryptography`, `#NIST`, `#elliptic-curves`, `#random-number-generation`, `#AI-assisted-research`

---

<a id="item-2"></a>
## [Tesla Roadster demo adds cold-gas thrusters and rocket propulsion modes](https://www.tesla.com/roadster) ⭐️ 8.0/10

Tesla published a new Roadster demo video and accompanying social posts showing the car equipped with cold-gas thrusters and, in a separate &quot;invite only&quot; configuration, real combustion rocket engines, with footage of the vehicle driving vertically and appearing to fly. Two configurations are described: a cold-gas \(non-combustion\) version used only to boost forward acceleration, and a combustion-rocket version that appears in the video. The demo reframes the long-delayed Roadster as a showcase for extreme engineering rather than a near-term product, generating massive attention \(over 1,100 points and 2,000 comments on HN\) and intensifying scrutiny of Tesla&\#x27;s ability to actually deliver promised vehicles. It also raises broader questions about safety, environmental impact, and whether such propulsion systems have any realistic commercial path. Cold-gas thrusters work by expelling pressurized, typically inert gas through a nozzle without any combustion, which makes them the simplest, cheapest and most reliable form of rocket propulsion but also far less thrust-efficient than combustion engines; they are commonly used on CubeSats for attitude control because they avoid pyrotechnics and contaminants. Commenters noted that the compressed gas supply is likely very limited, that the thrusters could be dangerous to anyone on the wrong side of the car, and that Tesla reportedly &quot;cannot guarantee&quot; existing Roadster pre-orders will ever be delivered.

hackernews · shekhar101 · Oct 16, 01:32 · [Discussion](https://news.ycombinator.com/item?id=50112657)

**Background**: A cold gas thruster is a type of rocket engine that generates thrust purely from the expansion of stored pressurized gas, with no combustion — just a tank, a regulating valve, a nozzle and some plumbing. Because they are simple and produce no exhaust contaminants, they are widely used for spacecraft attitude control and orbital maintenance, particularly on small satellites like CubeSats. The Roadster is Tesla&\#x27;s long-promised second-generation sports car, originally unveiled in 2017 and repeatedly delayed, with Musk having previously floated the idea of adding a &quot;SpaceX package&quot; of cold-gas thrusters for dramatically improved acceleration.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster</a></li>

</ul>
</details>

**Discussion**: Sentiment was split between genuine amazement at the engineering and heavy skepticism: some commenters were stunned that the car &quot;actually flies&quot; and can drive vertically, while others dismissed it as a meme-stock marketing stunt that will never ship. Recurring concerns included the unknown propellant used in the cold-gas thrusters and its potential as an environmental contaminant, the limited compressed-gas supply and safety risk of thrusters near people, and Tesla&\#x27;s inability to guarantee delivery of existing pre-orders.

**Tags**: `#Tesla`, `#Roadster`, `#electric vehicles`, `#rocket propulsion`, `#marketing stunt`

---

<a id="item-3"></a>
## [Mercor: 90% of US work hours lack solid AI benchmark coverage](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

Mercor&\#x27;s Labor Index research published a &quot;benchmark map&quot; concluding that roughly 90% of American working hours are spent on tasks with little or no coverage from existing AI benchmarks. The analysis also found that, even after controlling for overall AI-exposure, O\*NET tasks drawn from occupations with larger wage bills are significantly overrepresented among the prompts used in current benchmarks. If benchmarks only exercise a thin slice of real work, leaderboard scores become a poor proxy for whether a model is actually useful on the job, which matters for AI labs prioritizing research, enterprises choosing vendors, and policymakers trying to forecast labor-market disruption. It suggests evaluation, rather than raw capability, may be the near-term bottleneck for deploying AI in large parts of the economy. The mapping relies on O\*NET occupational task data matched against benchmark prompt sets, and the authors note that most task families are sampled extremely thinly — for example, a category such as social workers counseling parents on child-rearing problems counts as &quot;well covered&quot; on the strength of roughly 13 prompts. Community readers also flagged that the study&\#x27;s threshold for &quot;covered well&quot; is ambiguous, since it can mean anything from a handful of prompts to genuine, representative coverage.

hackernews · speckx · Oct 16, 17:08 · [Discussion](https://news.ycombinator.com/item?id=50121179)

**Background**: O\*NET \(Occupational Information Network\) is a free U.S. Department of Labor database that describes hundreds of occupations in terms of the tasks, skills, knowledge, and abilities they require, and it is commonly used as the taxonomy for studying how automation and AI touch different kinds of work. AI benchmarks such as MMLU or SWE-bench are standardized tests that score models on fixed sets of questions or tasks, and they are the numbers usually cited when comparing frontier models. Mercor is a platform that connects domain experts with AI labs and enterprises to build benchmarks, training data, and agent evaluations, which is why it is producing this kind of labor-market coverage analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Occupational_Information_Network">Occupational Information Network - Wikipedia</a></li>
<li><a href="https://www.dol.gov/agencies/eta/onet">O*NET - U.S. Department of Labor</a></li>
<li><a href="https://www.mercor.com/">Mercor | Organizing human intelligence to power the AI economy</a></li>
<li><a href="https://www.unrot.co/blogs/what-are-ai-benchmarks">What Are AI Benchmarks ? MMLU &amp; SWE-bench Explained... | Unrot</a></li>

</ul>
</details>

**Discussion**: Commenters largely accepted the gap but pushed back on the framing: one described it as a version of the &quot;Doorman Fallacy,&quot; where automating an obvious task \(a door\) misses the other vital functions the worker performed. Others argued that &quot;covered well&quot; is effectively being used to mean &quot;covered at all,&quot; since 13 prompts cannot represent a social worker&\#x27;s job, and one noted that benchmark prompts skew toward high-wage occupations. Several tied the finding to broader ideas — Baumol&\#x27;s cost disease appearing at the individual level as time saved on coding gets absorbed by presentations, Jira and QA, and Karpathy&\#x27;s estimate that AI currently handles only a small single-digit percentage of work.

**Tags**: `#AI benchmarks`, `#AI evaluation`, `#labor market`, `#future of work`, `#O\*NET`

---

<a id="item-4"></a>
## [Waymo Announces Expansion Into Toronto](https://waymo.com/blog/2026/10/waymo-in-toronto/) ⭐️ 7.0/10

Waymo published a blog post announcing its expansion into Toronto, extending its autonomous ride-hailing service beyond its established U.S. markets. The announcement leads with job creation, and it triggered a large Hacker News thread \(264 points, 368 comments\) mixing first-hand rider experiences with deployment and regulatory concerns. Toronto would push Waymo into a new country and a colder, snowier climate, testing whether the Waymo Driver generalizes beyond the Sun Belt and California cities where it is best established. The move also puts autonomous ride-hailing directly in front of Canadian regulators, local taxi and ride-hail drivers, and competitors such as Uber and Tesla&\#x27;s robotaxi efforts. Toronto&\#x27;s heavy winter snow, ice and salt spray on roads are a serious challenge for the lidar, radar and camera sensor suite that autonomous vehicles rely on, since lane markings and even road edges can be obscured. The post&\#x27;s emphasis on local job creation, plus the active regulatory pushback Waymo has faced elsewhere, suggests the rollout will depend as much on political and legislative approval as on technical readiness.

hackernews · ChrisArchitect · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118981)

**Background**: Waymo is Alphabet&\#x27;s autonomous driving subsidiary and runs Waymo One, a commercial robotaxi service that picks up paying passengers with no human safety driver behind the wheel; it has scaled up in cities such as Phoenix, San Francisco, Los Angeles and Austin. Its vehicles rely on the Waymo Driver, a self-contained stack of lidar, radar, cameras and onboard compute rather than on remote human driving. Expanding to a new country requires not just mapping and vehicle testing but also local operating permits and rules for driverless commercial service, which is why announcements like this one are often framed around jobs and safety.

**Discussion**: Sentiment was mixed: several commenters described excellent Waymo rides in San Francisco and a thrill at spotting Waymo vehicles in Tokyo, while one rider in Austin reported a 9-minute trip being randomly &quot;slightly extended&quot; to 45 minutes and ending with support simply dropping them at a restaurant. Others noted that the Toronto post foregrounds job creation and pointed to organized opposition to Waymo in the Boston area driven by fears of driver job losses.

**Tags**: `#Waymo`, `#autonomous vehicles`, `#robotaxi`, `#Toronto`, `#Hacker News`

---

<a id="item-5"></a>
## [Apple MLX Runs ~1T-Parameter Muse Spark Open on Four Mac Studios](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 7.0/10

Apple Machine Learning Research published a post showing that the latest MLX release enables distributed inference of Muse Spark Open, a frontier-class model with nearly a trillion parameters, across a cluster of four Mac Studios, generating over 36 tokens per second. The work uses MLX&\#x27;s new distributed inference and RDMA-based communication primitives to scale a single-Mac Studio deployment \(up to 512GB unified memory\) out to multiple machines. It demonstrates that a cluster of consumer-grade Apple Silicon desktops can serve a frontier-scale open-weight model at speeds above average human reading speed, which is a meaningful milestone for private, locally-hosted LLM inference as an alternative to renting datacenter GPUs. This strengthens Apple&\#x27;s position in the local/on-device AI ecosystem and gives developers a practical path to running very large models on hardware they already own. The 15–36 tokens/second figures in the headline chart were measured at a context length of 8,192 tokens, which commenters note is small by current standards, and the comparison shows Meta&\#x27;s Muse Spark Open at 4-bit quantization against Qwen only at native BF16 — a configuration that critics argue unfairly disadvantages Qwen. For reference, Apple&\#x27;s post also benchmarks Qwen 3.8 27B and Mistral Medium 3.5 128B on a single Mac Studio, taking up to 68GB and 158GB of RAM respectively at a 65,536-token context.

hackernews · antipaul · Oct 16, 13:43 · [Discussion](https://news.ycombinator.com/item?id=50118320)

**Background**: MLX is Apple&\#x27;s open-source array framework for machine learning on Apple silicon, built around the unified memory architecture so the CPU and GPU can share data without copying it between separate memory pools. Muse Spark Open is Meta&\#x27;s open-weight, coding- and agent-oriented model with 816B total parameters \(42B active, a mixture-of-experts design\) and a 1M-token context window. Distributed inference means splitting one model across several machines so that weights and computation exceed what any single device&\#x27;s memory could hold, with RDMA over fast interconnects like Thunderbolt 5 keeping the nodes in sync.

<details><summary>References</summary>
<ul>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/MLX_%28machine_learning_framework%29">MLX (machine learning framework) - Wikipedia</a></li>
<li><a href="https://huggingface.co/meta-models/Muse-Spark-Open-816B-A42B">meta- models / Muse - Spark - Open -816B-A42B · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical of the benchmarking rather than the engineering: several criticized comparing a 4-bit Meta model against Qwen at native BF16 and called the choice an unfair, marketing-driven comparison. Others noted that the headline throughput was measured at only 8,192 tokens of context, which they consider too small to be practically useful, while one user countered with independent benchmarks showing a single M5 Ultra running DeepSeek 4.1 Flash at ~45 tok/s and an M5 Max handling GLM 5.3 Flash with verified quality.

**Tags**: `#apple-mlx`, `#local-inference`, `#llm-serving`, `#distributed-computing`, `#benchmarking`

---

<a id="item-6"></a>
## [Sciences Po Analyzes Advanced AI Regulation Under the EU AI Act](https://news.google.com/rss/articles/CBMi0gFBVV95cUxNN1NtY0RrRzAyUHNSRnhCay1zQU80UkllT0N3UkJTcGdTV3QwdGtNUXRTZjdMczgyU0VfdUxELTlBNWpoUG5wRHgtVG9zWEZmTHlsSzc1ck5NTWM0RmJMRW0wNWZpVURWNUZncHJScDdCNVZtUnNwS3l0SUNEMWtCSnM1aW41SEZUN1BXbklRRlVFTE53cEh5N3hnS2Q0ZDhuTjExdDBVc2MyeXBodDZnaTVIVk03UFM4OWtiLWJoeHRhYk1vQzNCdVpyWXMxWjFEa3c?oc=5) ⭐️ 6.0/10

Sciences Po has published an analysis examining how advanced AI systems are regulated under the EU AI Act, distinguishing between pre-existing rules in the legislation, newly introduced provisions, and the practical difficulties of putting them into practice. The piece focuses on the compliance gap between the Act&\#x27;s legal text and the real-world implementation now underway across the EU. The EU AI Act is the world&\#x27;s first comprehensive, horizontal AI law, so how it treats advanced and frontier models will shape compliance expectations for developers and deployers worldwide. Ambiguities in its implementation could either raise costs for smaller AI firms in Europe or set a de facto global standard that other jurisdictions copy. The Act applies in staggered phases: prohibitions on unacceptable-risk practices and AI literacy duties took effect from 2 February 2025, general-purpose AI \(GPAI\) model obligations from 2 August 2025, and most high-risk system requirements from 2 August 2026, with AI embedded in regulated products following in 2027. GPAI models trained above roughly 10^25 FLOPs are presumed to carry systemic risk, and violations can draw fines of up to €35 million or 7% of global annual turnover.

rss · GoogleNews-欧盟监管 · Oct 16, 07:53

**Background**: The EU AI Act was published in the Official Journal of the European Union on 12 July 2024 and entered into force on 1 August 2024. It uses a risk-based approach, imposing light transparency duties on low-risk systems, strict obligations on high-risk uses such as hiring, credit scoring and critical infrastructure, and outright bans on practices like social scoring and manipulative techniques. General-purpose and frontier models — the category often called &\#x27;advanced AI&\#x27; — face separate transparency, documentation and systemic-risk obligations, which is the focus of the Sciences Po analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe ’s digital future</a></li>
<li><a href="https://artificialintelligenceact.eu/the-act/">The Act Texts | EU Artificial Intelligence Act</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#AI regulation`, `#AI governance`, `#AI policy`, `#advanced AI`

---