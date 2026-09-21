---
layout: default
title: "Horizon Summary: 2026-09-21 (EN)"
date: 2026-09-21
lang: en
---

> From 15 items, 4 important content pieces were selected

---

1. [Samsung to more than double HBM4 and HBM4E output next year](#item-1) ⭐️ 8.0/10
2. [Qwen Image 2.1: a 7B open-weight image model with native transparency](#item-2) ⭐️ 8.0/10
3. [ChatGPT Reportedly Gets Cross-Site Tracking Data From Ad Collectors](#item-3) ⭐️ 7.0/10
4. [Pirate Face Rescues Deleted LLM Weights via BitTorrent](#item-4) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Samsung to more than double HBM4 and HBM4E output next year](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say) ⭐️ 8.0/10

Samsung is expected to more than double its output of HBM4 and HBM4E DRAM in the coming year, according to industry sources cited in a September 2026 report. The expansion covers both the base HBM4 generation and its enhanced HBM4E successor, which Samsung has said it plans to build in 16-layer stacks. HBM is the key bottleneck in AI accelerator supply, so a major capacity increase from Samsung could loosen constraints on GPUs and custom AI chips, while also intensifying competition with SK hynix and Micron in the high-margin HBM market. Because HBM wafers consume roughly three times the capacity of equivalent DDR5 wafers, this ramp will also reshape the broader DRAM market and consumer memory pricing. HBM4 moves to a 2,048-bit interface and a logic-based base die that can be customized for individual customers, while HBM4E pushes pin speeds, process nodes and packaging further; as of mid-2026 no confirmed GPU product had shipped with HBM4E. The report is based on unnamed sources, so exact volume figures, timing and which customers receive the extra supply remain unconfirmed.

hackernews · giuliomagnifico · Sep 20, 17:38 · [Discussion](https://news.ycombinator.com/item?id=49778029)

**Background**: High Bandwidth Memory \(HBM\) is a type of DRAM in which multiple memory dies are stacked vertically and connected with through-silicon vias \(TSVs\), then placed on a base die right next to an AI accelerator such as an Nvidia or AMD GPU. This packaging gives HBM far higher bandwidth than conventional DIMM memory, which is why it is essential for training and serving large language models. HBM4 is the JEDEC-standardized generation succeeding HBM3E, and HBM4E is an enhanced follow-on built on the same platform. Producing HBM is difficult and expensive, and because it uses so much wafer capacity, every HBM ramp directly compresses supply of ordinary commodity DRAM.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.ersaelectronics.com/blog/hbm4-hbm4e">HBM4 compared to HBM4E</a></li>
<li><a href="https://xenospectrum.com/en/what-is-hbm-high-bandwidth-memory/">What Is HBM ? The Stacked DRAM Architecture That... | XenoSpectrum</a></li>

</ul>
</details>

**Discussion**: Commenters focused on supply-chain consequences: one noted that China&\#x27;s AI accelerator output, notably Huawei&\#x27;s Ascend, is limited less by processor dies or ASML EUV access than by CXMT&\#x27;s HBM capacity. Others flagged die-thinning as an underappreciated but economically vital manufacturing step, worried that Samsung&\#x27;s HBM expansion will push consumer DRAM prices even higher, asked what besides cost blocks HBM from serving as primary memory in consumer devices, and questioned whether even this added capacity can satisfy AI&\#x27;s demand.

**Tags**: `#HBM4`, `#Samsung`, `#DRAM`, `#AI hardware`, `#semiconductor supply chain`

---

<a id="item-2"></a>
## [Qwen Image 2.1: a 7B open-weight image model with native transparency](https://qwen.ai/blog?id=qwen-image-2.1) ⭐️ 8.0/10

Qwen released Qwen Image 2.1, a new 7B-parameter open-weight image generation model that is substantially smaller than its predecessor Qwen-Image 1 \(20B parameters\), while adding significantly improved text rendering and native transparency support. The release drew heavy attention on Hacker News \(479 points, 151 comments\) for its compact size and its ability to generate legible small text. A capable 7B image model lowers the hardware bar for local, self-hosted image generation, putting it in a class with only a handful of competitors such as the 6B Z-Image Turbo while remaining far smaller than Ideogram, Krea2 and Flux2. Its text-rendering strength is especially relevant for design and prompt-to-UI workflows, where legible typography has historically been the weak point of open-weight image models. At 7B parameters the model is far smaller than Qwen-Image 1&\#x27;s 20B, and commenters note that native transparency support is something essentially only Qwen is attempting among open-weight image generators, since others require background-removal postprocessing. The main caveat raised is licensing: unlike many earlier Qwen releases that used permissive Apache-style terms, Qwen Image 2.1 ships under a notably more restrictive license, which could limit commercial and downstream use.

hackernews · jmillikin · Sep 20, 13:09 · [Discussion](https://news.ycombinator.com/item?id=49775499)

**Background**: Open-weight models are AI systems whose trained parameters \(weights and biases\) are published for others to download and run, though the permission to modify, fine-tune or redistribute them depends on the accompanying license — a permissive Apache or MIT license is common for Chinese labs, while US labs often keep large models proprietary. Qwen \(also known as Tongyi Qianwen\) is Alibaba Cloud&\#x27;s family of predominantly open-weight models, spanning language and multimodal generation. Text rendering has long been a known weakness of diffusion-based image generators, which often produce garbled letters, so improvements there are a common benchmark of progress.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion was largely positive on the model&\#x27;s compact 7B size and its text rendering, with one commenter who runs a prompt-to-UI design site reporting that small-text fidelity is &\#x27;much, much better than anything else on the open weights market right now,&\#x27; backed by side-by-side tests against gpt-image-2. The main pushback was about licensing, since earlier Qwen models were often Apache-licensed while Qwen Image 2.1 uses a more restrictive one. Others debated why local image generation feels more advanced than local code generation, and asked how to serve the model locally in the way llama-server runs an LLM.

**Tags**: `#AI/ML`, `#image-generation`, `#open-weight-models`, `#Qwen`, `#text-rendering`

---

<a id="item-3"></a>
## [ChatGPT Reportedly Gets Cross-Site Tracking Data From Ad Collectors](https://www.buchodi.com/chatgpt-now-knows-what-you-do-on-other-websites-via-ad-collector/) ⭐️ 7.0/10

A blog post on buchodi.com reports that ChatGPT now receives cross-site behavioral data gathered by ad-tracking collectors \(adtech pixels/scripts\), and the item triggered a large Hacker News discussion \(about 570 points and 307 comments\). The claim is that standard advertising tracking infrastructure is now running inside an AI chat product used by hundreds of millions of people. Adtech tracking has long been normalized on the open web, but embedding it in an AI assistant matters because chat products accumulate unusually sensitive context, including questions users would never type into a search engine. If OpenAI sets this precedent, other AI chat providers may follow, reshaping privacy expectations for a whole product category that regulators are already scrutinizing. The underlying mechanism is described as ordinary adtech rather than a new technique — what is unprecedented is applying it to an AI chat product. The blog post itself drew credibility criticism in the comments, where a user linked to an AI-detection report \(Pangram\) and argued the article was AI-generated, and another commenter pointed to MDN documentation showing that Firefox, Brave and Safari block these cross-site mechanisms while Chrome and Edge do not.

hackernews · lmbbuchodi · Sep 20, 15:18 · [Discussion](https://news.ycombinator.com/item?id=49776729)

**Background**: Ad tracking is the practice of using cookies, tracking pixels and unique tracking URLs to record how people interact with ads and pages, which lets advertisers measure campaigns and build behavioral profiles. Because third-party cookies are increasingly blocked, trackers have turned to alternatives such as bounce tracking \(capturing data during a redirect through an intermediate domain\) and browser fingerprinting, which sit outside typical cookie consent banners. Cross-site behavioral data is what allows an ad system to know you searched for a product on one site and then show you an ad for it on another. ChatGPT is OpenAI&\#x27;s AI chat assistant, used by hundreds of millions of people.

<details><summary>References</summary>
<ul>
<li><a href="https://www.avg.com/en/signal/what-is-ad-tracking">What is Ad Tracking, How it Works &amp; How to Stop it</a></li>
<li><a href="https://www.advergize.com/glossary/bounce-tracking/">What Is Bounce Tracking ? - Advergize</a></li>
<li><a href="https://noahkenney.com/insight-third-party-tracking.html">Why Third-Party Tracking Is Being... | Noah Kenney Insight Report</a></li>

</ul>
</details>

**Discussion**: Commenters were largely uneasy, with one comparing the experience to Facebook&\#x27;s cross-site ad targeting that drove them away from that platform and noting they had already seen Gemini weave personal context into an answer. Others welcomed the EU&\#x27;s regulatory push against such practices, and one top comment crystallized the sentiment that while the mechanism is standard adtech, running it on an AI chat product has no precedent. A notable counterpoint was the accusation that the blog post was AI-generated, with a user linking an AI-detection result and suggesting the author should &quot;use your own words.&quot;

**Tags**: `#privacy`, `#adtech`, `#OpenAI`, `#web-tracking`, `#surveillance-capitalism`

---

<a id="item-4"></a>
## [Pirate Face Rescues Deleted LLM Weights via BitTorrent](https://pirateface.co/) ⭐️ 7.0/10

Pirate Face \(pirateface.co\) has emerged as a torrent-based service that lets anyone browse, download, and seed AI model weights without signing up, positioning itself as a discovery, provenance, and community layer for open-weight models. It offers optional Hugging Face handle verification intended to prevent impersonation and let creators claim ownership of their releases. By moving model weights onto BitTorrent, the project offers a censorship-resistant alternative to centralized hosts like Hugging Face, which can remove or restrict models under legal or policy pressure. This matters for open-weight AI research, where the disappearance of a single repository can erase an entire model from public access. Pirate Face distributes models via standard torrent magnet links and currently lacks scripted torrent creation, and commentators note its name may be an awkward fit for institutional or academic use. The related technical debate points out that distributing &\#x27;abliterated&\#x27; weights may be unnecessary, since refusal behavior can instead be neutralized at runtime by orthogonalizing activations using a few thousand floats of refusal vectors per layer.

hackernews · skepticalgenius · Sep 20, 15:16 · [Discussion](https://news.ycombinator.com/item?id=49776699)

**Background**: BitTorrent is a peer-to-peer protocol in which files are split into pieces and shared among many users \(peers\), so no single server is a point of failure; Blizzard famously used it to deliver World of Warcraft and StarCraft II updates before CDNs became cheap. Abliteration is a technique that removes a language model&\#x27;s built-in refusal mechanism, letting it comply with prompts it would normally decline, without retraining the model. Decentralized AI distribution refers to spreading models, data, or compute across independent nodes rather than relying on one provider.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/mlabonne/abliteration">Uncensor any LLM with abliteration</a></li>
<li><a href="https://abliteration.ai/abliterated-llm">What is an abliterated LLM ? | abliteration .ai</a></li>
<li><a href="https://en.wikipedia.org/wiki/Distributed_artificial_intelligence">Distributed artificial intelligence - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters broadly support torrents as the natural distribution method for model weights, with phoyd asking why anyone would rely on a single point of failure like Hugging Face and mococa recalling Blizzard&\#x27;s torrent-based game delivery as precedent. The most technically substantive point comes from wren6991, who argues you can skip abliterated weights entirely: orthogonalizing the activations at runtime is equivalent and cheap, so you could just distribute the refusal vectors \(a few thousand floats per layer\) and run them against stock weights — a capability Antirez&\#x27;s DS4 reportedly already supports. JonChesterfield calls the work important but criticizes the unhelpful name and the absence of scripted torrent creation, and asks whether hosting the same content on Academic Torrents would be viable; one comment was deleted by its author.

**Tags**: `#LLM`, `#BitTorrent`, `#model distribution`, `#censorship`, `#abliteration`

---