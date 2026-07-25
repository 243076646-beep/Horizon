---
layout: default
title: "Horizon Summary: 2026-07-25 (EN)"
date: 2026-07-25
lang: en
---

> From 16 items, 5 important content pieces were selected

---

1. [Anthropic Releases Claude Opus 5 with No Data Retention](#item-1) ⭐️ 9.0/10
2. [Security camera exposes GitHub admin token on login page](#item-2) ⭐️ 9.0/10
3. [Why software quality declines despite coding advances](#item-3) ⭐️ 8.0/10
4. [Google Signs EU AI Act Transparency Code, Setting Compliance Bar](#item-4) ⭐️ 6.0/10
5. [EU warns TikTok of fines for child safety breaches under DSA](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic Releases Claude Opus 5 with No Data Retention](https://www.anthropic.com/news/claude-opus-5) ⭐️ 9.0/10

Anthropic has released Claude Opus 5, a state-of-the-art AI model that comes close to the frontier intelligence of Claude Fable 5 at half the price. Notably, it does not have data retention requirements for general access, unlike Fable 5 which requires 30-day retention. This release provides organizations with a powerful AI model that does not require data retention, addressing a major privacy and compliance concern. It also sets a new benchmark for cost-effective frontier AI, potentially accelerating adoption in sensitive industries. Claude Opus 5 matches Fable 5 on most benchmarks while priced at half the cost. It continues many &\#x27;Claude-isms&\#x27; from its predecessor Opus 4.8, indicating stylistic consistency.

hackernews · alvis · Jul 24, 16:57 · [Discussion](https://news.ycombinator.com/item?id=49038433)

**Background**: Anthropic is an AI safety company that develops the Claude family of models. &\#x27;Opus&\#x27; models are high-capability models, while &\#x27;Fable&\#x27; models represent frontier intelligence. Data retention policies are critical for organizations handling sensitive data, as some models require retaining prompts and outputs for safety classifiers. Claude Opus 5 is released under a zero-data-retention policy, making it suitable for privacy-sensitive use cases.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-5">Introducing Claude Opus 5 \ Anthropic</a></li>
<li><a href="https://glitchwire.com/news/claude-opus-5-matches-fable-5-on-most-benchmarks-at-half-the-price/">Claude Opus 5 Matches Fable 5 on Most Benchmarks at... — Glitchwire</a></li>
<li><a href="https://coursiv.io/blog/claude-opus-5">Claude Opus 5 : Release Date, What We Know &amp; Model... | Coursiv Blog</a></li>

</ul>
</details>

**Discussion**: Community members highlight the zero data retention policy as a key advantage over Fable 5. A user reports that Opus 5 performs better than Fable 5 in image-to-HTML conversion, following design source of truth more accurately. Another comment notes the growing complexity of model routing as companies release many model variants.

**Tags**: `#AI`, `#LLM`, `#Claude`, `#Anthropic`, `#model release`

---

<a id="item-2"></a>
## [Security camera exposes GitHub admin token on login page](https://hhh.hn/hanwha-github-token/) ⭐️ 9.0/10

A security camera from Hanwha was found to contain a GitHub admin token hardcoded in its login page&\#x27;s source code, exposing administrative access to a GitHub repository. This incident highlights severe security failures in IoT devices, where hardcoded credentials can lead to widespread compromise of manufacturer infrastructure and customer data. The token was an admin-level GitHub personal access token \(PAT\) embedded in the camera&\#x27;s web interface, which could be used to access private repositories and manage organizations.

hackernews · hhh · Jul 24, 11:54 · [Discussion](https://news.ycombinator.com/item?id=49034292)

**Background**: A GitHub personal access token \(PAT\) is an authentication method that allows users to interact with GitHub&\#x27;s API without a password, with scopes defining its permissions. Exposing such a token publicly grants anyone with the token the same access as the token owner. IoT devices often lack proper security practices, and hardcoding credentials is a known vulnerability that can be exploited through device firmware or web interfaces.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens">Managing your personal access tokens - GitHub Docs</a></li>
<li><a href="https://csrc.nist.gov/pubs/sp/1800/36/final">SP 1800-36, Trusted Internet of Things (IoT) Device Network ...</a></li>

</ul>
</details>

**Discussion**: Community comments express frustration with IoT security, noting that many vendors ship devices with hardcoded credentials and broken security. One user recommended putting cameras on a separate VLAN without internet access as a mitigation. Another commenter pointed out that US Department of War IP addresses were also baked into the firmware, raising further concerns.

**Tags**: `#security`, `#IoT`, `#vulnerability`, `#GitHub`, `#camera`

---

<a id="item-3"></a>
## [Why software quality declines despite coding advances](https://ptrchm.com/posts/nothing-works-and-everyone-is-euphoric/) ⭐️ 8.0/10

An article argues that software quality is deteriorating due to non-technical decision-makers, update dread, and trade-offs of AI-generated code, sparking widespread discussion in the engineering community. This critique challenges the prevailing optimism about AI-assisted development, highlighting systemic issues in tech companies that affect millions of users. It resonates with many engineers who feel frustrated by declining user experience. The article specifically mentions Slack stealing focus on macOS and general dread of updates as examples of degraded experience. It also notes that AI code generation shifts the definition of &\#x27;fast&\#x27; but does not improve confidence in correctness.

hackernews · pchm · Jul 24, 09:08 · [Discussion](https://news.ycombinator.com/item?id=49033004)

**Background**: Update dread refers to the anxiety users feel when forced to install updates that may introduce regressions or unwanted changes. AI code generation tools like GitHub Copilot can speed up development but often produce code that requires careful review, introducing technical debt if not managed properly. The article&\#x27;s claim that non-technical decision-makers prioritize novelty over quality is a recurring theme in software engineering critiques.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aha.io/engineering/articles/the-architectural-trade-offs-of-ai-code-generation">The architectural trade-offs of AI code generation - Aha!</a></li>
<li><a href="https://waqas.ragnorx.com/blog/trade-offs-ai-code-generation">The Trade-Offs of Relying on AI for Code | Waqas Ahmad</a></li>

</ul>
</details>

**Discussion**: Community comments largely agree with the critique. One user points out that non-technical &\#x27;imposters&\#x27; control product decisions, while another shares personal experience of update dread. A third highlights the trade-off between speed and correctness in AI-assisted coding, noting that engineers must still invest time to ensure quality.

**Tags**: `#software quality`, `#tech industry`, `#UX`, `#AI code generation`, `#engineering culture`

---

<a id="item-4"></a>
## [Google Signs EU AI Act Transparency Code, Setting Compliance Bar](https://news.google.com/rss/articles/CBMimAFBVV95cUxOWjlwUDIzUnZFZlpTdjdQQ0F3VmthdW5qb3NmUFBiMjBVVVl5aDh6Qld4T3kybHQyYTNEb0V1OWR3UGVNVXpKQ3ZoRVBpaU9oVmE3ME81ckZMMXduUkhfdF9TV3dMTlN5T1BWX3lZWnA5Q0szZ1hFRkY4Y2ZFODN2Z3U1UUtPYXQtUndBT2wtWHlZZjg1NW9NeA?oc=5) ⭐️ 6.0/10

Google has signed the EU AI Act Transparency Code, becoming one of the first major tech companies to formally commit to the voluntary code of practice for marking and labeling AI-generated content. This move sets a high compliance bar for other AI developers and signals Google&\#x27;s proactive approach to AI regulation, which could influence industry standards and shape future enforcement of the AI Act. The transparency code is a voluntary framework that supports compliance with Article 50 of the EU AI Act, focusing on consistent and proportionate marking of AI-generated content. Signatories commit to clear labeling and transparency measures without replacing the legal obligations of the Act.

rss · GoogleNews-欧盟监管 · Jul 24, 14:46

**Background**: The EU AI Act is a landmark regulation that categorizes AI systems based on risk and imposes requirements including transparency. Article 50 specifically mandates that AI-generated content be clearly labeled. The Code of Practice on Transparency of AI-Generated Content provides a practical, EU-wide framework for signatories to demonstrate compliance with these transparency obligations.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialintelligenceact.eu/article/50/">Article 50: Transparency Obligations for Providers and ...</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content">Code of Practice on Transparency of AI-Generated Content</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#EU AI Act`, `#Google`, `#compliance`, `#tech policy`

---

<a id="item-5"></a>
## [EU warns TikTok of fines for child safety breaches under DSA](https://news.google.com/rss/articles/CBMi5AFBVV95cUxPTjhHLTMzTmpmcjByZldrT2hvbTNxMkF4YmxlOERrM1g3WHlWODRqRGFIbnp4aGFremdieXZBelR0am5oT2JsaWFJNG5TcEpZV2hSYnh6Q01fVlVfRXdFZWhlMnZJelhsamQ5ZzZSQ1BpYm5NdkpZY0ZLM1pFMHFicEw3UkdoOTh0SEl6cXN6Qk54cllsVVNsTWl6Y24xbHFRWlZlS09MTVdYbDBHdzRZV0RfeEpsc3JDZ2hUbk1VQ2FUa1VBYWxHaDNXX2xWOFhNN3AwSWJkUGhlTGpTUUpBMUNYYkrSAeoBQVVfeXFMT2ZkaWVaV1lUTHQzUFBwMWNxLWJXV2JtdU5FNnV1UGZwTV9qSkFGTFVxaEtqa01QY0F2Q0NkZDVBbEJUNmhGNXkxeFVNY1hyT0tRZi0yVVVtQTIwX1J1Y0paY0xsSUhNYlZDVURVbWRaLXZmVzdBTHpHM2ZrRk9aeTVGZVlQRTl1ZncxaDZrNEFJdmphYzNEckJSb0RnZ3EzODBwZkpaNVI2OEVWUGVNUGg4UDkybUdEV3huS3lOTTAzVmxMY2JvWUpOdmFZekNCc0hCQVRqZW0xa0ZlYl95a0Q4d2w1R09YUERR?oc=5) ⭐️ 6.0/10

The European Union has formally warned TikTok that it may face fines for failing to adequately protect children&\#x27;s safety on its platform, citing potential violations of the Digital Services Act. This enforcement action underscores the EU&\#x27;s commitment to holding large platforms accountable under the DSA, setting a precedent for child safety regulation across the tech industry. The warning is part of ongoing investigations under the DSA, which imposes strict obligations on Very Large Online Platforms like TikTok, including risk assessments and mitigation measures for minors.

rss · GoogleNews-欧盟监管 · Jul 24, 12:19

**Background**: The Digital Services Act \(DSA\) is an EU regulation that entered into force in 2022, establishing comprehensive rules for digital services, including content moderation and platform transparency. It applies to all online intermediaries, with stricter requirements for Very Large Online Platforms \(VLOPs\) serving over 45 million EU users. TikTok was designated as a VLOP in April 2023, making it subject to enhanced obligations under the DSA.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act">Digital Services Act</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/digital-services-act">The Digital Services Act | Shaping Europe’s digital future</a></li>

</ul>
</details>

**Tags**: `#EU regulation`, `#TikTok`, `#Digital Services Act`, `#child safety`, `#platform governance`

---