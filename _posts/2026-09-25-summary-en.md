---
layout: default
title: "Horizon Summary: 2026-09-25 (EN)"
date: 2026-09-25
lang: en
---

> From 12 items, 3 important content pieces were selected

---

1. [F-Droid 2.0 Launches Major Redesign of the Open-Source Android App Store](#item-1) ⭐️ 9.0/10
2. [Apple Pulls Advanced Data Protection in the UK, Creating Two Encryption Tiers](#item-2) ⭐️ 8.0/10
3. [FTC and 22 States Sue Amazon Over Secret Ad Auction &\#x27;Soft Reserve Price&\#x27;](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0 Launches Major Redesign of the Open-Source Android App Store](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 9.0/10

F-Droid announced version 2.0 on September 24, 2026, a major redesign and overhaul of the open-source Android app repository. The release reworks the app&\#x27;s user interface and repository management, and begins phasing out the F-Droid Privileged Extension \(FPE\). F-Droid is one of the few independent, non-Google channels for distributing free and open-source Android apps, so a major revision shapes how a large privacy-conscious user base installs and updates software. The redesign also lands just as Google&\#x27;s planned tightening of Android sideloading and developer verification looms, making F-Droid&\#x27;s usability and independence more consequential than usual. The overhaul focuses on smoother repository management — long a pain point for users — and removes the need for the privileged system extension that many found difficult to configure. Early screenshots shown in the announcement drew criticism for weak visual hierarchy, unclear tap affordances, and text-wrapping glitches such as &quot;Syncthing-For k&quot; breaking across lines.

hackernews · daveoc64 · Sep 24, 15:26 · [Discussion](https://news.ycombinator.com/item?id=49831968)

**Background**: F-Droid is a community-run catalog and client for Android that hosts only free and open-source software, offering an alternative to Google Play. Historically its client was seen as dated and awkward compared to third-party front-ends such as Droid-ify, which many users on hardened systems like GrapheneOS adopted instead. The F-Droid Privileged Extension \(FPE\) was an optional system component that let F-Droid install and update apps silently on devices where it was built into the ROM, but it required special configuration. Google&\#x27;s forthcoming restrictions on sideloaded apps and developer verification have raised broader questions about how long independent repositories can operate as they do today.

**Discussion**: Commenters welcomed the overhaul and the phase-out of FPE, with one noting they had switched to Droid-ify on GrapheneOS precisely because F-Droid&\#x27;s UI and privileged extension were so painful. Others were sharply critical of the new design&\#x27;s flat, low-contrast style, complaining about the lack of visual separation between sections, unclear tap targets, and sloppy text layout in the marketing screenshots. A recurring worry was what F-Droid&\#x27;s future looks like once Google enacts its Android lockdown next year.

**Tags**: `#F-Droid`, `#Android`, `#Open Source`, `#App Distribution`, `#UI/UX`

---

<a id="item-2"></a>
## [Apple Pulls Advanced Data Protection in the UK, Creating Two Encryption Tiers](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

Apple has withdrawn Advanced Data Protection \(ADP\) for iCloud in the United Kingdom rather than comply with a legal order that would have required it to alter the security architecture underpinning end-to-end encryption. As a result, UK users&\#x27; iCloud data in categories such as Backup, Photos, Notes and iCloud Drive falls back to Standard Data Protection, where Apple holds the keys and can respond to lawful legal process. The move turns encryption from a uniform global property into a jurisdiction-dependent setting, effectively creating a two-tier regime where UK users get weaker protection than everyone else. It also sets a precedent for how governments can pressure platform providers into weakening security without technically forcing them to build a backdoor, and raises questions about how far Apple will go before exiting a market. Apple notes that withdrawing ADP did not touch the 14 iCloud categories already end-to-end encrypted by default, including iCloud Keychain and Health, whereas ADP raises the total from 14 to 23 categories; the extra categories revert to Standard Data Protection in the UK. The dispute stems from a Technical Capability Notice \(TCN\) issued under the UK&\#x27;s Investigatory Powers Act, and commenters argue the claim that the 14 baseline categories are unaffected is not strictly accurate because some end-to-end encrypted secrets are exposed in common usage scenarios.

hackernews · ReturnoftheHack · Sep 24, 10:39 · [Discussion](https://news.ycombinator.com/item?id=49828731)

**Background**: Advanced Data Protection is an optional iCloud setting that extends end-to-end encryption to more data types, meaning only the user&\#x27;s trusted devices hold the decryption keys and Apple itself cannot recover the data if the user loses access. Under the standard setting, Apple retains keys for some categories so it can help with account recovery and respond to valid legal requests. The UK&\#x27;s Investigatory Powers Act allows the government to issue notices compelling a company to build or modify capabilities to assist investigations, though the government is generally barred from publicly confirming such notices exist.

<details><summary>References</summary>
<ul>
<li><a href="https://macanorak.com/two-tier-encryption-in-the-uk/">Two-Tier Encryption in the UK - macanorak.com</a></li>
<li><a href="https://mjtsai.com/blog/2026/09/22/two-tier-encryption-in-the-uk/">Michael Tsai - Blog - Two-Tier Encryption in the UK</a></li>
<li><a href="https://mangodeveloper.com/articles/uk-users-now-split-into-two-encryption-tiers-after-apple-pulls-advanced-data-protection">UK Users Now Split Into Two Encryption Tiers After Apple ...</a></li>

</ul>
</details>

**Discussion**: Commenters are largely critical: one argues Apple had the courage to resist in 2015 but not today, citing mandatory age-verification screens during iPhone setup as evidence of a slippery slope, another says &quot;two-tier encryption&quot; sounds like a backdoor with extra steps, and a third hopes Apple would pull out of the UK market entirely rather than keep selling to the UK government. A more technical commenter pushes back on the claim that the 14 default end-to-end encrypted categories were unaffected, arguing UK users&\#x27; encrypted secrets can still be exposed in common scenarios.

**Tags**: `#encryption`, `#privacy`, `#Apple`, `#UK policy`, `#security`

---

<a id="item-3"></a>
## [FTC and 22 States Sue Amazon Over Secret Ad Auction &\#x27;Soft Reserve Price&\#x27;](https://www.reddit.com/r/ecommerce/comments/1wp0mkn/amazon_got_sued_for_lying_about_your_ad_auction/) ⭐️ 7.0/10

On August 31, the FTC and 22 state attorneys general sued Amazon, alleging that since 2019 it secretly added a &quot;soft reserve price&quot; to its ad auctions — described in Amazon&\#x27;s own internal documents as an invented auction participant that pushes advertisers up toward their maximum bid. The complaint cites internal figures showing the share of Sponsored Products ads that charged the advertiser their full bid climbed from 30–40% in 2021 to about 70% in 2022 and roughly 80% by 2024. The lawsuit covers more than 1.2 million advertisers, including over 500,000 small and medium-sized businesses, and attacks the pricing mechanics of an advertising business that has become a major profit driver for Amazon. If the allegations hold up, Amazon could be forced to change how its auctions are designed and disclosed, and the case adds to the broader wave of antitrust scrutiny of dominant ad platforms. The complaint covers Sponsored Products, Sponsored Brands and Sponsored Display placements, and alleges the hidden surcharge raised what advertisers paid above what the advertised auction format should have produced. Because advertisers cannot audit an auction they do not run, the post suggests a rough diagnostic: compare average CPC against max bid campaign by campaign — though a genuinely tight auction can produce the same pattern, so it is a lead, not proof.

reddit · r/ecommerce · /u/BaptisteNo · Sep 24, 12:43

**Background**: Amazon&\#x27;s Sponsored Products ads are pay-per-click placements in search results, historically sold through a second-price \(Vickrey\) auction: the highest bidder wins but pays only the second-highest bid plus a cent, a design meant to encourage bidders to bid their true value. The alleged &quot;soft reserve price&quot; breaks that promise by inserting a floor-like participant that can push the winner&\#x27;s payment up to their own maximum bid. The FTC and states argue this undisclosed change inflated ad costs across the marketplace.

<details><summary>References</summary>
<ul>
<li><a href="https://www.affiversemedia.com/ftc-states-amazon-ad-auction-pricing-lawsuit/">FTC and 22 States Sue Amazon Over Ad Auctions</a></li>
<li><a href="https://openclassactions.com/news/ftc-amazon-ad-surcharge-lawsuit.php">FTC Sues Amazon Over Hidden Ad Auction Surcharges</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vickrey_auction">Vickrey auction - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Amazon`, `#FTC`, `#antitrust`, `#ad auctions`, `#ecommerce`

---