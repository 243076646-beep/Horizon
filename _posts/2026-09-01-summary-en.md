---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 13 items, 4 important content pieces were selected

---

1. [Google Removes Manifest V2 Extensions Including uBlock Origin from Chrome Web Store](#item-1) ⭐️ 8.0/10
2. [Turning Security Cameras into an Automatic Bird Identification System](#item-2) ⭐️ 7.0/10
3. [EU Tightens DSA Oversight on ChatGPT, Reddit, and Roblox](#item-3) ⭐️ 7.0/10
4. [Playa Phone Project: Hacker&\#x27;s Gift Connects Burning Man Community](#item-4) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Google Removes Manifest V2 Extensions Including uBlock Origin from Chrome Web Store](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has officially removed Manifest V2 \(MV2\) extensions from the Chrome Web Store, including the widely used ad blocker uBlock Origin. This is part of the browser&\#x27;s transition to Manifest V3 \(MV3\), which restricts extension capabilities. This move affects millions of users who relied on uBlock Origin for effective ad blocking and protection against malicious ads. It also raises concerns about Google&\#x27;s control over the web and the future of ad-blocking extensions, pushing some users to alternative browsers like Firefox. uBlock Origin used the webRequest API to block network requests in real time, an ability largely curtailed in Manifest V3. While an MV3 version, uBlock Origin Lite, exists, it is less powerful; users can still manually install MV2 extensions or switch to Firefox, where uBlock Origin remains fully supported.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: Manifest V2 is an older extension API standard that allowed extensions like uBlock Origin to intercept and block network requests before a page loads. In 2021, Google announced a shift to Manifest V3, claiming better security and performance, but critics like the Electronic Frontier Foundation argue it weakens privacy tools and innovation. uBlock Origin is a free, open-source content filter with tens of millions of users, making it one of the most popular extensions on both Chrome and Firefox.

<details><summary>References</summary>
<ul>
<li><a href="https://www.eff.org/deeplinks/2021/12/googles-manifest-v3-still-hurts-privacy-security-innovation">Google’s Manifest V 3 Still Hurts Privacy, Security, and Innovation</a></li>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">UBlock Origin</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>

</ul>
</details>

**Discussion**: Community reactions are largely negative, with users calling for a switch to Firefox. Commenters noted that ad blocking has become a safety necessity for vulnerable users, criticized Google&\#x27;s unilateral control over the web, and pointed out that uBlock Origin always worked best on Firefox.

**Tags**: `#Chrome`, `#Manifest V3`, `#Ad Blocking`, `#Privacy`, `#Extensions`

---

<a id="item-2"></a>
## [Turning Security Cameras into an Automatic Bird Identification System](https://jasontucker.blog/how-i-turned-my-security-cameras-into-an-automatic-bird-identification-system-with-birdnet-go/) ⭐️ 7.0/10

Jason Tucker describes using BirdNet-Go with existing security cameras to automatically detect and identify bird species by their calls. The project turns a home surveillance setup into a real-time bird monitoring station. This DIY project demonstrates how commodity hardware and open-source AI \(BirdNET\) can be repurposed for citizen science and biodiversity observation. It sparked a popular community discussion with 93 comments, showing strong interest in low-cost acoustic monitoring. BirdNet-Go ingests audio from soundcard inputs or network audio streams \(e.g., RTSP\), runs multi-model classification, and displays detections in a web UI. One commenter noted that BirdNET expects 48 kHz audio, which can be a limitation for cameras that only support 16 kHz.

hackernews · speckx · Aug 31, 16:47 · [Discussion](https://news.ycombinator.com/item?id=49511856)

**Background**: BirdNET is an AI-powered sound identification tool developed by Cornell University that recognizes over 6,000 bird species globally. BirdNet-Go is a self-hosted, real-time soundscape classifier that runs on devices like the Raspberry Pi. Security cameras with built-in microphones can provide continuous audio streams, making them a convenient input source for such systems.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/tphakala/birdnet-go">GitHub - tphakala/ birdnet - go : Self-hosted realtime soundscape...</a></li>
<li><a href="https://birdnet.cornell.edu/">BirdNET – AI-Powered Sound ID</a></li>

</ul>
</details>

**Discussion**: Commenters shared similar setups, such as using a Unifi doorbell cam with RTSP, or building a portable Birdnet-Pi for hiking. Some discussed technical issues like wind noise and audio sampling rate limits, while others suggested complementary apps like Merlin and small display enhancements. Overall, the sentiment was enthusiastic and collaborative, with users exchanging concrete improvements.

**Tags**: `#BirdNet`, `#DIY project`, `#machine learning`, `#security cameras`, `#birdwatching`

---

<a id="item-3"></a>
## [EU Tightens DSA Oversight on ChatGPT, Reddit, and Roblox](https://news.google.com/rss/articles/CBMiuwFBVV95cUxPM3dWNGxkTFhFQXVheUxlSllZLWdmNmJ1NHdQTGVPSkFNZWJzQ3VwenBYWUxZNm5XWE11WUlsWk0xTWFLd2ZWZDZBVWQ1blBsWUJoejQxMGJSV2l3cnhnZUpHdGg0SzhfdG1KSkd3dUYyR1RsZGV6N0lZWkgwN1F1bGJjNklNWUFSOG9kcnBrWjItVE5ZOXVwQVRqOEhmQXpHZUZxbEk3dGVnTnJXbnhLdmhsTG9hOEFCMWhn?oc=5) ⭐️ 7.0/10

The European Union has designated ChatGPT, Reddit, and Roblox as subject to stricter oversight under the Digital Services Act \(DSA\). The move brings these platforms under enhanced accountability and transparency obligations within the EU. This signals the EU&\#x27;s intent to apply DSA rules beyond conventional social networks to AI chatbots and gaming platforms. Affected companies must step up content moderation, risk management, and transparency reporting, and other tech firms may be next. Under the DSA&\#x27;s tiered system, stricter obligations are reserved for very large online platforms with more than 45 million monthly EU users. These obligations can include systemic risk assessments, external auditing, and data access for regulators and researchers.

rss · GoogleNews-欧盟监管 · Aug 31, 15:07

**Background**: The Digital Services Act is a comprehensive EU regulation that entered into force in 2022, setting accountability, content moderation, and transparency rules for digital services. It creates a tiered approach: basic obligations for all services, enhanced duties for online platforms, and the strictest requirements for very large online platforms \(VLOPs\) and search engines. The designation of ChatGPT, Reddit, and Roblox follows this framework.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act_Regulation">Digital Services Act Regulation</a></li>
<li><a href="https://zvelo.com/eu-regulations-attempt-to-tame-the-internet/">EU Regulations Attempt to Tame the Internet</a></li>

</ul>
</details>

**Tags**: `#EU`, `#Digital Services Act`, `#regulation`, `#AI`, `#platform governance`

---

<a id="item-4"></a>
## [Playa Phone Project: Hacker&\#x27;s Gift Connects Burning Man Community](https://playaphone.com/) ⭐️ 6.0/10

Reddit user aaron42net shared their Playa Phone project — a working pay phone at Burning Man that lets attendees call home for free — which quickly gained 495 points and 182 comments. The post prompted numerous personal stories and questions. This project demonstrates how a simple, functional piece of technology can create meaningful human connections in Burning Man&\#x27;s temporary city. It also highlights the event&\#x27;s culture of interactive art, gifting, and community, inspiring others to build similarly playful &\#x27;playa apps.&\#x27; The pay phone concept dates back to 2013, when the creator wanted to call home to a young child. The installation has been used by thousands of attendees, with lines forming during busy times, and the phone model echoes one used on the playa from 2004 to 2012.

hackernews · cutoff · Aug 31, 14:52 · [Discussion](https://news.ycombinator.com/item?id=49510514)

**Background**: Burning Man is an annual gathering in Nevada&\#x27;s Black Rock Desert where participants create a temporary city centered on self-expression, art, and gifting. &\#x27;Playa&\#x27; refers to the dry lake bed where the event takes place, and &\#x27;playa apps&\#x27; are community-built interactive projects found around the city. Because cell service is unreliable, pay phones like this offer a nostalgic and reliable way to reach the outside world.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sfgate.com/sf-culture/article/burning-man-pay-phone-19736797.php">&#x27;Talk to Mom&#x27;: Thousands of Burning Man attendees use this phone to call home</a></li>
<li><a href="https://burningman.org/black-rock-city/preparation/playa-apps/">Playa Apps – Burning Man Project</a></li>

</ul>
</details>

**Discussion**: Commenters shared personal stories, including an impromptu wedding triggered by the phone booth, and asked whether Burning Man is truly welcoming or dominated by the wealthy. One developer plugged a similar &\#x27;beacon&\#x27; app for spontaneous calls, while another reported the phone sometimes wouldn&\#x27;t call out. Overall, sentiment was warmly appreciative.

**Tags**: `#burning-man`, `#interactive-art`, `#community`, `#phone`, `#project`

---