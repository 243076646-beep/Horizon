---
layout: default
title: "Horizon Summary: 2026-09-28 (EN)"
date: 2026-09-28
lang: en
---

> From 7 items, 3 important content pieces were selected

---

1. [Blog post questions Google Search&\#x27;s strange AI-powered results](#item-1) ⭐️ 7.0/10
2. [Fireworks AI Launches Ember-1, Its First In-House Reasoning Model Built on Kimi K3](#item-2) ⭐️ 7.0/10
3. [Meta Muse Shopping Agent Threatens Amazon&\#x27;s $50B Interface Control](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Blog post questions Google Search&\#x27;s strange AI-powered results](https://sancho.bearblog.dev/google-weird/) ⭐️ 7.0/10

A critical blog post titled &quot;When did Google get so weird?&quot; sparked a large Hacker News discussion \(751 points, 401 comments\) about how Google Search&\#x27;s AI-generated summaries and increasingly conversational results are changing the search experience. Commenters shared anecdotes of AI answers flatly contradicting reality, such as one user whose query about the Halifax Wanderers&\#x27; playoff chances returned a confident but false claim that the team had already secured a playoff spot. The debate sits at the center of a broader shift in how billions of people retrieve information, as Google, Microsoft and others replace link lists with LLM-generated answers. It raises hard questions about trust, factual reliability and the incentives of an ad-funded search engine that now speaks in its own voice rather than pointing users to sources. The core complaint is not that AI answers are useless but that they can be confidently wrong, and that recovering the correct answer requires users to scroll past the summary and manually re-verify sources. Commenters also noted the shift toward a conversational assistant has been framed by Google as an improvement, while critics argue it monetises attention and erodes users&\#x27; habit of checking primary sources.

hackernews · sancho-panza · Sep 27, 20:12 · [Discussion](https://news.ycombinator.com/item?id=49870367)

**Background**: Large language models are AI systems, typically transformer-based neural networks, trained on vast amounts of text to predict and generate language; they are the technology behind chatbots such as ChatGPT, Gemini and Claude, and increasingly behind AI search summaries. Because their outputs are generated probabilistically from training data, biased or inaccurate data can make them unreliable, which is why benchmark evaluations for reasoning, factual accuracy and safety exist. Google&\#x27;s AI Overviews place such generated text at the very top of search results, ahead of the traditional ranked links.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model</a></li>

</ul>
</details>

**Discussion**: Sentiment was sharply divided. Some commenters argued that ordinary users have always wanted &quot;a little guy in their computer&quot; to talk to, making this a genuine product win for Google, while others called it &quot;disturbing,&quot; accusing the tech industry of using AI-fuelled fear to boost its credibility. A notable thread argued the deeper issue is widespread loneliness, claiming people settle for parasocial relationships with software instead of asking real friends.

**Tags**: `#google`, `#search`, `#ai`, `#llm`, `#user-experience`

---

<a id="item-2"></a>
## [Fireworks AI Launches Ember-1, Its First In-House Reasoning Model Built on Kimi K3](https://fireworks.ai/blog/ember-1) ⭐️ 7.0/10

Fireworks AI announced Ember-1, its first Fireworks-branded model, a specialized reasoning model built on top of Kimi K3 that is designed to deliver comparable quality while producing far shorter reasoning traces — reportedly around 40% fewer tokens. It is available today through Fireworks&\#x27; serverless API \(pay-per-token, OpenAI-compatible clients\) and accepts text and images, supports tool calling and structured output, and offers a 1M-token context window. The release marks Fireworks&\#x27; shift from being purely an inference host for other labs&\#x27; open-weight models to also being a model developer, which could reshape how customers view its neutrality and vendor-lock-in risk. Token-efficiency gains also matter directly for agent workloads, where long reasoning traces dominate both latency and cost. Ember-1 is a post-trained derivative of Kimi K3 and is priced at the same $3/$15 per million tokens as the base model, so the savings come purely from emitting fewer tokens rather than from a cheaper rate; one third-party analysis cites up to 71% fewer reasoning tokens in some A/B tests while cautioning that for certain tasks keeping base K3 may still be better. Fireworks says it originally built the model as a starting checkpoint for continued post-training in vertical domains before realizing many users wanted the more concise, less verbose reasoning directly.

hackernews · gmays · Sep 27, 17:31 · [Discussion](https://news.ycombinator.com/item?id=49868830)

**Background**: Fireworks AI is an inference platform that specializes in fast, scalable serving of open-weight AI models, buying GPU capacity in bulk and routing across clouds so customers don&\#x27;t have to manage infrastructure themselves. Kimi K3 is a large open-weight reasoning model that Fireworks also serves, and &\#x27;reasoning&\#x27; models work by generating a long chain of intermediate thinking tokens before producing a final answer. Post-training refers to additional training applied after a model&\#x27;s initial pre-training, typically to specialize behavior — here, to make the reasoning traces much shorter at similar quality.

<details><summary>References</summary>
<ul>
<li><a href="https://fireworks.ai/blog/ember-1">Introducing Ember-1 - fireworks.ai</a></li>
<li><a href="https://www.explainx.ai/blog/fireworks-ember-1-kimi-k3-reasoning-tokens-2026">Ember-1: 71% Fewer Reasoning Tokens at K3 Price (2026 ...</a></li>
<li><a href="https://nano-gpt.com/models/text/fireworks/ember-1">Ember 1 model | NanoGPT</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was mixed: several commenters \(tukHelix, tangled\) questioned whether Fireworks, known primarily as an inference provider, entering model research creates trust or dependency concerns for customers who use it to serve other labs&\#x27; models, while jamienk argued open models tend to advance faster than proprietary ones, citing Linux and Wikipedia as precedents. GodelNumbering celebrated a &\#x27;golden age of model training,&\#x27; describing how they fine-tuned a Qwen 3 0.6B base model with 140k+ generated samples over about two days to build a strong English-to-Bash translation model, and netvarun noted off-topic that Kimi K3&\#x27;s price/quality value proposition is weakening now that Sol&\#x27;s pricing dropped.

**Tags**: `#LLM`, `#Fireworks AI`, `#open-source models`, `#model training`, `#AI inference`

---

<a id="item-3"></a>
## [Meta Muse Shopping Agent Threatens Amazon&\#x27;s $50B Interface Control](https://www.reddit.com/r/ecommerce/comments/1ws0hu4/meta_muse_may_cost_amazon_50b/) ⭐️ 7.0/10

A widely discussed analysis on r/ecommerce argues that Meta&\#x27;s newly launched Muse personal AI agent — which can shop on a user&\#x27;s behalf — could expose roughly $50B of Amazon&\#x27;s revenue, after Amazon blocked the agent from shopping on its site almost immediately. The author frames the block as less about safety or terms of use and more about Amazon defending ownership of the shopping interface itself. If AI agents become the front door to shopping, Amazon&\#x27;s storefront, search results, and sponsored listings lose much of their influence, since the agent — not the human — compares and picks products. Among the three exposed businesses, advertising is the most fragile because a sponsored listing that no human ever sees generates no value. The author tallies Amazon&\#x27;s FY2025 online stores at $269B, third-party seller services at $172B, and advertising at $69B — about $510B, or roughly 70% of Amazon — meaning a mere 10% shift in shopping intent would expose $50B, which is &quot;exposed, not lost overnight.&quot; Amazon&\#x27;s official justification for the block is expected to be safety, unauthorised access, and terms of use, and the post concedes Amazon still holds Prime, logistics, and trust.

reddit · r/ecommerce · /u/MustIReadIt · Sep 28, 00:40

**Background**: Meta launched Muse in September 2026 as a personal AI agent that can browse, fill forms, negotiate, and make purchases directly from a WhatsApp conversation, part of a broader shift toward &quot;agentic commerce&quot; in which AI agents research, negotiate and buy on a consumer&\#x27;s behalf under delegated authorization. Under the traditional e-commerce model, platforms like Amazon monetise the moment a shopper searches, browses and compares, because that is where ads and fees live; an agent that skips that page bypasses the monetisation entirely.

<details><summary>References</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for...</a></li>
<li><a href="https://www.stateofaimarketing.co/news/meta-muse-shopping-agent/">Meta Muse turns WhatsApp into a shopping agent</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-commerce">What is agentic commerce? - IBM</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#e-commerce`, `#Amazon`, `#Meta`, `#platform economics`

---