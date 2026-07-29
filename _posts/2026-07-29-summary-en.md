---
layout: default
title: "Horizon Summary: 2026-07-29 (EN)"
date: 2026-07-29
lang: en
---

> From 20 items, 4 important content pieces were selected

---

1. [Substack writers urged to maintain own websites](#item-1) ⭐️ 8.0/10
2. [Sebastian Raschka Analyzes Kimi K3&\#x27;s NoPE and KDA Architecture](#item-2) ⭐️ 8.0/10
3. [OpenAI open-sources Codex Security CLI scanner](#item-3) ⭐️ 7.0/10
4. [10-Step EU AI Act Compliance Checklist Released](#item-4) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Substack writers urged to maintain own websites](https://elizabethtai.com/2026/06/10/substack-writers-you-need-a-website/) ⭐️ 8.0/10

An article argues that Substack writers should host their own websites to retain control over content and audience, avoiding platform lock-in. The Hacker News community extensively debated this with 379 points and 195 comments. This debate highlights the growing tension between leveraging platform distribution and maintaining content ownership. Writers risk losing their audience and content if Substack changes policies or shuts down, making self-hosting a crucial long-term strategy. Commenters suggest practical strategies such as using Substack with a custom domain like subdomain.website.com, or publishing first on a personal blog and then copying to Substack for email distribution. Tools like Simon Willison&\#x27;s blog-to-newsletter script facilitate this hybrid approach.

hackernews · speckx · Jul 28, 16:58 · [Discussion](https://news.ycombinator.com/item?id=49086788)

**Background**: Substack is a platform that allows writers to publish newsletters and monetize via subscriptions. However, relying solely on Substack means the writer&\#x27;s content and subscriber list are tied to the platform, creating a risk if the platform changes terms or ceases operations. Owning a personal website ensures the writer has full control and can move elsewhere easily.

**Discussion**: The comments show a split between those who value Substack&\#x27;s distribution and ease of use, and those who prioritize ownership and independence. Simon Sarris uses a subdomain approach to keep control, while simonw hybrid-publishes to both his blog and Substack. Skippyfish counters that self-hosting lacks push mechanisms to reach readers, arguing Substack&\#x27;s email distribution is essential.

**Tags**: `#Substack`, `#indie web`, `#content ownership`, `#blogging`, `#platform risk`

---

<a id="item-2"></a>
## [Sebastian Raschka Analyzes Kimi K3&\#x27;s NoPE and KDA Architecture](https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html) ⭐️ 8.0/10

Sebastian Raschka published a detailed analysis of Kimi K3&\#x27;s architectural innovations, which include removing all Rotary Position Embeddings \(RoPE\) in favor of No Positional Embeddings \(NoPE\) and introducing Key-Value Design Attention \(KDA\). This analysis is significant because Kimi K3&\#x27;s novel approach challenges conventional wisdom that positional embeddings are necessary for language models, and KDA&\#x27;s linear attention with fine-grained gating could enable longer context windows and greater efficiency. KDA is a gated linear attention variant that refines Gated DeltaNet with channel-wise decay, and it is interleaved with full attention layers in a 3:1 ratio, reducing KV-cache usage by up to 75%.

hackernews · ModelForge · Jul 28, 15:48 · [Discussion](https://news.ycombinator.com/item?id=49085698)

**Background**: NoPE is an approach that omits positional embeddings entirely, relying on the model&\#x27;s ability to infer token positions from context. Kimi K3, developed by Moonshot AI, is an open-weight LLM with a 1M token context length. KDA \(Kimi Delta Attention\) is a linear attention mechanism designed for efficient long-context processing.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/andrewdalpino/NoPE-GPT">GitHub - andrewdalpino/NoPE-GPT: A GPT-style small language model (SLM) with no positional embeddings (NoPE). · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2510.26692">[2510.26692] Kimi Linear: An Expressive, Efficient Attention ... Kimi Delta Attention (KDA): algorithm, pseudocode, flow ... Kimi K3 Technical Advancements Explained - nextbigfuture.com Kimi Linear: Expressive &amp; Efficient Attention KDA (Kimi Delta Attention) | fla-org/flash-linear-attention ...</a></li>
<li><a href="https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html">Kimi K 3 Architecture Notes | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**Discussion**: Community comments are positive and inquisitive: some express surprise that NoPE works, while others praise Raschka&\#x27;s detailed breakdown and note that Kimi K3&\#x27;s novel architecture disproves claims that it is merely a distillation attack.

**Tags**: `#LLM architecture`, `#NoPE`, `#Kimi K3`, `#deep learning`, `#positional embeddings`

---

<a id="item-3"></a>
## [OpenAI open-sources Codex Security CLI scanner](https://github.com/openai/codex-security) ⭐️ 7.0/10

OpenAI has open-sourced Codex Security, a CLI-based security scanner that uses AI to identify and fix vulnerabilities in code repositories. The tool was previously available as a plugin and is now publicly available on GitHub. This release makes AI-powered security scanning accessible to a wider audience, but early user reports of long runtimes and high API usage raise practical concerns. It also highlights the ongoing debate about AI companies offering security tools given their potential conflicts of interest. Users report that scanning even a small repository can take nearly an hour and consume half of a Pro plan&\#x27;s weekly API quota. The tool relies on English &\#x27;Skill definitions&\#x27; that instruct the LLM, and OpenAI has the compute resources to optimize these prompts.

hackernews · bakigul · Jul 28, 20:52 · [Discussion](https://news.ycombinator.com/item?id=49089755)

**Background**: Codex is an AI coding agent from OpenAI, released in April 2025, that assists with software engineering tasks like writing and fixing code. Codex Security, introduced in March 2026, is an application-security agent that identifies and fixes vulnerabilities by building threat models and scanning repository history.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Codex_Security">Codex Security</a></li>
<li><a href="https://help.openai.com/en/articles/20001107-codex-security">Codex Security | OpenAI Help Center</a></li>

</ul>
</details>

**Discussion**: Community feedback is mixed: some users report extremely long runtimes and high API costs, while others point out the value of the open-source Skill definitions. There is also skepticism, with one commenter comparing AI security tools to &\#x27;fire departments run by arsonists.&\#x27;

**Tags**: `#security`, `#open-source`, `#AI tools`, `#code analysis`, `#OpenAI`

---

<a id="item-4"></a>
## [10-Step EU AI Act Compliance Checklist Released](https://news.google.com/rss/articles/CBMipwFBVV95cUxNczhEdzFiM3ExdEdzOU1YZXFJbnNNUnNPMC1KRVdCS3dwV1htcVRad2NROTN1bGxybHdjam4xZUk4dWlNaHN0bjhHa2l3X0tJWlozWlU4X0JTT0pseGx0NFJ6eFpwNzZRTEZ5YzlfSGZqQkJFVVpBbmNDcWpxalFUbjNvZXlETmE5TXBmTlFmTjNXNFdGbWlxU29iRkt3RnpvS0w0TWN5MA?oc=5) ⭐️ 7.0/10

Security Boulevard published a 10-step compliance checklist to help organizations avoid costly penalties under the EU AI Act. This checklist provides practical guidance for businesses to navigate the EU AI Act&\#x27;s complex requirements, potentially saving them from significant fines and legal repercussions. The checklist addresses key compliance areas such as risk classification, transparency obligations, and governance structures, aligned with the Act&\#x27;s risk-based framework.

rss · GoogleNews-欧盟监管 · Jul 28, 08:02

**Background**: The EU AI Act, effective August 1, 2024, is the world&\#x27;s first comprehensive AI regulation, classifying AI systems by risk level \(unacceptable, high, limited, minimal\). It imposes obligations on providers and users, with penalties for non-compliance, and applies extraterritorially to entities with EU users.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe ’s digital future</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#AI governance`

---