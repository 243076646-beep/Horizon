---
layout: default
title: "Horizon Summary: 2026-07-23 (EN)"
date: 2026-07-23
lang: en
---

> From 24 items, 11 important content pieces were selected

---

1. [Terence Tao Uses ChatGPT to Explore Jacobian Conjecture Counterexample](#item-1) ⭐️ 9.0/10
2. [GigaToken: ~1000x faster language model tokenization](#item-2) ⭐️ 8.0/10
3. [Bento packs entire PowerPoint into a single offline HTML file](#item-3) ⭐️ 8.0/10
4. [AI Labs&\#x27; SVG Biases: Pelicans on Bicycles Always Face Right](#item-4) ⭐️ 8.0/10
5. [Tech Journalist John C. Dvorak Dies at 78](#item-5) ⭐️ 7.0/10
6. [Does using LLMs count as &\#x27;making&\#x27;?](#item-6) ⭐️ 7.0/10
7. [Postgres Survival Guide for Startups](#item-7) ⭐️ 7.0/10
8. [EU AI Act 2026: Key Changes and Deployer Obligations](#item-8) ⭐️ 7.0/10
9. [EU AI Act Article 50 Compliance Checklist Now Available](#item-9) ⭐️ 7.0/10
10. [France Bans Social Media for Under-15s But Weakens Enforcement](#item-10) ⭐️ 6.0/10
11. [EU AI Transparency Rules Take Effect August 2 for German Firms](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Terence Tao Uses ChatGPT to Explore Jacobian Conjecture Counterexample](https://chatgpt.com/share/6a5fdc7a-d6f8-83e8-bbea-8deb42cfed56) ⭐️ 9.0/10

Renowned mathematician Terence Tao published a ChatGPT conversation where he collaboratively explores a recently discovered counterexample to the Jacobian conjecture, using the AI to analyze polynomial maps and verify properties. This demonstrates how leading mathematicians can leverage large language models as active research assistants, potentially accelerating discovery and verification in pure mathematics. The counterexample was initially discovered using Anthropic&\#x27;s Claude Fable 5 model and presented by mathematician Levent Alpöge on July 19, 2026; Tao&\#x27;s conversation focuses on understanding the structure and implications of this explicit counterexample in three dimensions.

hackernews · gmays · Jul 22, 17:30 · [Discussion](https://news.ycombinator.com/item?id=49010345)

**Background**: The Jacobian conjecture is a longstanding problem in algebraic geometry stating that a polynomial map with a nonzero constant Jacobian determinant must have a polynomial inverse. It has been open for over a century, with many false proofs published. The recent counterexample disproves the conjecture for dimensions greater than 2, though the 2-dimensional case remains unsolved.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jacobian_conjecture">Jacobian conjecture</a></li>

</ul>
</details>

**Discussion**: Commenters were fascinated by how Tao&\#x27;s precise questioning extracts deep insights from ChatGPT, noting that without his expertise the same prompts would not yield such results. Some highlighted the similarity to their own AI usage patterns, while others appreciated the structured progression of the conversation.

**Tags**: `#AI`, `#mathematics`, `#LLM`, `#research`, `#Jacobian conjecture`

---

<a id="item-2"></a>
## [GigaToken: ~1000x faster language model tokenization](https://github.com/marcelroed/gigatoken/) ⭐️ 8.0/10

GigaToken is a new tokenization library that achieves approximately 1000x speed improvement over conventional tokenizers by leveraging SIMD instructions and optimized caching for pretokenization mappings. This speedup significantly reduces time and cost for offline data preparation and pretraining of large language models, enabling faster iteration cycles when processing terabytes of text. GigaToken supports a wide range of CPU hardware \(modern x86 and ARM\) and nearly all commonly used tokenizers, with optimizations focused on pretokenization which is typically handled by a regex engine.

hackernews · syrusakbary · Jul 22, 17:20 · [Discussion](https://news.ycombinator.com/item?id=49010167)

**Background**: Tokenization is the process of converting text into subword units \(tokens\) that language models can process. It is typically a small fraction of inference time \(less than 0.1%\) but can be a significant bottleneck when preprocessing large training datasets. SIMD \(Single Instruction, Multiple Data\) is a parallel computing technique that allows a processor to perform the same operation on multiple data points simultaneously, which GigaToken exploits to accelerate the regex-based pretokenization step.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/marcelroed/gigatoken">marcelroed/gigatoken: Language model tokenization at GB/s - GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49010167">GigaToken: ~1000x faster Language model tokenization | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The community is impressed by the performance claims, with one commenter calling it &\#x27;mind-bending.&\#x27; However, some note that tokenization is a minor part of inference, suggesting the value is greater for offline data prep. The author clarifies that optimizations are consistent across CPUs and tokenizers, not over-optimized for a specific setup.

**Tags**: `#tokenization`, `#performance`, `#LLM`, `#SIMD`, `#optimization`

---

<a id="item-3"></a>
## [Bento packs entire PowerPoint into a single offline HTML file](https://bento.page/slides/) ⭐️ 8.0/10

Bento is a new tool that packages a full presentation editor, viewer, data, and collaboration features into a single self-contained HTML file that works entirely offline without any server or cloud login. This approach eliminates the need for cloud dependencies and internet connectivity, making presentations easy to share, edit, and collaborate on—simply by sending a file. It resonates with developers who value simplicity and offline-first tools. The default deck is about 560 KB and uses reveal.js along with homegrown libraries; the app logic is stored in a base64 blob that decompresses in the browser using DecompressionStream. Collaboration is achieved via an encrypted blind relay that cannot see the data.

hackernews · starfallg · Jul 22, 15:19 · [Discussion](https://news.ycombinator.com/item?id=49008211)

**Background**: Traditional presentation tools like PowerPoint or Google Slides require installation or cloud connectivity. Single-file web apps bundle an entire application into one HTML file, allowing it to run offline in any browser. Reveal.js is a popular HTML presentation framework, and blind relays enable end-to-end encrypted data transfer without the relay accessing the content.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blinding_%28cryptography%29">Blinding (cryptography) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The creator explained the file structure \(JSON data plus base64-encoded app logic\), and many commenters praised the concept, with some noting potential performance issues under heavy concurrent editing, such as an M1 Mac freezing during the guestbook demo.

**Tags**: `#web tool`, `#presentation`, `#single-file app`, `#collaboration`, `#offline`

---

<a id="item-4"></a>
## [AI Labs&\#x27; SVG Biases: Pelicans on Bicycles Always Face Right](https://dylancastillo.co/posts/pelicanmaxxing.html) ⭐️ 8.0/10

Dylan Castillo systematically generated 1008 SVGs across 7 AI labs and 48 animal-vehicle combinations, finding that all 21 pelican-on-bicycle images face right, a unique bias not seen in other combinations. This bias suggests potential training data contamination or systematic curation, raising concerns about the reliability of AI benchmarks and the integrity of model evaluations. The analysis covered 7 labs including OpenAI, Google, and Anthropic, generating 1008 SVGs in total, with 60% of all images facing right, but pelican-bicycle was the only combination with 100% right-facing consistency across all labs.

hackernews · dcastm · Jul 22, 17:17 · [Discussion](https://news.ycombinator.com/item?id=49010129)

**Background**: Training data contamination occurs when evaluation data leaks into training, inflating performance metrics. SVG generation by AI models involves creating vector graphics from text prompts. This study tests unusual combinations to detect if models have been specifically trained on certain concepts.

<details><summary>References</summary>
<ul>
<li><a href="https://www.holisticai.com/blog/overview-of-data-contamination">An Overview of Data Contamination: The Causes, Risks, Signs, and Defenses</a></li>
<li><a href="https://www.svggenie.com/blog/ai-svg-generator-comparison-2025">Best AI SVG Generators in 2026: 7 Tools Tested Head-to-Head</a></li>

</ul>
</details>

**Discussion**: Comments highlight the methodological rigor and discuss the possibility of labs cheating on specific benchmarks. Users also note other biases, like otters depicted correctly on planes, which may indicate targeted training on popular examples.

**Tags**: `#AI`, `#image generation`, `#SVGs`, `#training data`, `#ML`

---

<a id="item-5"></a>
## [Tech Journalist John C. Dvorak Dies at 78](https://twitter.com/na_announce/status/2079952538040672302) ⭐️ 7.0/10

John C. Dvorak, a prominent technology journalist known for his provocative columns and long tenure at PC Magazine and as a frequent podcaster on TWiT, has passed away. The announcement was made via social media and community forums on March 8, 2026. Dvorak was a iconic figure in tech journalism, influencing generations of readers and commentators. His death marks the end of an era in computing media, prompting reflection on the evolution of technology reporting. Dvorak was the nephew of August Dvorak, inventor of the Dvorak keyboard layout. He wrote for publications including InfoWorld and MacUser, and was a regular on the podcast &\#x27;No Agenda&\#x27; and &\#x27;This Week in Tech&\#x27; \(TWiT\) until a falling out with host Leo Laporte.

hackernews · coleca · Jul 22, 19:22 · [Discussion](https://news.ycombinator.com/item?id=49012070)

**Background**: John C. Dvorak \(1946-2026\) was a veteran tech journalist whose career spanned from the 1980s to the 2020s. He was known for his contrarian and often humorous takes on the tech industry. His columns in PC Magazine and other outlets were widely read, and he later became a fixture in the podcasting world, co-hosting shows like &\#x27;No Agenda&\#x27; with Adam Curry. Despite controversies and disagreements, he remained a respected voice in tech commentary.

**Discussion**: The community expressed deep respect and nostalgia, with many recalling Dvorak&\#x27;s bold takes and the fun of reading his columns in the 80s and 90s. Commenters highlighted his knack for guessing software features from box art and his humorous interactions with Leo Laporte. Some noted his falling out with Laporte and Adam Curry&\#x27;s religious turn, but overall the tone was appreciative of his lasting impact.

**Tags**: `#John C. Dvorak`, `#tech journalism`, `#obituary`, `#PC Magazine`, `#TWiT`

---

<a id="item-6"></a>
## [Does using LLMs count as &\#x27;making&\#x27;?](https://beej.us/blog/data/ai-making/) ⭐️ 7.0/10

Beej published a blog post on his website reflecting on whether using large language models \(LLMs\) to produce work qualifies as &\#x27;making&\#x27;, sparking a heated community discussion on Hacker News with over 250 points and 100 comments. This debate touches on core questions about creativity, authorship, and the value of human effort in an era where AI can generate code, art, and text. It matters for software engineers, artists, and anyone who uses AI tools to create, as it forces a re-examination of what we consider genuine creation. The author compares using an LLM to hiring a landscaper: you still take pride in the result even if you didn&\#x27;t do the manual work. A commenter distinguishes &\#x27;making&\#x27; by the extent one can reason about how input changes affect output, drawing a line between doing and asking to be done.

hackernews · erikschoster · Jul 22, 15:33 · [Discussion](https://news.ycombinator.com/item?id=49008440)

**Background**: Large language models \(LLMs\) like GPT-4 are AI systems trained on vast text data to understand and generate human language. They can produce code, articles, and creative works, raising longstanding philosophical questions about machine creativity and whether AI-generated outputs can be considered original or truly creative.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What Are Large Language Models (LLMs)? | IBM</a></li>

</ul>
</details>

**Discussion**: Commenters were divided: some feel pride in LLM-assisted creations, viewing the LLM as a tool like any other, while others miss the joy of hands-on making and worry about losing human ingenuity. A notable point was that the ability to reason about cause and effect distinguishes genuine making from merely prompting.

**Tags**: `#AI`, `#LLM`, `#software engineering`, `#philosophy of making`, `#creativity`

---

<a id="item-7"></a>
## [Postgres Survival Guide for Startups](https://hatchet.run/blog/postgres-survival-guide) ⭐️ 7.0/10

A practical blog post titled &\#x27;The startup&\#x27;s Postgres survival guide&\#x27; was published on Hatchet, covering common PostgreSQL pitfalls and best practices for startups. This guide is highly relevant for startups as it addresses frequent issues like indexing, vacuuming, and ORM usage that can impact database performance and reliability. The guide emphasizes practices such as using UUIDv7 over UUIDv4, avoiding ORMs, and implementing append-only patterns, but notably omits backup strategies according to community feedback.

hackernews · abelanger · Jul 22, 12:36 · [Discussion](https://news.ycombinator.com/item?id=49005787)

**Background**: PostgreSQL is a powerful open-source relational database often used by startups. Common challenges include performance tuning via indexing and vacuuming, and avoiding pitfalls like deadlocks and table bloat. Proper indexing strategies and regular autovacuum configuration are critical for maintaining performance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.mydbops.com/blog/postgresql-indexing-best-practices-guide">PostgreSQL Index Best Practices for Faster Queries | Mydbops</a></li>
<li><a href="https://www.enterprisedb.com/blog/postgresql-vacuum-and-analyze-best-practice-tips">PostgreSQL VACUUM Guide and Best Practices | EDB</a></li>

</ul>
</details>

**Discussion**: Commenters suggest adding backup strategies, using UUIDv7, and avoiding ORMs. Some warn against cascading deletes and recommend deterministic lock ordering. Overall sentiment is positive but with practical corrections.

**Tags**: `#PostgreSQL`, `#startup`, `#database`, `#best-practices`

---

<a id="item-8"></a>
## [EU AI Act 2026: Key Changes and Deployer Obligations](https://news.google.com/rss/articles/CBMixAFBVV95cUxQZVJ1NDNlbXIyWDBLeUVRSDFSVXkyMWlhZ0FSV1NwR1cxWlJDZExVakp0TzhsTXhhZ3RhV0MzaHpKOTA4cWU2c3lXRDM5RlNLcHlhcy05WjZUd2NCWUhYSWJNUEMzQkc2MnZteVkzaFM4aFF0RmJCc0JPSE1xTTZoXzI1UHRaa2NPR0toWk9SUVdhUUF1c1MzSTNEUEltUERXLXY3Q1dPYVBqYXZsWEd6T3N6alA3WkhkT2k4Tkg2ZFJURU5K0gHEAUFVX3lxTFBlUnU0M2VtcjJYMEt5RVFIMVJVeTIxaWFnQVJXU3BHVzFaUkNkTFVqSnRPOGxNeGFndGFXQzNoeko5MDhxZTZzeVdEMzlGU0tweWFzLTlaNlR3Y0JZSFhJYk1QQzNCRzYydm15WTNoUzhoUXRGYkJzQk9ITXFNNmhfMjVQdFprY09HS2haT1JRV2FRQXVzUzNJM0RQSW1QRFctdjdDV09hUGphdmxYR3pPc3pqUDdaSGRPaThOSDZkUlRFTko?oc=5) ⭐️ 7.0/10

An article published on Process Excellence Network outlines the key changes in the EU AI Act that take effect in 2026 and summarizes the ongoing obligations for deployers of high-risk AI systems. This update is critical for organizations deploying AI in the EU, as it clarifies evolving compliance requirements and emphasizes that deployers must still adhere to human oversight and data protection obligations. Deployers of high-risk AI systems must use the information provided by providers to conduct data protection impact assessments and implement human oversight measures, and these obligations are without prejudice to other national laws.

rss · GoogleNews-欧盟监管 · Jul 22, 10:17

**Background**: The EU AI Act is a comprehensive legal framework that regulates AI systems based on their risk level. High-risk AI systems, such as those used in critical infrastructure or employment, face stringent requirements including transparency, accuracy, and human oversight. Deployers are entities that use such systems in a professional capacity and are responsible for compliance with specific operational obligations.

<details><summary>References</summary>
<ul>
<li><a href="https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-26">AI Act Service Desk - Article 26: Obligations of deployers of ...</a></li>
<li><a href="https://artificialintelligenceact.eu/article/26/">Article 26: Obligations of Deployers of High-Risk AI Systems</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#deployers`

---

<a id="item-9"></a>
## [EU AI Act Article 50 Compliance Checklist Now Available](https://news.google.com/rss/articles/CBMipgFBVV95cUxPUVlzdHc5cC1ZM1VHeXNIbWJWMEMtbVdBamE4cnRjUmpWY2dzR2lVX2V1el9ORGFhVnhtR1dJSEx6ZzhPTHhqdjFUWjlFLWJkdGRMZXRwaG9sMHljMmxPZVNWb2pLdmZic1Y0WFFQSXRfeU9WcTlNS09YOWtiVnBPemwwZjZLblNfTnlPa1RzZzYwWE9EVko1UFl4RHJDQUsySGJJWDhB?oc=5) ⭐️ 7.0/10

Resemble AI has published a compliance checklist for Article 50 of the EU AI Act, targeting both providers and deployers. The checklist details transparency obligations for AI systems that interact with humans or generate synthetic content. This checklist helps AI stakeholders prepare for the enforcement of Article 50 on August 2, 2026, avoiding fines of up to €15 million or 3% of global annual turnover. It also clarifies the distinct responsibilities of providers and deployers under the EU AI Act. Article 50 transparency obligations become enforceable on August 2, 2026, with a Code of Practice expected by June 2026. Non-compliance can result in significant financial penalties under Article 99\(4\)\(g\) of the Act.

rss · GoogleNews-欧盟监管 · Jul 22, 18:01

**Background**: The EU AI Act entered into force on August 1, 2024, and applies in stages. Article 50 sets transparency requirements for AI systems that interact with humans, generate synthetic content, or use emotion recognition. Providers are responsible for designing the AI system and bear the heaviest compliance burden, while deployers \(users\) have fewer obligations. The checklist serves as a practical tool to help both parties meet these requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://gdprlocal.com/eu-ai-act-article-50/">EU AI Act Article 50 : Transparency Rules for Businesses - GDPR Local</a></li>
<li><a href="https://humantext.pro/blog/eu-ai-act-article-50-explained">EU AI Act Article 50 Explained: Practical Compliance</a></li>
<li><a href="https://www.aoshearman.com/en/insights/ao-shearman-on-tech/zooming-in-on-ai-4-what-is-the-interplay-between-deployers-and-providers-in-the-eu-ai-act">EU AI Act: roles of providers and deployers explained</a></li>

</ul>
</details>

**Tags**: `#EU AI Act`, `#compliance`, `#regulation`, `#AI governance`

---

<a id="item-10"></a>
## [France Bans Social Media for Under-15s But Weakens Enforcement](https://news.google.com/rss/articles/CBMitgFBVV95cUxNTlByMm9GLXdMaXRaQXdGXzY5R25tUDlld3YyUk1uZkFrODhEdXZIcGV3Znp0dlNKVTlyM1hyVlo3Ymo1QWw5dDFUVEM3SWxqTGhfSG15cEVBdjFJSVB0NkVLTDRFbFFVSVpJc1gwUi1KekdtMEdJb0swejNvY3RmeEQxV3doMDVHcXdBczNfeEtLcHdpaHFucmhHeFphRFlpQW5RYWc1T0JNd0lpRjlNOTJuT1ZMdw?oc=5) ⭐️ 6.0/10

France has passed a law banning social media for children under 15, but the enforcement mechanism has been significantly weakened, reducing the law&\#x27;s immediate impact. This law represents a major regulatory step in child online safety, but the lack of robust enforcement may set a precedent for other countries considering similar measures. The law requires social media platforms to verify users&\#x27; ages and obtain parental consent for minors under 15, but the enforcement mechanism—such as fines or technical checks—was cut, making compliance largely voluntary.

rss · GoogleNews-欧盟监管 · Jul 22, 18:18

**Background**: France has been active in regulating digital platforms to protect minors, with previous proposals including mandatory age verification and parental controls. This law is part of a broader European trend toward stricter online safety regulations, but practical enforcement challenges often lead to compromises. The weakened enforcement mechanism reflects tensions between child protection goals and industry feasibility concerns.

**Tags**: `#social media`, `#regulation`, `#France`, `#online safety`, `#policy`

---

<a id="item-11"></a>
## [EU AI Transparency Rules Take Effect August 2 for German Firms](https://news.google.com/rss/articles/CBMiyAFBVV95cUxQaTlRMnl5Tm1ob0NxelctSTdhcGdIRElFaUZMNmRmcWlJWHNUUFlGLWlFRFptd3lvRmRTUVVQRHJJSmVvY09nS2M4cDJpSFJYR1M5dWpjMlNPWFZmOFVLbHhKclZoaE1od2xRYTJnLVpWRUtWb0hlUDJOZWN2enA1X0duUmZPNC1yTXhlU2JxNWV0ajdjQUJ0T1pDQWZ3bHFJQlhuUGZFZG1wWXFUbTJlME9xQnVhd3p4eGc0ZVBrNHVoc3Q4MnEzOA?oc=5) ⭐️ 6.0/10

German companies must comply with new EU AI transparency rules by August 2, 2026, as Article 50 of the EU AI Act takes effect for new AI systems. This deadline marks the first enforceable transparency obligations under the EU AI Act, requiring companies to label AI-generated content and inform users when interacting with AI systems, impacting a wide range of businesses. Systems released before August 2 have until December 2, 2026 to comply, and the obligations apply broadly to AI systems that interact with humans, generate deepfakes, or provide emotion recognition.

rss · GoogleNews-欧盟监管 · Jul 22, 18:43

**Background**: The EU AI Act, enacted in August 2024, is the first comprehensive AI regulation. Article 50 mandates transparency for low-risk AI systems, such as chatbots and content generators, while high-risk systems have stricter requirements. The August 2 deadline specifically triggers obligations for new systems placed on the market after that date.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialintelligenceact.eu/transparency-rules-article-50/">The EU AI Act’s Transparency Rules: A Practical Guide to ...</a></li>
<li><a href="https://www.theregister.com/ai-and-ml/2026/07/20/eus-ai-labeling-rules-take-effect-next-month/5274917">EU &#x27;s AI labeling rules take effect next month</a></li>
<li><a href="https://www.euractiv.com/news/how-eu-ai-transparency-rules-will-change-what-you-see-online/">How EU AI transparency rules will change what you see... | Euractiv</a></li>

</ul>
</details>

**Tags**: `#EU regulation`, `#AI transparency`, `#compliance`, `#Germany`

---