---
layout: default
title: "Horizon Summary: 2026-09-11 (EN)"
date: 2026-09-11
lang: en
---

> From 15 items, 5 important content pieces were selected

---

1. [Shopify moves its mobile app from React Native back to native Swift and Kotlin](#item-1) ⭐️ 8.0/10
2. [Researchers question whether OpenAI can be trusted with unpublished math](#item-2) ⭐️ 8.0/10
3. [Cognition launches SWE-2 coding model to rival frontier models at lower cost](#item-3) ⭐️ 7.0/10
4. [NASA&\#x27;s Decorrelation Stretch Technique Reveals Faint Ancient Rock Art](#item-4) ⭐️ 7.0/10
5. [Microsoft designates Rust a tier-1 language](#item-5) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Shopify moves its mobile app from React Native back to native Swift and Kotlin](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify&\#x27;s engineering team published a post explaining why it is migrating its flagship mobile app away from React Native back to fully native code, with separate Swift and Kotlin codebases for iOS and Android. The write-up, titled &quot;Back to Native,&quot; sparked a large Hacker News thread \(748 points, roughly 499 comments\) debating cross-platform versus native tradeoffs. Shopify is one of the most visible companies to reverse course on React Native, making this a high-profile case study in the long-running shared-codebase-versus-native debate that many mobile teams are still weighing. The discussion also raises a newer question: whether AI coding assistants have now made expensive native migrations economically viable where they previously were not. The public excerpt of the post does not include the specific engineering metrics Shopify used, but the surrounding debate centers on concrete pain points such as debugging crashes that span the JavaScript, C++ and native layers, plus the testing tooling involved in a rewrite. Commenters reference their own migrations using tools such as Maestro for UI testing and LLM coding agents to inventory and port screens.

hackernews · fnthawar2 · Sep 10, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49643982)

**Background**: React Native is Meta&\#x27;s open-source framework that lets developers write application logic and UI in JavaScript or TypeScript while rendering to real native components on both iOS and Android, so one codebase can serve two platforms. Going &quot;fully native&quot; means writing and maintaining separate Swift \(iOS\) and Kotlin \(Android\) apps, which costs more engineering effort but gives teams direct access to platform APIs, performance tuning and a smaller, simpler runtime. Companies have moved in both directions over the years, and each high-profile reversal is treated as evidence in the broader argument about whether cross-platform frameworks are worth their abstraction cost.

**Discussion**: Sentiment in the thread leans toward endorsing the move: several native engineers say they feel validated after years of arguing against shared codebases, and one commenter argues that debugging crashes across JS, C++ and native threads costs more than maintaining two codebases. A notable counterpoint comes from a commenter who led a mid-size React Native to Swift/Kotlin rewrite mostly before 2026 and without LLM assistance, disputing the narrative that AI tooling is what made such migrations affordable. Others share fast LLM-driven migration anecdotes, while one commenter argues that if code is increasingly generated anyway, there is little upside left in starting with React Native.

**Tags**: `#React Native`, `#Mobile Development`, `#Swift`, `#Kotlin`, `#Cross-Platform`

---

<a id="item-2"></a>
## [Researchers question whether OpenAI can be trusted with unpublished math](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

A Mathstodon thread by @andreasthom, amplified on Hacker News \(roughly 638 points and 615 comments\) and shared on X and Bluesky, questions whether researchers can trust OpenAI with their unpublished mathematics. The concern follows reports that OpenAI apparently drew on insights from collaborative chats with researchers without attributing them, and then disputed whether its results were actually derived from that data. This is a research-integrity and attribution dispute rather than a technical breakthrough, but it strikes at the trust relationship between frontier AI labs and the academic mathematicians whose unpublished work feeds them. If researchers conclude that sharing their open problems with a commercial model risks uncited absorption into a proprietary system, they may restrict access, which would slow both mathematical progress and the labs&\#x27; own claims about AI-driven discovery. The core technical argument is whether OpenAI&\#x27;s reported progress on open problems reflects memorization of researchers&\#x27; chats during pretraining or genuinely novel techniques discovered during reinforcement learning on verifiable math problems with massive compute. One commenter also flags as suspicious that OpenAI would generate 300 billion output tokens from a model still in training shortly after learning that a major math proof might have been in that model&\#x27;s training data.

hackernews · pred\_ · Sep 10, 06:49 · [Discussion](https://news.ycombinator.com/item?id=49639408)

**Background**: Mathstodon is a Mastodon instance for mathematicians that renders LaTeX in the web interface, so technical arguments circulate there in a form suitable for the field. Mastodon is a decentralized, federated social network, unlike single-company platforms, and the thread&\#x27;s links point to X \(often read through privacy front-ends such as xcancel\) and to Bluesky, whose accounts are identified by did:plc decentralized identifiers. In AI development, &quot;pretraining&quot; means learning statistical patterns from huge text corpora, while &quot;reinforcement learning&quot; \(RL\) trains a model against a reward signal, such as a verifier that can check whether a math proof is correct — the distinction matters because only the latter could plausibly produce results beyond what was in the training data.

<details><summary>References</summary>
<ul>
<li><a href="https://mathstodon.xyz/">A Mastodon instance for maths people. We have LaTeX rendering in...</a></li>
<li><a href="https://atproto.wiki/en/wiki/reference/identifiers/did-plc">DID:PLC | AT Protocol Community Wiki</a></li>
<li><a href="https://github.com/ryantenney/xcancel-forwarder/blob/main/README.md">xcancel -forwarder/README.md at main · ryantenney/ xcancel -forwarder</a></li>

</ul>
</details>

**Discussion**: Commenters largely treat the case as a test of OpenAI&\#x27;s ethics, with nezi arguing that if OpenAI were a human collaborator publishing work from a shared collaboration without attribution, it would be plainly unethical. sashank\_1509 offers the counterpoint that both explanations can be true at once — pretraining may sharpen the model&\#x27;s intuition while RL discovers genuinely superhuman techniques — whereas bertonvv worries the field may be fooled about how fast AI is actually solving open problems, and fwlr calls the timing of the 300-billion-token generation run suggestive of &quot;parallel construction.&quot;

**Tags**: `#AI ethics`, `#OpenAI`, `#research integrity`, `#attribution`, `#AI policy`

---

<a id="item-3"></a>
## [Cognition launches SWE-2 coding model to rival frontier models at lower cost](https://cognition.com/blog/swe-2) ⭐️ 7.0/10

Cognition, the company behind the autonomous coding agent Devin, announced SWE-2, its most advanced coding model, which scores 50.0% on FrontierCode 1.1 Main — within one point of Fable 5.1 — while costing up to 70% less. The company says it scaled reinforcement learning to the multi-trillion-parameter regime for the first time, building on the SWE-1.7 training infrastructure and recipe. A near-frontier coding model at a fraction of the cost could shift the economics of AI coding agents, pressuring closed-weight labs on price and giving developers a cheaper option for high-volume agentic workloads. It also intensifies the ongoing debate over how coding models are benchmarked and whether closed weights can compete with increasingly capable open alternatives. SWE-2 is reportedly post-trained from Kimi K3 rather than built as a fully new base model, and its weights appear to be closed. Critics point to the huge gap between its Terminal Bench 2.1 score \(92.8%\) and its Terminal Bench 4 score \(27.3%\), with the newer benchmark released only a couple of weeks earlier, as possible evidence of benchmark overfitting.

hackernews · seelos · Sep 10, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49645443)

**Background**: Cognition is an AI startup best known for Devin, one of the first commercial &\#x27;agentic&\#x27; coding tools that attempts to complete software tasks autonomously. Benchmarks like FrontierCode and Terminal Bench are standardized tests used to compare models on coding and command-line tasks, while &\#x27;Pareto frontier&\#x27; refers to the balance a model strikes between capability and cost. Reinforcement learning \(RL\) is the training technique used to improve a model&\#x27;s reasoning on such tasks, and open-weight models like those from DeepSeek give users the ability to run and inspect the model themselves.

<details><summary>References</summary>
<ul>
<li><a href="https://cognition.com/blog/swe-2">Introducing SWE-2: Pushing the Pareto Frontier | Cognition</a></li>
<li><a href="https://officechai.com/ai/cognition-releases-swe-2-says-it-performs-close-to-frontier-at-70-lower-cost/">Cognition Releases SWE-2, Says It Performs Close To Frontier ...</a></li>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-1">Introducing Claude Fable 5 . 1 and Claude Mythos 5 . 1 \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly skeptical: several flagged the Terminal Bench 2.1-versus-4 gap as evidence the model may be &\#x27;benchmaxxed&\#x27; rather than genuinely generalizing, and others questioned why anyone would choose another closed-weight model over DeepSeek Flash 4.1. Critics also resurfaced Cognition&\#x27;s past demo credibility issues and complaints about Devin&\#x27;s reliability, though some noted that since SWE-2 is built on the already-capable Kimi K3, it likely isn&\#x27;t bad.

**Tags**: `#AI/ML`, `#coding-agents`, `#model-release`, `#benchmarking`, `#open-weights`

---

<a id="item-4"></a>
## [NASA&\#x27;s Decorrelation Stretch Technique Reveals Faint Ancient Rock Art](https://spinoff.nasa.gov/Manipulating_Satellite_Photos_Now_Reveals_Ancient_Images) ⭐️ 7.0/10

NASA&\#x27;s decorrelation stretch, an image-enhancement method originally developed to sharpen satellite imagery of Mars and Earth, is now being applied to archaeology to recover ancient rock paintings that have faded almost to invisibility. The technique exaggerates subtle color differences that the human eye can no longer distinguish, pulling detail out of rock art, old aerial photographs, and film. This is a notable example of space-technology transfer, showing how a tool built for planetary and Earth-observation remote sensing can be repurposed for cultural heritage preservation and archaeology. It also highlights a broader lesson: optical sensors and human vision are not canonical ways of seeing the world, so processing multiband data can expose information that is otherwise lost forever. Decorrelation stretch is based on Principal Component Analysis: it removes inter-channel correlations in a multispectral image and rescales each channel&\#x27;s variance to target values, boosting color contrast. Researchers note that many rock-art motifs were clearly made with deliberate effort, but in most cases no one really knows why they were created.

hackernews · gumby · Sep 10, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49645437)

**Background**: Decorrelation stretch is an image-enhancement technique that emphasizes color differences by making an image&\#x27;s color planes uncorrelated and assigning them desired variances, which makes it useful for multispectral datasets. Related concepts include false-color composites, where wavelengths the human eye cannot see \(such as near-infrared\) are mapped to visible red, green, and blue channels; a classic example is vegetation appearing red instead of green because near-infrared is assigned to the red channel.

<details><summary>References</summary>
<ul>
<li><a href="https://morningoverview.com/a-nasa-photo-technique-is-now-pulling-lost-images-out-of-old-film/">A NASA photo technique is now pulling lost images out of old ...</a></li>
<li><a href="https://www.mdpi.com/2227-7390/13/20/3297">Numerical Methods for Decorrelation Stretch - MDPI</a></li>
<li><a href="https://en.wikipedia.org/wiki/False_color">False color - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters generally found the cross-domain reuse fascinating, with one sharing that false-color composites were a high-school and undergraduate &quot;Eureka\!&quot; moment about signals and sensors \(&quot;vegetation is red, not green\!&quot;\). Others offered hands-on replication tips—one described doing something similar in GIMP by decomposing to LAB, auto-leveling the A/B chroma channels, and recomposing—while another recounted a failed attempt to find hidden rock art at Angkor Wat using multiple bandpass filters.

**Tags**: `#remote-sensing`, `#image-processing`, `#archaeology`, `#signal-processing`, `#nasa-spinoff`

---

<a id="item-5"></a>
## [Microsoft designates Rust a tier-1 language](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 7.0/10

In a guest post published on the Rust Foundation site, Microsoft formally recognizes Rust as a tier-1 language, putting it alongside the company&\#x27;s traditionally first-class languages such as C, C++ and C\#. The announcement itself contains little new tooling, but it makes official a status that had previously only been hinted at in hiring posts and internal goals. All major OS vendors that also shape C and C++ tooling now offer a diversified set of systems-programming options for greenfield work, which strengthens Rust&\#x27;s position as an enterprise-grade choice rather than a niche experiment. It also raises expectations that Microsoft will deepen first-party support such as MSVC integration, which matters to anyone writing Windows-facing systems code. Commenters note the label is more about policy and support tiers than about a single product release, and point to Microsoft&\#x27;s stated ambition \(described as a hiring manager&\#x27;s vision-casting goal\) to convert 1 billion lines of code to Rust by 2030 through automated tooling at a rate of &\#x27;1 engineer, 1 month, 1 million lines of code&\#x27;. Rust&\#x27;s memory safety guarantees are the core technical motivation for such migrations, though automated conversion is still not fully reliable.

hackernews · mmastrac · Sep 10, 13:39 · [Discussion](https://news.ycombinator.com/item?id=49643546)

**Background**: Rust is a systems programming language that enforces memory safety and thread safety at compile time without a garbage collector, which makes it attractive for replacing C and C++ in security-sensitive code. At Microsoft, &\#x27;tier-1&\#x27; generally means a language receives first-class, fully supported tooling and platform integration rather than best-effort community support. The comparison languages in the discussion are Zig, a general-purpose C replacement first announced in 2016, and Odin, a data-oriented alternative to C created by Bill Hall starting in late 2016; both are considerably younger and less polished than Rust. DARPA&\#x27;s TRACTOR \(TRanslating All C TO Rust\) program funds multiple teams exploring automated C-to-Rust conversion to improve memory safety.

<details><summary>References</summary>
<ul>
<li><a href="https://andrewtetzeli.substack.com/p/yet-more-reasons-to-learnuse-rust">Yet more reasons to learn/use Rust : DARPA converting from C to Rust</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_%28programming_language%29">Zig (programming language)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Odin_%28programming_language%29">Odin ( programming language ) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was largely positive but measured: one top comment joked &\#x27;Embrace. Extend. &amp;lt;-- You are here. Extinguish.&\#x27;, while others surfaced concrete context such as Microsoft&\#x27;s 1-billion-line migration goal and DARPA-funded C-to-Rust transpilation research. Several commenters argued the news shows Rust is no longer a fast-moving fledgling and is now a mature competitor to C++ and C\#, with one long-time Rust developer saying they see no technical reason to choose another language for high-level application work; others cautioned that comparisons with newer &\#x27;better C/C++&\#x27; languages like Zig and Odin should account for those languages&\#x27; immaturity.

**Tags**: `#rust`, `#microsoft`, `#programming-languages`, `#systems-programming`, `#software-migration`

---