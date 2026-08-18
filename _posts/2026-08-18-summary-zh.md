---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 18 条内容中筛选出 6 条重要资讯。

---

1. [用 20 美元工具救活变砖的 Framework 13 笔记本电脑](#item-1) ⭐️ 8.0/10
2. [Linux 7.3 提升显存耗尽时的性能](#item-2) ⭐️ 8.0/10
3. [Seth Godin：亚马逊广告泛滥的搜索正在向用户征收“税”](#item-3) ⭐️ 7.0/10
4. [把铁路网变成巨型平板扫描仪](#item-4) ⭐️ 7.0/10
5. [冰岛食品的黑色幽默：小心管理顾问](#item-5) ⭐️ 6.0/10
6. [欧盟 AI 训练数据披露要求进入执法阶段](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [用 20 美元工具救活变砖的 Framework 13 笔记本电脑](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

一篇新的维修指南详细介绍了如何使用约 20 美元的工具救活一台因 BIOS 更新失败而变砖的 Framework 13 AMD（7040 系列）笔记本电脑。该文章发布于 2026 年 8 月 16 日，一步一步记录了完整的救砖过程。 BIOS 更新失败经常让原本完好的笔记本电脑沦为看似只能报废的电子垃圾，因此一条廉价且有据可查的修复路径对用户和更广泛的“维修权”运动都意义重大。这篇指南也让一个争论变得更加尖锐：当厂商自己的固件更新损坏硬件时，厂商是否应承担法律或保修责任。 修复过程采用标准的 SPI 闪存恢复方法：打开笔记本电脑，断开包括 CMOS 电池在内的所有电源，用线夹夹住 BIOS 芯片，再通过 CH341A USB 编程器在另一台电脑上重写固件。编程器和线夹的总成本约为 20 美元，但能否成功取决于线夹型号是否正确以及固件是否与主板完全匹配。

hackernews · jp\_sc · 8月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49345220)

**背景**: “变砖”（bricked）的设备指的是因固件损坏或更新中断而完全无法使用、像砖头一样毫无用处的设备。BIOS（或 UEFI）是操作系统加载前初始化硬件的底层固件，一旦损坏，电脑可能完全无法开机。恢复通常需要借助外部编程器对固件芯片进行物理重刷，这项技术过去需要专业设备，如今用 CH341A 这类廉价工具就能实现。官方 BIOS 更新导致笔记本电脑变砖的情况依然频繁发生，这正是这篇指南及其引发的讨论能引起共鸣的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Brick_%28electronics%29">Brick (electronics) - Wikipedia</a></li>
<li><a href="https://jpdias.me/hardware/msi/bios/2020/05/10/back-from-the-dead.html">Back from the Dead: Recovering from a Bricked BIOS</a></li>
<li><a href="https://www.laboneinside.com/ch341a-usb-programmer/">CH341A USB Programmer For Sale | Lab-One</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对作者表示同情，并把这件事变成对厂商的批评：有人认为官方固件更新导致设备变砖应产生法律责任，甚至建议通过小额索赔法院解决；另一个人分享了 ThinkPad Nano 的类似遭遇，称 BIOS 变砖仍然“极其常见”。还有人把争论延伸到保修政策，坚持认为安装官方更新应延长保修期；一位 Framework 用户则表达了对该平台的后悔，因为备件只能从 Framework 官方购买，而且经常缺货。

**标签**: `#hardware`, `#BIOS`, `#repair`, `#framework-laptop`, `#consumer-rights`

---

<a id="item-2"></a>
## [Linux 7.3 提升显存耗尽时的性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

即将推出的 Linux 7.3 内核包含在 GPU 显存耗尽时提升性能的改进，可减少卡顿与降速。这些改动聚焦于更优的过量分配处理和将 GPU 缓冲区换出到系统内存的策略。 这很重要，因为显存耗尽通常是游戏和 GPU 计算工作负载的常见瓶颈，经常导致严重掉帧或应用程序崩溃。更好的处理方式能让显存有限的 GPU 更实用，并降低对高显存型号的依赖。 根据社区讨论，内核无法完美获知最佳内存位置，因此文章建议应用程序应能提示显存的“粘性”。Nvidia 显卡目前完全不支持显存分页，因此这些改进可能首先使 AMD 和 Intel 核显/独显受益。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: 在 Linux 内核中，GPU 内存管理由 DRM 驱动程序通过 TTM（Translation Table Maps）和 drm\_mm 分配器等子系统处理。当显存满了之后，内核必须将缓冲对象换出到系统内存，这会造成性能损失。异构内存管理（HMM）等创新技术允许在 CPU 和 GPU 之间更好地共享和迁移内存。这项工作的目标就是让过量分配路径更高效。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kernel.org/doc/html/v4.14/gpu/drm-mm.html">DRM Memory Management — The Linux Kernel documentation</a></li>
<li><a href="https://www.kernel.org/doc/html/v5.0/vm/hmm.html">Heterogeneous Memory Management (HMM) — The Linux Kernel documentation</a></li>
<li><a href="https://www.xda-developers.com/used-my-nvidia-gpus-vram-as-system-swap-freed-me-from-buying-more-memory/">I used my Nvidia GPU&#x27;s VRAM as system swap , and it freed me from...</a></li>

</ul>
</details>

**社区讨论**: 评论者对该更新很兴奋，有人说“已经等不及 7.3 了”。还有人希望 Linux 中内存压力相关的行为（如内存占满时系统冻结）也能得到修复。一位 Nvidia 用户指出其硬件不支持任何形式的显存分页，其他人则称赞内核开发社区。

**标签**: `#Linux`, `#kernel`, `#VRAM`, `#memory management`, `#performance`

---

<a id="item-3"></a>
## [Seth Godin：亚马逊广告泛滥的搜索正在向用户征收“税”](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 7.0/10

在 2026 年 8 月一篇题为《The Amazon tax》的博文中，Seth Godin 指出，亚马逊的搜索结果如今优先展示赞助广告和平台自身的商业利益，而非用户的真实意图，实际上是在对消费者的注意力和信任征税。这篇文章引发了关于亚马逊搜索质量下降的广泛讨论。 亚马逊是全球最大的购物平台之一，其排序和展示产品的方式变化会影响数百万买家和卖家。这一批评揭示了一个更广泛的行业趋势：平台将搜索意图变现，削弱用户信任，并可能促使消费者转向其他电商平台。 Godin 将这一现象称为一种“税”，但消费者付出的不是金钱，而是注意力、信任和浪费的时间。评论区有用户反映，亚马逊搜索结果中大约四分之三是赞助广告，即使消费者清楚自己想要的商品，广告的相关性也常常很差。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊的产品搜索主要依靠 A9 算法，该算法会根据销售历史、相关性、评论和价格等信号对自然搜索结果进行排序。除了自然列表，亚马逊还通过类似拍卖的竞价系统出售赞助产品广告位，使付费广告与自然结果混排在一起。这种付费与自然内容混合的机制意味着用户看到的结果同时受到广告主预算和算法相关性的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://epinium.com/en/blog/amazon-a9-algorithm-2/">Amazon A 9 Algorithm Guide | Epinium</a></li>
<li><a href="https://www.channable.com/blog/amazon-sponsored-products">Amazon Sponsored Products ads: The complete guide</a></li>
<li><a href="https://advertising.amazon.co.uk/help/GCU2BUWJH2W3A8Z7">Bidding strategies for Sponsored Products | Amazon Ads Support...</a></li>

</ul>
</details>

**社区讨论**: 评论区普遍认同这一批评，许多用户提到多年来搜索质量不断下降，并将赞助广告形容为“广告雷区”。有人表示已将购买转向本地商店、Etsy 等平台，还有一位用户正在考虑注销使用了 15 年的亚马逊账户。少数不同观点认为广告有时也能带来相关的替代选择，但整体情绪是亚马逊更看重自身变现而非用户意图。

**标签**: `#Amazon`, `#e-commerce`, `#search quality`, `#advertising`, `#consumer experience`

---

<a id="item-4"></a>
## [把铁路网变成巨型平板扫描仪](https://philo.gay/linecam/) ⭐️ 7.0/10

「linecam」项目将铁路网络用作移动平台进行线扫描成像，把列车旅程变成对风景的连续扫描。它通过拼接列车移动时捕捉的窄条图像，生成绵延无缝的全景图。 这个创意黑客项目展示了日常基础设施如何变成艺术与技术工具，模糊了实用与艺术创作的界限。它还为人们提供了一种新颖且容易上手的方式来探索线扫描成像技术——这套原理也正是办公扫描仪和卫星影像的基础。 该项目采用了线扫描成像（又称推扫式扫描）技术：一维传感器借助相对运动来构建二维图像。由于列车提供了运动，图像沿轨道方向连续延展，每一列竖线都在不同的瞬间被捕捉。

hackernews · otherayden · 8月18日 12:43 · [社区讨论](https://news.ycombinator.com/item?id=49344825)

**背景**: 线扫描成像利用单排传感器像素，在物体或相机运动时将图像逐行构建成二维图像。推扫式扫描仪是该原理的一种常见应用，广泛用于复印机、文档扫描仪以及轨道卫星相机（如月球勘测轨道飞行器的 NAC 相机）。这个项目将同样的原理运用于铁路旅行，让任何人都能在列车窗口体验这门技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.teledynevisionsolutions.com/en-in/learn/learning-center/machine-vision/line-scan-primer/">Line Scan Primer | Teledyne Vision Solutions</a></li>
<li><a href="https://en.wikipedia.org/wiki/Push_broom_scanner">Push broom scanner</a></li>
<li><a href="https://www.vision-systems.com/factory/article/55266728/the-fundamentals-of-line-scan-imaging-part-1-what-it-is-and-when-to-use-it">Fundamentals of Line Scan Imaging , Part... | Vision Systems Design</a></li>

</ul>
</details>

**社区讨论**: 评论区分享了相关实验和历史轶事，包括 2008 年与 Ward Cunningham 用 iSight 摄像头做过的类似尝试，以及一个缝隙扫描网页小玩具。有人称赞这个项目鼓舞人心，称其拉伸了时间与空间，还有人讲述了自己独立发现类似技术的经历。

**标签**: `#creative-coding`, `#imaging`, `#railway`, `#hack`, `#line-scan`

---

<a id="item-5"></a>
## [冰岛食品的黑色幽默：小心管理顾问](https://about.iceland.co.uk/our-story/the-dark-ages/beware-management-consultants/) ⭐️ 6.0/10

冰岛食品公司在其官网上发布了一个故意做得很难用的幻灯片式页面，标题为《小心管理顾问》，以幽默方式讲述了与一家大型咨询公司合作的灾难性经历。这段内容被放在其品牌历史栏目“黑暗时代”之下，将该经历定性为一段公司倒退期。 这篇文章之所以引发广泛共鸣，是因为它尖锐地概括了许多组织和员工对昂贵却收效甚微的咨询项目的不满。它以幽默但犀利的笔触，为关于咨询行业动机与实效的长期争论提供了新素材，对科技和商业领域的读者尤具现实意义。 这个幻灯片页面刻意设计了糟糕的用户体验——字体极小、导航笨拙、必须逐页点击——这是一种有意的风格选择，用来模仿文中所描述的那种痛苦且官僚化的过程。这篇文章是冰岛食品公司历史系列故事的一部分，而“黑暗时代”这一表述暗示咨询项目那段时期被视为公司低谷，后来才逐渐恢复。

hackernews · KolmogorovComp · 8月18日 19:29 · [社区讨论](https://news.ycombinator.com/item?id=49351324)

**背景**: 冰岛食品公司是一家英国冷冻食品连锁超市，以其冷冻食品闻名。在其官网“我们的故事”栏目中，公司会以坦诚而幽默的方式回顾过去的失误，“黑暗时代”就是专门讲述一段决策失误时期的章节。管理顾问是指被企业聘请来改善绩效的外部专家，但批评者认为，他们的激励机制往往更偏向于多卖项目，而非真正解决客户问题，从而造成浪费和挫败感。

**社区讨论**: 评论区大多数网友很喜欢这篇讽刺文，不少人称赞刻意设计的糟糕用户体验是一种巧妙的做法，逼着读者放慢速度仔细阅读——有人表示它“防止了多动症式跳读”。也有人反思自己在公司治理和外包中的角色，承认站在“管理层”一边的尴尬；还有评论者质疑管理层为何迷恋咨询顾问，认为他们的激励并不一致，且公司常常过分强调改变。

**标签**: `#management-consulting`, `#corporate-culture`, `#satire`, `#business`, `#hacker-news`

---

<a id="item-6"></a>
## [欧盟 AI 训练数据披露要求进入执法阶段](https://news.google.com/rss/articles/CBMihAFBVV95cUxPelhzQ0ZSbTBnRnU1LWRiT2xCR3llSzlqNFZLa1pFLTBkOWJGZURRX09oZG56ZTAzMlUzZFBUSkdMLV9kS1lHUnRDSmhBV0dBakF0WGhUcFljdDFMRDRlNGFYR21ZZzR3S2JVTldSQWVTY1dJVVBfQ0JSX1lFQW5kZWRGVFI?oc=5) ⭐️ 6.0/10

欧盟委员会已发布强制模板，要求通用人工智能（GPAI）提供商根据《欧盟人工智能法案》第 53\(1\)\(d\)条公布其训练数据摘要，表明此前“低调”的要求现在进入执法阶段。合规义务正按分阶段时间表开始生效。 这一执法举措将人工智能透明度从自愿或模糊的披露转变为具有约束力的法律要求，影响所有面向欧盟市场的 GPAI 提供商。这可能会加强公众对训练数据来源的审查，并为其他考虑类似透明度规则的司法管辖区树立先例。 该模板由 AI 事务办公室发布，要求提供训练所用内容的“足够详细的摘要”，包括受版权保护的数据。《欧盟人工智能法案》分阶段实施，主要里程碑预计到 2028 年 8 月 2 日前全面适用，意味着义务是逐步落实的。

rss · GoogleNews-欧盟监管 · 8月18日 14:09

**背景**: 《欧盟人工智能法案》（即第\(EU\)2024/1689 号条例）引入了第 53\(1\)\(d\)条，要求通用人工智能模型提供商公布训练所用内容的摘要。许多提供商最初给出的摘要模糊或不完整。委员会现已发布标准化模板来执行这一透明度义务，并与该法案的分阶段实施时间表保持一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wilmerhale.com/en/insights/blogs/wilmerhale-privacy-and-cybersecurity-law/european-commission-releases-mandatory-template-for-public-disclosure-of-ai-training-data">European Commission Releases Mandatory Template for Public Disclosure of AI Training Data</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/faqs/template-general-purpose-ai-model-providers-summarise-their-training-content">Template for general-purpose AI model providers to summarise their training content | Shaping Europe’s digital future</a></li>
<li><a href="https://artificialintelligenceact.eu/implementation-timeline/">Implementation Timeline | EU Artificial Intelligence Act</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#EU`, `#compliance`, `#training data`

---