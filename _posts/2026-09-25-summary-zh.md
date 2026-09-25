---
layout: default
title: "Horizon Summary: 2026-09-25 (ZH)"
date: 2026-09-25
lang: zh
---

> 从 12 条内容中筛选出 3 条重要资讯。

---

1. [F-Droid 2.0 发布：开源安卓应用商店迎来重大重设计](#item-1) ⭐️ 9.0/10
2. [Apple 在英国撤下高级数据保护，形成两级加密格局](#item-2) ⭐️ 8.0/10
3. [FTC 与 22 个州起诉亚马逊，指控其广告拍卖暗藏“软保留价”](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0 发布：开源安卓应用商店迎来重大重设计](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 9.0/10

F-Droid 于 2026 年 9 月 24 日发布 2.0 版本，对这款开源安卓应用仓库进行了大规模重设计与重构。此次更新重做了应用界面与软件仓库管理功能，并开始逐步淘汰 F-Droid Privileged Extension（FPE）。 F-Droid 是为数不多独立于 Google 的自由开源安卓应用分发渠道，因此一次大版本更新会直接影响大量注重隐私的用户安装与更新软件的方式。这次重设计又恰逢 Google 计划收紧安卓侧载与开发者验证机制之际，使得 F-Droid 的易用性与独立性变得格外关键。 此次重构重点改善了长期以来被用户诟病的仓库管理体验，并去掉了许多用户认为难以配置的特权系统扩展。不过，公告中的早期截图也招致批评，包括视觉层级薄弱、可点击区域提示不明确，以及诸如 &quot;Syncthing-For k&quot; 断行之类的文本排版错误。

hackernews · daveoc64 · 9月24日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49831968)

**背景**: F-Droid 是一个由社区运营的安卓应用目录与客户端，只收录自由开源软件，是 Google Play 的替代方案。它的客户端长期被认为界面陈旧、操作别扭，因此不少用户（尤其是在 GrapheneOS 等加固系统上）转用 Droid-ify 这类第三方前端。F-Droid Privileged Extension（FPE）是一个可选系统组件，在预装进 ROM 的设备上可让 F-Droid 静默安装和更新应用，但需要专门配置。而 Google 即将对侧载应用与开发者验证施加的限制，让人开始质疑独立应用仓库还能以现有方式运作多久。

**社区讨论**: 评论者普遍欢迎这次大改版以及 FPE 的淘汰，有人表示自己正是因为 F-Droid 的界面和特权扩展太难用才在 GrapheneOS 上改用 Droid-ify。也有人对新设计提出尖锐批评，认为其扁平低对比风格缺乏区块划分、点击目标不明确，宣传截图中的文字排版也相当粗糙。此外，不少人对明年 Google 实施安卓封锁之后 F-Droid 的前景表示担忧。

**标签**: `#F-Droid`, `#Android`, `#Open Source`, `#App Distribution`, `#UI/UX`

---

<a id="item-2"></a>
## [Apple 在英国撤下高级数据保护，形成两级加密格局](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

Apple 没有遵从一项要求其修改端到端加密底层安全架构的法律命令，而是选择在英国撤下 iCloud 的“高级数据保护”（ADP）功能。其结果是，英国用户在 iCloud 备份、照片、备忘录和 iCloud Drive 等类别中的数据退回“标准数据保护”模式，在该模式下 Apple 持有密钥并可依法回应法律请求。 此举把加密从一种全球统一的能力变成了取决于司法辖区的设置，实际上形成了英国用户保护弱于其他地区的“两级”体制。它还为各国政府如何在不直接强制厂商构建后门的情况下迫使其削弱安全性立下先例，并引发外界质疑：Apple 究竟会退让到何种程度才会选择退出某个市场。 Apple 指出，撤下 ADP 并未影响默认已端到端加密的 14 个 iCloud 类别（包括 iCloud 钥匙串和健康数据），而 ADP 会把这一总数从 14 个提高到 23 个；在英国，多出来的那些类别退回标准数据保护。该争议源于英国依据《调查权力法》发出的“技术能力通知”（TCN），而有评论者认为“14 个基础类别不受影响”这一说法并不严格成立，因为在常见使用场景下某些端到端加密的密钥材料仍可能被暴露。

hackernews · ReturnoftheHack · 9月24日 10:39 · [社区讨论](https://news.ycombinator.com/item?id=49828731)

**背景**: 高级数据保护（ADP）是一项可选的 iCloud 设置，可将端到端加密扩展到更多数据类型，意味着只有用户受信任的设备持有解密密钥，即使用户失去访问权限，Apple 自身也无法恢复数据。在标准设置下，Apple 为部分类别保留密钥，因而可以提供账户恢复协助并回应合法的法律请求。英国的《调查权力法》允许政府发出通知，强制企业构建或修改用于协助调查的技术能力，不过政府通常被禁止公开确认此类通知的存在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://macanorak.com/two-tier-encryption-in-the-uk/">Two-Tier Encryption in the UK - macanorak.com</a></li>
<li><a href="https://mjtsai.com/blog/2026/09/22/two-tier-encryption-in-the-uk/">Michael Tsai - Blog - Two-Tier Encryption in the UK</a></li>
<li><a href="https://mangodeveloper.com/articles/uk-users-now-split-into-two-encryption-tiers-after-apple-pulls-advanced-data-protection">UK Users Now Split Into Two Encryption Tiers After Apple ...</a></li>

</ul>
</details>

**社区讨论**: 评论整体持批评态度：有人认为 Apple 在 2015 年有勇气抵抗，如今却没有，并以 iPhone 设置过程中强制出现的年龄验证界面作为“口子一开就收不住”的证据；有人直言“两级加密”不过是换了个说法的后门；还有人希望 Apple 干脆彻底退出英国市场，而不是继续向英国政府供货。一位技术型评论者则反驳了“默认端到端加密的 14 个类别未受影响”的说法，认为英国用户的加密密钥材料在常见场景下仍可能被暴露。

**标签**: `#encryption`, `#privacy`, `#Apple`, `#UK policy`, `#security`

---

<a id="item-3"></a>
## [FTC 与 22 个州起诉亚马逊，指控其广告拍卖暗藏“软保留价”](https://www.reddit.com/r/ecommerce/comments/1wp0mkn/amazon_got_sued_for_lying_about_your_ad_auction/) ⭐️ 7.0/10

8 月 31 日，美国联邦贸易委员会（FTC）与 22 个州的总检察长对亚马逊提起诉讼，指控其自 2019 年起在广告拍卖中秘密加入“软保留价”——亚马逊内部文件将其描述为一个虚构的竞价参与者，把广告主的价格一路推高至其出价上限。起诉书引用的内部数据显示，按广告主最高出价全额扣费的 Sponsored Products 广告占比从 2021 年的 30%–40%，升至 2022 年的约 70%，到 2024 年已达约 80%。 该诉讼涉及超过 120 万名广告主，其中包括逾 50 万家中小商家，直指已成为亚马逊重要利润来源的广告业务的定价机制。若指控成立，亚马逊可能被迫改变其拍卖机制的设计与信息披露方式；此案也进一步推高了对占据主导地位的广告平台进行反垄断审查的浪潮。 起诉书涵盖 Sponsored Products、Sponsored Brands 和 Sponsored Display 等广告位，并指这一隐性加价使广告主的实际支付高于其对外宣称的拍卖机制本应产生的价格。由于广告主无法审计自己并不运营的拍卖，原帖提出一种粗略的排查方法：逐条对比各广告活动的平均 CPC 与最高出价——但真正竞争激烈的拍卖也会呈现类似现象，因此这只是线索而非证据。

reddit · r/ecommerce · /u/BaptisteNo · 9月24日 12:43

**背景**: 亚马逊的 Sponsored Products 是搜索结果中的按点击付费广告，历来采用第二价格拍卖（即维克里拍卖）：最高出价者胜出，但只需支付第二高出价加一分钱，这种设计意在鼓励竞价者报出自己真实的价值。而所谓的“软保留价”破坏了这一承诺，相当于插入一个类似底价的参与者，把胜出者的支付额推高到其自身的最高出价。FTC 与各州认为，这一未披露的改动抬高了整个平台的广告成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.affiversemedia.com/ftc-states-amazon-ad-auction-pricing-lawsuit/">FTC and 22 States Sue Amazon Over Ad Auctions</a></li>
<li><a href="https://openclassactions.com/news/ftc-amazon-ad-surcharge-lawsuit.php">FTC Sues Amazon Over Hidden Ad Auction Surcharges</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vickrey_auction">Vickrey auction - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Amazon`, `#FTC`, `#antitrust`, `#ad auctions`, `#ecommerce`

---