---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 13 条内容中筛选出 4 条重要资讯。

---

1. [谷歌从 Chrome 网上应用店移除 MV2 扩展，含 uBlock Origin](#item-1) ⭐️ 8.0/10
2. [把安防摄像头变成自动鸟类识别系统](#item-2) ⭐️ 7.0/10
3. [欧盟依据《数字服务法》加强对 ChatGPT、Reddit、Roblox 的监管](#item-3) ⭐️ 7.0/10
4. [Playa Phone 项目：黑客的礼物连接 Burning Man 社区](#item-4) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [谷歌从 Chrome 网上应用店移除 MV2 扩展，含 uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

谷歌已正式从 Chrome 网上应用店移除 Manifest V2（MV2）扩展，其中包括广受欢迎的广告拦截器 uBlock Origin。这是其向更严格的 Manifest V3（MV3）框架过渡的一部分，这一框架限制了扩展功能。 这一变动影响了数百万依赖 uBlock Origin 进行有效广告拦截和抵御恶意广告的用户。同时，它也引发了对谷歌对网络控制权和广告拦截扩展未来的担忧，促使部分用户转向 Firefox 等替代浏览器。 uBlock Origin 过去使用 webRequest API 实时拦截网络请求，而这一能力在 Manifest V3 中受到大幅限制。虽然存在 MV3 版本的 uBlock Origin Lite，但其功能较弱；用户仍可手动安装 MV2 扩展，或切换到仍完全支持 uBlock Origin 的 Firefox。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Manifest V2 是一种较旧的扩展 API 标准，允许 uBlock Origin 等扩展在网页加载前拦截并阻止网络请求。2021 年，谷歌宣布转向 Manifest V3，声称能提升安全性和性能，但电子前沿基金会等批评者认为这会削弱隐私保护工具并阻碍创新。uBlock Origin 是一款免费开源的内容过滤扩展，拥有数千万用户，是 Chrome 和 Firefox 上最受欢迎的扩展之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eff.org/deeplinks/2021/12/googles-manifest-v3-still-hurts-privacy-security-innovation">Google’s Manifest V 3 Still Hurts Privacy, Security, and Innovation</a></li>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">UBlock Origin</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>

</ul>
</details>

**社区讨论**: 社区反应普遍负面，许多用户呼吁转向 Firefox。评论者指出，广告拦截对易受骗的用户已成为一种安全必需，批评谷歌对网络的单方面控制，并提到 uBlock Origin 在 Firefox 上始终表现最好。

**标签**: `#Chrome`, `#Manifest V3`, `#Ad Blocking`, `#Privacy`, `#Extensions`

---

<a id="item-2"></a>
## [把安防摄像头变成自动鸟类识别系统](https://jasontucker.blog/how-i-turned-my-security-cameras-into-an-automatic-bird-identification-system-with-birdnet-go/) ⭐️ 7.0/10

Jason Tucker 介绍了如何利用 BirdNet-Go 与已有的安防摄像头，通过鸣声自动检测并识别鸟类。这个项目将家庭监控设备变成了实时鸟类监测站。 这个 DIY 项目展示了如何将商用硬件和开源 AI（BirdNET）重新用于公民科学与生物多样性观察。它引发了 93 条评论的热烈社区讨论，表明人们对低成本声音监测有浓厚兴趣。 BirdNet-Go 从声卡输入或网络音频流（例如 RTSP）获取音频，运行多模型分类，并在 Web 界面中显示检测结果。一位评论者指出 BirdNET 需要 48 kHz 音频，这对仅支持 16 kHz 的摄像头是一个限制。

hackernews · speckx · 8月31日 16:47 · [社区讨论](https://news.ycombinator.com/item?id=49511856)

**背景**: BirdNET 是康奈尔大学开发的基于 AI 的声音识别工具，可识别全球超过 6,000 种鸟类。BirdNet-Go 是一个自托管的实时声景分类器，可运行在树莓派等设备上。带有内置麦克风的安防摄像头可以提供连续音频流，因此很适合作为这类系统的输入源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tphakala/birdnet-go">GitHub - tphakala/ birdnet - go : Self-hosted realtime soundscape...</a></li>
<li><a href="https://birdnet.cornell.edu/">BirdNET – AI-Powered Sound ID</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了类似设置，例如使用支持 RTSP 的 UniFi 门铃摄像头，或构建便携式 Birdnet-Pi 用于徒步旅行。一些人讨论了技术问题，如风噪和音频采样率限制，还有人推荐了如 Merlin 等辅助应用及小型显示增强。总体氛围热情且乐于协作，用户们交流了具体的改进方案。

**标签**: `#BirdNet`, `#DIY project`, `#machine learning`, `#security cameras`, `#birdwatching`

---

<a id="item-3"></a>
## [欧盟依据《数字服务法》加强对 ChatGPT、Reddit、Roblox 的监管](https://news.google.com/rss/articles/CBMiuwFBVV95cUxPM3dWNGxkTFhFQXVheUxlSllZLWdmNmJ1NHdQTGVPSkFNZWJzQ3VwenBYWUxZNm5XWE11WUlsWk0xTWFLd2ZWZDZBVWQ1blBsWUJoejQxMGJSV2l3cnhnZUpHdGg0SzhfdG1KSkd3dUYyR1RsZGV6N0lZWkgwN1F1bGJjNklNWUFSOG9kcnBrWjItVE5ZOXVwQVRqOEhmQXpHZUZxbEk3dGVnTnJXbnhLdmhsTG9hOEFCMWhn?oc=5) ⭐️ 7.0/10

欧盟已将对 ChatGPT、Reddit 和 Roblox 的监管纳入《数字服务法》（DSA）框架下更严格的监督范围。此举使这些平台在欧盟内承担更高的问责与透明度义务。 这表明欧盟有意将《数字服务法》的规则从传统社交网络扩展到 AI 聊天机器人和游戏平台。受影响的公司必须加强内容审核、风险管理和透明度报告，其他科技公司也可能紧随其后。 根据《数字服务法》的分级制度，更严格的义务适用于月活欧盟用户超过 4500 万的超大型在线平台。这些义务可包括系统性风险评估、外部审计，以及向监管机构和研究人员提供数据访问权限。

rss · GoogleNews-欧盟监管 · 8月31日 15:07

**背景**: 《数字服务法》是欧盟于 2022 年生效的一部综合性法规，为数字服务制定了问责、内容审核和透明度规则。它采用分级治理：所有服务承担基本义务，在线平台承担更高要求，而超大型在线平台（VLOPs）和搜索引擎则面临最严格的规定。ChatGPT、Reddit 和 Roblox 此次被指定正是基于该框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Services_Act_Regulation">Digital Services Act Regulation</a></li>
<li><a href="https://zvelo.com/eu-regulations-attempt-to-tame-the-internet/">EU Regulations Attempt to Tame the Internet</a></li>

</ul>
</details>

**标签**: `#EU`, `#Digital Services Act`, `#regulation`, `#AI`, `#platform governance`

---

<a id="item-4"></a>
## [Playa Phone 项目：黑客的礼物连接 Burning Man 社区](https://playaphone.com/) ⭐️ 6.0/10

Reddit 用户 aaron42net 分享了他的 Playa Phone 项目——一部安装在 Burning Man 上、可让参与者免费打电话回家的公用电话——这篇帖子迅速获得 495 分和 182 条评论，引发了大量个人故事和提问。 这个项目表明，一件简单而实用的技术作品能在 Burning Man 的临时城市中创造有意义的联结。它也凸显了这场活动所倡导的互动艺术、礼物文化和社区精神，激励他人打造类似好玩的“playa apps”。 这个公用电话的想法源于 2013 年，当时创建者想给家里年幼的孩子打电话。该装置已被数以千计的参与者使用，高峰期还会排队；其电话机型与 2004 年至 2012 年间出现在 playa 上的一部电话型号相同。

hackernews · cutoff · 8月31日 14:52 · [社区讨论](https://news.ycombinator.com/item?id=49510514)

**背景**: Burning Man 是每年在美国内华达州黑岩沙漠举办的大型聚会，参与者会建造一个以自我表达、艺术和礼物文化为核心的临时城市。“Playa”指的是活动场地的干涸湖床，而“playa apps”是遍布城市中的社区互动项目。由于手机信号不稳定，这样的公用电话提供了一种怀旧而可靠的与外界联系的方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sfgate.com/sf-culture/article/burning-man-pay-phone-19736797.php">&#x27;Talk to Mom&#x27;: Thousands of Burning Man attendees use this phone to call home</a></li>
<li><a href="https://burningman.org/black-rock-city/preparation/playa-apps/">Playa Apps – Burning Man Project</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了个人故事，包括一个因电话亭而引发的即兴婚礼，并询问 Burning Man 是否真的包容，还是被富人主导。一位开发者借机推广了类似的“beacon”应用来恢复随性通话，另有人提到电话有时无法拨出。总体而言，大家的态度是热情而感激的。

**标签**: `#burning-man`, `#interactive-art`, `#community`, `#phone`, `#project`

---