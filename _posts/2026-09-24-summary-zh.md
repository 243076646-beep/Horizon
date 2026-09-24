---
layout: default
title: "Horizon Summary: 2026-09-24 (ZH)"
date: 2026-09-24
lang: zh
---

> 从 18 条内容中筛选出 3 条重要资讯。

---

1. [Claude 自主发现类 CRISPR 重复序列系统，引发争议](#item-1) ⭐️ 8.0/10
2. [修复波托贝洛警察局的塔钟](#item-2) ⭐️ 6.0/10
3. [IAPP 称欧盟《人工智能法案》素养条款调整或令合规更复杂](#item-3) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude 自主发现类 CRISPR 重复序列系统，引发争议](https://www.anthropic.com/news/claude-discovers-novel-enzyme-system) ⭐️ 8.0/10

Anthropic 宣布，其 Claude 模型以自主智能体的方式扫描原始 DNA 序列数据，发现了一个此前未被描述的酶系统——其核心是一个反转录酶，两侧带有类 CRISPR 的串联重复序列阵列。据 Anthropic 称，该智能体只收到一个高层次的提示，其余分析全部自行完成，其运行记录中还出现了类似“反转录酶旁边的 DNA 有一个肉眼可见的串联重复阵列”的惊叹。 这一说法被视为“AI 用于科学”的一个里程碑：推动真正基因组发现的不是人类研究者，而是一个 LLM 智能体，它直接从未加工的序列数据中得出结论。如果这类智能体驱动的发现能够站得住脚，就意味着未来 AI 可以自主提出假设并挖掘公共序列数据库；但这次事件同样说明，炒作很容易跑在实际发现前面。 批评者指出，这次发现的核心其实是一种已知的类逆转录子（retron）反转录酶，因此更审慎的表述应是：Claude 识别出了一个围绕已知酶的新型基因组排列，而不是一个全新的酶系统。此外，重复区域仍需仔细验证，因为低复杂度的串联重复序列在历史上常被误判为 CRISPR 元件；而运行记录中的引语来自智能体自身的推理，而非独立的实验验证。

hackernews · raahelb · 9月23日 18:06 · [社区讨论](https://news.ycombinator.com/item?id=49820134)

**背景**: CRISPR 系统是一类基因组位点，由成簇的、规律间隔的短回文重复序列组成，在自然界中帮助细菌记录曾经感染过它们的病毒信息，科学家则借助 Cas9 核酸酶把它改造成了基因编辑工具。反转录酶是一种能把 RNA 逆向转录为 DNA 的酶，而逆转录子（retron）是细菌中把这类酶与一段小的非编码 RNA 配对在一起的元件。串联重复序列是指一小段 DNA 序列连续重复多次的区域；由于复杂度低，外观相似的结构有时会被误认成 CRISPR 位点。LLM 智能体则是以大语言模型作为控制中枢的 AI 系统，结合规划、记忆与工具调用能力来完成扫描序列数据库等多步骤任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CRISPR_gene_editing">CRISPR gene editing - Wikipedia</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC5294841/">Not all predicted CRISPR–Cas systems are equal - PMC - NIH</a></li>
<li><a href="https://www.promptingguide.ai/research/llm-agents">LLM Agents - Prompt Engineering Guide</a></li>

</ul>
</details>

**社区讨论**: 讨论区整体分成“兴奋”与“怀疑”两派。一些评论者认为应谨慎表述为：围绕已知类逆转录子反转录酶的一个此前未被描述的基因组排列，并指出治疗性基因编辑的主要瓶颈是递送而非核酸酶本身；另一些人则乐于把智能体的运行记录引语当成一种新的科学记录来重读；还有少数人对 Anthropic 对这些智能体实际能力的包装提出质疑，而最阴暗的回复则在拿人造病毒或 AI 引发灾难开玩笑。

**标签**: `#AI for science`, `#CRISPR`, `#genomics`, `#Anthropic`, `#LLM agents`

---

<a id="item-2"></a>
## [修复波托贝洛警察局的塔钟](https://pointinthecloud.com/2026-04-11-211700.html) ⭐️ 6.0/10

一位博主发表了一篇详细的第一手记录，讲述了他修复和维护波托贝洛警察局机械钟的过程，记录了爬上钟楼、查看机芯状况以及所执行的维护工作。这篇文章登上了 Hacker News 首页，获得了 378 个赞和 85 条评论。 这个故事之所以引起共鸣，是因为它展现了维持老旧公共基础设施运转的那种不起眼却需要亲力亲为的手艺——这类维护工作容易被忽视，但一旦失效，替换成本却很高。它也凸显出遗产钟表机械所依赖的、愿意且有能力爬进钟楼维护机芯的人正越来越少。 这篇记录涉及一些实际的维护问题，例如通往钟楼的木质梯子和台阶的状况，以及电路上很可能作为备用电源的一块电池。评论者指出，这类备用电池可能能用几十年，但也可能已经接近寿命终点；同时如果市电供应稳定，备用电池失效一时也不会造成影响。

hackernews · avidly · 9月23日 15:18 · [社区讨论](https://news.ycombinator.com/item?id=49817469)

**背景**: 塔钟（turret clock）是安装在塔楼中的机械钟，一个或多个钟面由下方机芯伸出的传动轴驱动。这类机芯使用擒纵机构——通常是调节钟摆的锚形擒纵器——把重锤（或发条）持续的拉力转化为规律的滴答走时。由于塔钟长期暴露在灰尘和温差之中且鲜有人照看，其修复工作包括拆解、清洁和修理齿轮及其他内部零件，就像维护历史上的街头钟或塔钟一样。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Turret_clock">Turret clock - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Escapement">Escapement - Wikipedia</a></li>
<li><a href="https://americlock.com/restoration-repair/">Clock Restoration &amp; Repair - Americlock</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一致给予好评，有人称这正是“我希望互联网成为的样子”，还有一位本地读者提到自己的父亲曾在那所警察局工作。实用建议包括在木质梯子踏板上加装自粘防滑贴以提高安全性，以及用一台低成本的 PoE 网络摄像头对准齿轮机构进行廉价远程监控；还有人分享了备用电池用了二十年后失效，以及旧教堂阁楼的灰尘触发机场安检检测的趣闻。

**标签**: `#hardware`, `#clockwork`, `#restoration`, `#maintenance`, `#hacker-news`

---

<a id="item-3"></a>
## [IAPP 称欧盟《人工智能法案》素养条款调整或令合规更复杂](https://news.google.com/rss/articles/CBMimwFBVV95cUxNaUdhdFpUSFRScktuVjJNUk9PaTVTRTBKYmdGNDFBUzNIMVgweXJUeEMyLVBrd1dQM0tjQy0xZ2s0Rm5KVEVuaEl4YUcxd1g5MlRLUFZENjlyUWdpYlhIa2FaRmlzYUluVGVmUkZ6UVg5NXVIbVVLT1BqXzBIOXVhVFpxeC12NXRsVkEtLTRDclIxZXQtdk8tZDRCTQ?oc=5) ⭐️ 6.0/10

国际隐私专业人员协会（IAPP）指出，欧盟《人工智能法案》中人工智能素养（AI literacy）要求的最新调整，可能让企业的合规工作变得更困难，而非更简单。该分析认为，修改后的措辞带来了新的解释上的模糊空间，而不是企业所期待的简化。 《人工智能法案》第 4 条规定的 AI 素养义务广泛适用于 AI 系统的提供者和部署者，因此任何模糊之处都会直接影响成千上万家企业如何设计员工培训并留存合规证据。由于该要求已于 2025 年 2 月生效，许多机构已经开始依据可能仍会变化的表述做出实际运营决策，从而提高了返工成本的风险。 第 4 条要求提供者和部署者确保代表其操作 AI 系统的人员具备足够的 AI 素养，并需结合其技术知识、培训情况和使用场景来判断——但该条款并未规定具体的认证或课程大纲。正是这种开放式、以结果为导向的表述方式，使得最新修订难以转化为具体且可审计的合规步骤；在未履行素养义务的情况下，可能面临处罚。

rss · GoogleNews-欧盟监管 · 9月23日 16:02

**背景**: 欧盟《人工智能法案》是欧盟针对人工智能的综合性法规，其各项义务是分阶段推行的。AI 素养由第 4 条规范，是最早适用的一批义务之一，自 2025 年 2 月起对 AI 系统的提供者和部署者生效。与法案中许多聚焦高风险系统和合规性评估的其他部分不同，第 4 条针对的是 AI 使用中“人”的一面——确保员工了解 AI 基础知识并负责任地使用这些工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sectionai.com/blog/passing-the-eu-ai-literacy-requirements">Passing the EU ’s AI Literacy Requirements</a></li>
<li><a href="https://threatcop.com/blog/eu-ai-act-ai-literacy/?trk=article-ssr-frontend-pulse_little-text-block">EU AI Act AI Literacy : What Article 4 Requires Now</a></li>
<li><a href="https://www.axonpark.com/ai-literacy-requirements-eu-ai-act">AI Literacy Training for EU AI Act | Axon Park | Axon Park</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI regulation`, `#compliance`, `#AI literacy`, `#policy`

---