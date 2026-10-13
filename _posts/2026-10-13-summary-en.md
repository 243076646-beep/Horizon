---
layout: default
title: "Horizon Summary: 2026-10-13 (EN)"
date: 2026-10-13
lang: en
---

> From 21 items, 6 important content pieces were selected

---

1. [Hackers Trigger Defrost Cycles in European Supermarket Fridges](#item-1) ⭐️ 8.0/10
2. [Developer turns WiFi 7 router chipset into a 320 Msps SDR receiver](#item-2) ⭐️ 8.0/10
3. [Codex CLI quietly installs a persistent, self-updating background daemon by default](#item-3) ⭐️ 8.0/10
4. [Z.ai Releases GLM-Legal, an Agentic Model for Legal Workflows](#item-4) ⭐️ 7.0/10
5. [A Modern Web App in C Sparks Debate on Low-Dependency Stacks](#item-5) ⭐️ 7.0/10
6. [Reddit test claims Meta&\#x27;s Muse shopping AI favors well-known merchants](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Hackers Trigger Defrost Cycles in European Supermarket Fridges](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

A cyberattack exploited internet-connected refrigeration controllers at European supermarket chains, including roughly 400 French stores such as Intermarché, forcing automatic defrost cycles that heated fridges to around 50°C and disrupted store operations. Reports indicate the incident also impacted delivery logistics and in-store pricing. The incident is a high-profile real-world example of an OT/ICS attack causing physical disruption in retail, showing how the cold-chain infrastructure that keeps food safe can be turned against operators. It underscores that operational technology security is no longer just a factory or utility concern but a retail and supply-chain issue affecting everyday consumers. Danfoss said the hijacked controllers were mostly legacy units running outdated firmware, with community analysis pointing to 15–20 year old models such as the SM800 \(end-of-support 2021\) and SC355 \(end-of-support 2016\). Prior security research by Claroty&\#x27;s Team82 had already disclosed vulnerabilities in Danfoss refrigeration controllers, and Danfoss publishes coordinated vulnerability disclosures and advisories for affected products.

hackernews · Zeekaas · Oct 12, 12:16 · [Discussion](https://news.ycombinator.com/item?id=50055304)

**Background**: Commercial refrigeration controllers, such as those made by Danfoss, manage temperature, defrost cycles and energy efficiency for supermarket display cases and cold rooms. Vendors often promote connecting these devices to the internet so issues can be diagnosed remotely and defrosts started without dispatching a service engineer, plus performance benchmarking across a fleet of stores. OT \(operational technology\) or ICS \(industrial control systems\) security focuses on protecting the physical-process devices that run such equipment, which frequently lack modern security features and are difficult to patch once deployed.

<details><summary>References</summary>
<ul>
<li><a href="https://cybernews.com/security/danfoss-refrigeration-hack-france-supermarkets/">Refrigeration Cyberattack Hits French Supermarkets | Cybernews</a></li>
<li><a href="https://www.msn.com/en-us/technology/cybersecurity/danfoss-says-hacked-controllers-behind-50c-french-supermarket-fridges-ran-old-firmware/ar-AA2e6nkW">Danfoss says hacked controllers behind 50C French ... - MSN</a></li>
<li><a href="https://en.wikipedia.org/wiki/IoT_security_device">IoT security device</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters traced the likely root cause to 15–20 year old end-of-life Danfoss controllers and debated why insecure devices get internet-connected in the first place, citing vendor remote-management features and subscription-locked lab equipment that cannot run tests without a paid connection. Others connected the event to an August 2026 incident involving US military commissary freezers and speculated about whether it is the same actor, an imitator, or unrelated.

**Tags**: `#cybersecurity`, `#ICS-OT-security`, `#IoT`, `#supply-chain`, `#infrastructure`

---

<a id="item-2"></a>
## [Developer turns WiFi 7 router chipset into a 320 Msps SDR receiver](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

A developer \(h0m3us3r\) has reverse-engineered the chipset in a W1700K WiFi 7 router so it can operate as a software-defined radio receiver sampling at 320 Msps in the 5 GHz band, publishing the work as an open-source project on GitHub. It shows that commodity WiFi 7 hardware can deliver high-bandwidth SDR reception at a fraction of the cost of dedicated equipment, potentially opening cheap RF experimentation to hobbyists, researchers and small labs. If the technique generalizes to common WiFi cards, everyday laptops could double as wideband receivers. The hack yields a receive-only SDR with a 320 Msps sample rate centered in the 5 GHz band — not a DC-to-daylight general-coverage radio — and because it targets the same chipset, commenters believe it should also work on the Banana Pi R4, which provides built-in PCIe for NVMe storage.

hackernews · djfergus · Oct 12, 12:41 · [Discussion](https://news.ycombinator.com/item?id=50055593)

**Background**: Software-defined radio \(SDR\) replaces traditionally analog RF components such as mixers, filters and demodulators with software running on a general-purpose processor, typically fed by an analog-to-digital converter behind an RF front end. This lets a single piece of hardware receive many different radio protocols simply by changing software. WiFi 7 \(IEEE 802.11be\) is the newest WiFi standard, operating in the 2.4, 5 and 6 GHz bands, and its wide channels and high throughput make its front-end chipsets attractive raw sampling hardware for SDR experiments.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software-defined_radio">Software-defined radio</a></li>
<li><a href="https://en.wikipedia.org/wiki/WiFi_7">WiFi 7</a></li>

</ul>
</details>

**Discussion**: Commenters were enthusiastic, noting that the same developer previously built an SDR from an ESP32 microcontroller \(eSpDR\) and hoping such tricks spread to common WiFi cards so any laptop could become a budget SDR. Others flagged likely compatibility with the Banana Pi R4, praised it as the cheapest route to a 320 Msps receiver at 5 GHz, and speculated about software-defined radios in phones and building cheap modern service monitors from desktop CNC, custom PCBs and commodity parts.

**Tags**: `#SDR`, `#WiFi 7`, `#hardware-hacking`, `#RF`, `#embedded-systems`

---

<a id="item-3"></a>
## [Codex CLI quietly installs a persistent, self-updating background daemon by default](https://github.com/openai/codex/issues/48195) ⭐️ 8.0/10

A widely discussed GitHub issue \(openai/codex \#48195\) reports that OpenAI&\#x27;s Codex CLI installs a persistent, self-updating background daemon by default, with no documented way to disable it. The issue, which drew a 488-point Hacker News thread with 249 comments, stems from community reports of multi-gigabyte disk bloat, permission corruption, and hidden background behavior. Codex CLI is a popular developer tool, so defaulting to a persistent self-updating daemon affects many users&\#x27; machines, disk usage, and security posture without explicit consent. It raises a broader industry question about how much background infrastructure AI coding agents should install silently versus how traditional CLIs are expected to behave. The daemon currently sits behind a feature flag and can be disabled by setting daemon\_auto\_start = false under \[features\] in ~/.codex/config.toml, though no official settings UI or documentation exposes this. Users report the daemon writes pid and lock files to ~/.codex and that one user measured roughly 12 GB of disk usage from accumulated old versions.

hackernews · whimblepop · Oct 12, 18:29 · [Discussion](https://news.ycombinator.com/item?id=50060694)

**Background**: Codex CLI is OpenAI&\#x27;s lightweight coding agent that runs locally in the terminal, distinct from the original Codex language model behind GitHub Copilot. A daemon is a background process that runs continuously rather than starting and stopping with a terminal window, and a self-updating daemon fetches new versions on its own. Users typically expect a CLI installed via a package manager like NPM to run only when invoked and not to persist or update itself silently.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openai/codex/issues/48195">CLI: make ` daemon _auto_start` opt-in — a persistent, self - updating ...</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28language_model%29">OpenAI Codex (language model)</a></li>

</ul>
</details>

**Discussion**: Commenters are largely critical: one notes the daemon isn&\#x27;t documented but can be disabled via a feature flag, another reports ~12 GB of disk bloat from old versions, and others describe bugs where auto-updating corrupted file permissions and made .git read-only. Several users also share frustration that installing a CLI via NPM shouldn&\#x27;t spawn persistent background processes, while a few point to minimal bare-bones harness alternatives as a refreshing contrast to overengineered agents.

**Tags**: `#Codex CLI`, `#OpenAI`, `#background daemon`, `#privacy`, `#software engineering`

---

<a id="item-4"></a>
## [Z.ai Releases GLM-Legal, an Agentic Model for Legal Workflows](https://z.ai/blog/glm-legal) ⭐️ 7.0/10

Z.ai announced GLM-Legal, a legal-domain agentic large language model that it evaluated across complex task execution, specialized legal reasoning, and real-world legal workflows. The company reports a 19.2% all-pass rate on Harvey LAB while matching frontier closed-source models on LegalBench and PLawBench, despite running on a significantly leaner parameter footprint. The release shows frontier-model vendors pushing into a high-stakes professional domain where errors carry real legal and financial consequences, and it lands amid growing debate over whether AI systems should be allowed to act in legal matters without a qualified human reviewer. The low end-to-end pass rate also gives a concrete data point on how far agentic AI still is from independently delivering client-ready legal work. The 19.2% all-pass rate on Harvey LAB means the model still fails the large majority of end-to-end legal tasks, which the vendor itself frames as evidence that agentic legal work remains immature. Z.ai also says its evaluation harness and model training iterate together, so production feedback is converted into concrete engineering loss signals.

hackernews · ilreb · Oct 12, 16:11 · [Discussion](https://news.ycombinator.com/item?id=50058507)

**Background**: Z.ai is the international brand of Zhipu AI, a Chinese company founded in 2019 by Tsinghua University researchers that develops the open-weight GLM \(General Language Model\) family, first published in 2021 and popularized as the ChatGLM chatbot in 2023. GLM-Legal is a domain-specialized variant of that family aimed at legal practice, and it is being measured against legal benchmarks such as LegalBench, PLawBench and Harvey LAB, which test reasoning and task completion rather than general conversation. &\#x27;Agentic&\#x27; here means the model is expected to carry out multi-step workflows on its own rather than only answering single questions.

<details><summary>References</summary>
<ul>
<li><a href="https://z.ai/blog/glm-legal">GLM-Legal: Advancing Agentic Legal Intelligence</a></li>
<li><a href="https://www.unite.ai/z-ai-unveils-glm-legal-an-agentic-model-for-legal-workflows/">Z.ai Unveils GLM-Legal, an Agentic Model for Legal Workflows</a></li>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z.ai - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical: an attorney said a 20% pass rate on a benchmark is unimpressive because litigation practice is about handling novel situations rather than relitigating past ones. Others raised trust concerns, pointing to past reports that Z.ai snapshotted entire workspaces before every prompt, and one commenter cited Anthropic&\#x27;s policy update requiring a qualified &\#x27;human in the loop&\#x27; for uses affecting legal rights. A counterpoint argued LLMs could still help clear massive case backlogs, such as India&\#x27;s 58 million pending court cases, on clear-cut matters.

**Tags**: `#AI`, `#legal-tech`, `#LLM`, `#benchmarks`, `#privacy`

---

<a id="item-5"></a>
## [A Modern Web App in C Sparks Debate on Low-Dependency Stacks](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

An article titled &quot;A Modern Web App in C&quot; demonstrates how to build a modern web application using the C language, arguing for a simple, low-dependency server architecture. It drew a large Hacker News discussion \(426 points, 175 comments\) covering CGI, FastCGI, privilege separation, and alternative web stacks. The piece and its discussion highlight a growing counter-movement against heavyweight, dependency-heavy web frameworks, showing that decades-old techniques like CGI can still be viable for many workloads. This matters to systems programmers and small-team developers who value simplicity, security, and operational minimalism over ecosystem trendiness. Practitioners in the thread emphasized privilege-dropping mechanisms such as pledge and chroot, and noted that BusyBox ships with built-in cgi-bin support; some readers questioned whether invoking a binary per request via nginx \(the classic CGI model\) is preferable to a stateful backend process.

hackernews · prophittcorey · Oct 12, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50058528)

**Background**: The Common Gateway Interface \(CGI\) is an interface specification that lets a web server execute an external program to handle an HTTP request, making it a foundational way to generate dynamic content. FastCGI is a later binary protocol variation that reduces CGI&\#x27;s per-request process overhead. Privilege separation is a security technique that splits a program into components, each granted only the minimal privileges it needs, to limit the damage from vulnerabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Common_Gateway_Interface">Common Gateway Interface - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/FastCGI">FastCGI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Privilege_separation">Privilege separation</a></li>

</ul>
</details>

**Discussion**: Overall sentiment was positive and nostalgic, with practitioners sharing real-world CGI and FastCGI experience: one founded a web dev company 22 years ago on a C/FastCGI stack, another built a Civ-like game with a C++/WebAssembly client and C++ server, and others noted BusyBox&\#x27;s cgi-bin support. Some disagreed on architecture, preferring stateful Rust/SQLite backends \(e.g., Tokio, Actix, Diesel\) that persist in memory rather than launching a process per request.

**Tags**: `#C`, `#web-development`, `#systems-programming`, `#CGI`, `#hacker-news`

---

<a id="item-6"></a>
## [Reddit test claims Meta&\#x27;s Muse shopping AI favors well-known merchants](https://www.reddit.com/r/ecommerce/comments/1x40wwd/metas_shopping_ai_is_stacked_against_you_if_you/) ⭐️ 6.0/10

An analytics company reportedly obtained internal instructions for Meta&\#x27;s shopping AI agent Muse, which state it is &quot;imperative&quot; that the top five products come from well-known merchants, and then ran 50 searches to test this. In that test, stores from the Shopify catalog supplied 94% of the products the agent considered, but received only about a third of the displayed spots, with the remainder going to two sites the agent found on its own. If shopping agents become a primary way people buy online, the ranking rules baked into those agents effectively decide which merchants get discovered, and a built-in preference for well-known brands could squeeze out small independent stores that dominate marketplaces today. This turns a technical design choice inside Muse into a broader question of fairness and gatekeeping in agentic commerce. The evidence is thin: it relies on a single analytics company&\#x27;s 50-search test, Meta has not commented, and no methodology or raw data has been published, so the findings should be treated as anecdotal rather than proven bias. Meta&\#x27;s own public descriptions of Muse emphasize that it searches retail sites, tracks prices and prepares a purchase for the user&\#x27;s approval, but they do not disclose how products are ranked.

reddit · r/ecommerce · /u/BaptisteNo · Oct 12, 12:46

**Background**: Muse is Meta&\#x27;s personal AI agent, and one of its stated uses is shopping: it can search retail sites, surface deals, track prices and prepare a checkout that the user approves before anything is bought. Unlike a traditional marketplace search ranked by relevance or ads, an AI agent chooses on the user&\#x27;s behalf, so its internal guidance effectively acts as a ranking policy. Shopify&\#x27;s catalog is a large, structured product feed that agents like Muse can pull from, which is why merchants on that platform care about how their listings are treated.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/muse/shopping/">Muse for Shopping: Deals, Price Tracking, Returns | AI at Meta</a></li>
<li><a href="https://www.cnbc.com/2026/10/03/meta-muse-shopping-ai-agent.html">Meta Muse shopping: How checkout, payments and privacy work</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#ecommerce`, `#Meta`, `#recommendation bias`, `#Shopify`

---