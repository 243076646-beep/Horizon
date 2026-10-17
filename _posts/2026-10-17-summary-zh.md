---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 17 条内容中筛选出 6 条重要资讯。

---

1. [Claude 揭开 NIST 椭圆曲线种子源自 lrand48 之谜](#item-1) ⭐️ 9.0/10
2. [特斯拉 Roadster 演示加入冷气推进器与火箭推进模式](#item-2) ⭐️ 8.0/10
3. [Mercor 研究：美国 90%的工作时长缺乏有效的 AI 基准测试覆盖](#item-3) ⭐️ 8.0/10
4. [Waymo 宣布进军多伦多](#item-4) ⭐️ 7.0/10
5. [苹果 MLX 在四台 Mac Studio 集群上运行近万亿参数 Muse Spark Open](#item-5) ⭐️ 7.0/10
6. [巴黎政治学院解析《欧盟人工智能法案》对先进 AI 的监管](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude 揭开 NIST 椭圆曲线种子源自 lrand48 之谜](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 的 Claude 发现，NIST 的 P-192、P-224、P-256、P-384 和 P-521 椭圆曲线所对应的种子并非来自任何哈希算法，而是直接由 C 标准库的伪随机数生成器 lrand48 生成，并以 Unix 时间戳作为种子。这一发现解开了一个自 2000 年这些曲线随 FIPS 186-2 发布以来悬置约四分之一个世纪的谜团。 NIST 曲线种子的来源长期引发不信任，因为这些种子由 NSA 提供，批评者担心其中可能隐藏类似后来在 Dual\_EC\_DRBG 随机数生成器中发现的秘密后门。证明这些种子只是普通的 lrand48 输出，削弱（但并未完全消除）了外界对广泛部署的密码标准中存在蓄意参数操纵的怀疑。 即便生成方法得到确认，外界仍无法看到哪些候选种子在生成后被丢弃，因此从原理上讲，这些曲线仍可能是通过在时间戳空间中搜索、以挑选具备某种特定性质的参数而得到。此外，第五个二进制域种子 B-163 与 Claude 尝试的任何方法都不匹配，仍然无法解释，一种可能较为平淡的解释是发布该数值时出现了笔误。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: 椭圆曲线密码学的安全性依赖于曲线和生成元的参数选择，ANSI X9.62 等标准要求以“可验证随机”的方式生成参数，即对任意种子做 SHA-1 哈希再推导参数，从而杜绝暗中做手脚的可能。NIST 在 2000 年的 FIPS 186-2 中公布了 P-192 至 P-521 曲线，其种子由 NSA 提供，但原始种子值从未公开，密码学家 Filippo Valsorda 因此悬赏 1.2 万美元征集这些种子。lrand48 是经典 System V C 库的伪随机数生成器，采用线性同余算法和 48 位整数运算，很容易用当前时间等可预测值作为种子。此外，椭圆曲线标准可能暗藏后门的担忧曾因 Dual\_EC\_DRBG 事件而广为人知。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://words.filippo.io/dispatches/seeds-bounty/">Announcing the $12k NIST Elliptic Curves Seeds Bounty</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/bounty-offered-for-secret-nsa-seeds-behind-nist-elliptic-curves-algo/">Bounty offered for secret NSA seeds behind NIST elliptic curves algo</a></li>
<li><a href="https://www.schneier.com/blog/archives/2023/10/bounty-to-recover-nists-elliptic-curve-seeds.html">Bounty to Recover NIST &#x27;s Elliptic Curve Seeds - Schneier on Security</a></li>

</ul>
</details>

**社区讨论**: 评论者大多为此发现欢呼，认为这终结了“13 年的阴谋论帽子”，有人调侃说这对整整一代 NIST 密码学阴谋论而言是毁灭性消息。但更谨慎的观点（也得到所链接分析的呼应）指出，确认生成方法并不能对参数选择下结论，因为被丢弃的候选值无从查证，理论上仍可能通过搜索时间戳来挑选具备特定性质的曲线。还有评论者认为，B-163 对不上很可能只是发布时的笔误，而非采用了另一种生成方法。

**标签**: `#cryptography`, `#NIST`, `#elliptic-curves`, `#random-number-generation`, `#AI-assisted-research`

---

<a id="item-2"></a>
## [特斯拉 Roadster 演示加入冷气推进器与火箭推进模式](https://www.tesla.com/roadster) ⭐️ 8.0/10

特斯拉发布了新的 Roadster 演示视频及配套社交媒体内容，展示该车配备冷气推进器，并在另一个“仅限受邀”版本中搭载真正的燃烧式火箭发动机，视频中车辆可垂直行驶并呈现出飞行状态。官方描述了两个版本：使用冷气（无燃烧）推进的版本仅用于增强前向加速，以及在视频中出现的燃烧火箭版本。 这次演示把一再跳票的 Roadster 重新包装为极端工程能力的展示，而非近期可交付的产品，从而引发巨大关注（Hacker News 上超 1100 分、2000 多条评论），并加剧了外界对特斯拉能否真正兑现承诺车型的质疑。它还引发了关于安全性、环境影响，以及这类推进系统是否存在现实商业化路径的更广泛讨论。 冷气推进器通过喷管排出加压的（通常为惰性的）气体产生推力，过程中不发生燃烧，因此是结构最简单、成本最低、最可靠的火箭推进形式，但推力效率远低于燃烧式发动机；由于不涉及火工品和污染物，它常被用于 CubeSat 的姿态控制。评论者指出，压缩气体储量可能非常有限，推进器可能对车辆侧后方的任何人造成危险，并且有报道称特斯拉“无法保证”现有的 Roadster 预订最终能够交付。

hackernews · shekhar101 · 10月16日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50112657)

**背景**: 冷气推进器是一种完全依靠储存的加压气体膨胀来产生推力的火箭发动机，过程中没有燃烧——结构上仅包含气瓶、调节阀、喷管和少量管路。由于结构简单且不产生污染性排气，它被广泛用于航天器的姿态控制和轨道维持，尤其是 CubeSat 等小型卫星。Roadster 是特斯拉承诺已久的第二代跑车，2017 年首次亮相后屡次延期，马斯克此前曾提出为它加入“SpaceX 套件”，即用冷气推进器大幅提升加速性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster</a></li>

</ul>
</details>

**社区讨论**: 社区情绪在由衷惊叹与强烈质疑之间分裂：一些评论者对车子“真的会飞”并能垂直行驶感到震惊，另一些人则斥之为炒作股价的营销噱头、永远无法量产交付。反复出现的担忧包括冷气推进器所用推进剂成分不明、可能成为环境污染物，压缩气体储量有限以及推进器靠近人群时的安全风险，还有特斯拉无法保证现有预订最终交付。

**标签**: `#Tesla`, `#Roadster`, `#electric vehicles`, `#rocket propulsion`, `#marketing stunt`

---

<a id="item-3"></a>
## [Mercor 研究：美国 90%的工作时长缺乏有效的 AI 基准测试覆盖](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

Mercor 的 Labor Index 研究发布了一份“基准测试地图”，结论是美国约 90%的工作时长都花在现有 AI 基准测试很少覆盖、甚至完全没有覆盖的任务上。分析还发现，即使在控制了整体“AI 暴露度”之后，来自工资总额更高职业的 O\*NET 任务，在现有基准测试的提示词中仍被显著过度采样。 如果基准测试只覆盖了真实工作中很窄的一部分，那么榜单分数就很难代表模型在实际工作中是否真的有用——这对决定研究优先级的 AI 实验室、挑选供应商的企业，以及试图预测劳动力市场冲击的政策制定者都至关重要。这也意味着，对于经济中大量岗位而言，短期瓶颈可能不是模型能力本身，而是评测体系。 该研究把 O\*NET 的职业任务数据与基准测试的提示词集合进行匹配，作者指出大多数任务族被采样的密度极低——例如“社工就育儿问题为父母提供咨询”这类任务，仅凭大约 13 条提示词就被算作“覆盖良好”。社区读者也指出，该研究对“覆盖良好”的界定含义模糊，因为它既可能只是寥寥数条提示词，也可能意味着真正有代表性的覆盖。

hackernews · speckx · 10月16日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=50121179)

**背景**: O\*NET（Occupational Information Network，职业信息网络）是美国劳工部维护的一个免费数据库，用任务、技能、知识和能力等维度描述数百种职业，常被用作研究自动化与 AI 如何影响不同工作的分类体系。MMLU、SWE-bench 等 AI 基准测试则是用固定题目或任务给模型打分的标准化测试，也是比较前沿模型时最常被引用的数字。Mercor 是一个把领域专家与 AI 实验室、企业对接起来构建基准、训练数据和智能体评测的平台，这正是它会产出这类劳动力市场覆盖分析的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Occupational_Information_Network">Occupational Information Network - Wikipedia</a></li>
<li><a href="https://www.dol.gov/agencies/eta/onet">O*NET - U.S. Department of Labor</a></li>
<li><a href="https://www.mercor.com/">Mercor | Organizing human intelligence to power the AI economy</a></li>
<li><a href="https://www.unrot.co/blogs/what-are-ai-benchmarks">What Are AI Benchmarks ? MMLU &amp; SWE-bench Explained... | Unrot</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认可这一差距，但对表述方式提出质疑：有人认为这是“门卫谬误”（Doorman Fallacy）的一种版本——把“开门”自动化掉，却忽略了门卫承担的其他关键职能。也有人指出，“覆盖良好”实际上被当成了“有覆盖”的同义词，因为 13 条提示词根本无法代表一名社工的工作；还有人指出基准提示词明显偏向高薪职业。多位评论者把该发现与更大的概念联系起来——例如鲍莫尔成本病开始以微观形式出现（写代码省下的时间被演示、Jira 和 QA 填满），以及 Karpathy 关于 AI 目前仅承担个位数百分比工作的判断。

**标签**: `#AI benchmarks`, `#AI evaluation`, `#labor market`, `#future of work`, `#O\*NET`

---

<a id="item-4"></a>
## [Waymo 宣布进军多伦多](https://waymo.com/blog/2026/10/waymo-in-toronto/) ⭐️ 7.0/10

Waymo 发布博客文章，宣布将其自动驾驶网约车服务拓展至加拿大多伦多，从既有的美国市场进一步向外扩张。该公告开篇即强调创造就业岗位，并在 Hacker News 上引发了一场大规模讨论（264 分、368 条评论），内容既有乘客的第一手体验，也涉及部署与监管方面的担忧。 多伦多意味着 Waymo 将进入一个新的国家以及更寒冷、多雪的气候环境，这相当于检验 Waymo Driver 能否在其最成熟的阳光地带和加州城市之外同样适用。此举还会把自动驾驶网约车直接推到加拿大监管机构、当地出租车与网约车司机，以及 Uber 和 Tesla 的 robotaxi 等竞争者面前。 多伦多冬季的大雪、结冰以及道路上的融雪盐雾，对自动驾驶汽车所依赖的激光雷达、毫米波雷达与摄像头传感器套件构成严峻挑战，因为车道线和道路边缘都可能被遮盖。公告中对当地就业创造的强调，加上 Waymo 在其他地区遭遇的监管阻力，说明其落地既取决于技术成熟度，也同样取决于政治与立法层面的批准。

hackernews · ChrisArchitect · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118981)

**背景**: Waymo 是 Alphabet 旗下的自动驾驶子公司，运营着名为 Waymo One 的商业 robotaxi 服务，车上没有人类安全员，乘客付费乘坐；该服务已在凤凰城、旧金山、洛杉矶和奥斯汀等城市逐步铺开。其车辆依靠 Waymo Driver 这一整套车载系统，包括激光雷达、毫米波雷达、摄像头与车载计算平台，而非依赖远程人工驾驶。进入一个新国家不仅需要建图和车辆测试，还需要当地的运营许可和无人物流/载客服务的相关法规，因此此类公告往往会围绕就业与安全来表述。

**社区讨论**: 讨论情绪褒贬不一：多位评论者表示在旧金山乘坐 Waymo 的体验非常出色，也有人在东京街头看到 Waymo 车辆时感到兴奋；但一位在奥斯汀的乘客称，原本 9 分钟的行程被莫名其妙地“略微延长”到 45 分钟，最后客服只是把他们放在一家餐厅门口了事。也有人指出，多伦多的公告把创造就业放在突出位置，并提到波士顿地区因担心司机失业而出现了有组织的反对 Waymo 的活动。

**标签**: `#Waymo`, `#autonomous vehicles`, `#robotaxi`, `#Toronto`, `#Hacker News`

---

<a id="item-5"></a>
## [苹果 MLX 在四台 Mac Studio 集群上运行近万亿参数 Muse Spark Open](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 7.0/10

苹果机器学习研究团队发布博文，展示最新版本 MLX 如何通过分布式推理，让近万亿参数的前沿级模型 Muse Spark Open 在由四台 Mac Studio 组成的集群上运行，生成速度超过每秒 36 个 token。该方案借助 MLX 新增的分布式推理能力与基于 RDMA 的通信原语，把原本单台 Mac Studio（最高 512GB 统一内存）的部署扩展到多机集群。 它表明，由消费级苹果芯片台式机组成的集群也能以超过人类平均阅读速度的吞吐量来服务前沿规模的开源权重模型，这对希望以本地私有方式运行大模型的用户而言是一个实质性里程碑，可视为租用数据中心 GPU 之外的替代方案。这也巩固了苹果在本地/端侧 AI 生态中的地位，让开发者能在自己已有的硬件上运行超大模型。 头条图表中 15–36 token/秒的数据是在 8,192 token 上下文长度下测得的，有评论者指出这在当今已算很小；同时对比中 Meta 的 Muse Spark Open 使用 4-bit 量化，而 Qwen 仅以原生 BF16 呈现，批评者认为这种设置对 Qwen 并不公平。作为参考，苹果博文还在单台 Mac Studio 上测试了 Qwen 3.8 27B 与 Mistral Medium 3.5 128B，在 65,536 token 上下文下分别占用最高 68GB 和 158GB 内存。

hackernews · antipaul · 10月16日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=50118320)

**背景**: MLX 是苹果为 Apple silicon 打造的开源数组计算框架，围绕统一内存架构设计，使 CPU 与 GPU 可以共享数据而不必在各自独立的内存池之间来回拷贝。Muse Spark Open 是 Meta 推出的开源权重模型，面向编程与智能体任务，采用专家混合架构，总参数 816B（激活参数 42B），上下文窗口达 100 万 token。分布式推理指把单个模型拆分到多台机器上，使权重和计算量超出任何单机内存所能承载的范围，并通过 Thunderbolt 5 等高速互联上的 RDMA 让各节点保持同步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/MLX_%28machine_learning_framework%29">MLX (machine learning framework) - Wikipedia</a></li>
<li><a href="https://huggingface.co/meta-models/Muse-Spark-Open-816B-A42B">meta- models / Muse - Spark - Open -816B-A42B · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者更多是质疑基准测试本身而非工程实现：多人批评把 4-bit 的 Meta 模型与原生 BF16 的 Qwen 相比并不公平，认为这是带有营销目的的选择。也有人指出，头条吞吐量只在 8,192 token 上下文下测得，实际使用价值有限；同时有用户给出独立测试反驳，称单台 M5 Ultra 运行 DeepSeek 4.1 Flash 可达约 45 token/秒，M5 Max 也能顺畅运行 GLM 5.3 Flash，且质量指标经过验证。

**标签**: `#apple-mlx`, `#local-inference`, `#llm-serving`, `#distributed-computing`, `#benchmarking`

---

<a id="item-6"></a>
## [巴黎政治学院解析《欧盟人工智能法案》对先进 AI 的监管](https://news.google.com/rss/articles/CBMi0gFBVV95cUxNN1NtY0RrRzAyUHNSRnhCay1zQU80UkllT0N3UkJTcGdTV3QwdGtNUXRTZjdMczgyU0VfdUxELTlBNWpoUG5wRHgtVG9zWEZmTHlsSzc1ck5NTWM0RmJMRW0wNWZpVURWNUZncHJScDdCNVZtUnNwS3l0SUNEMWtCSnM1aW41SEZUN1BXbklRRlVFTE53cEh5N3hnS2Q0ZDhuTjExdDBVc2MyeXBodDZnaTVIVk03UFM4OWtiLWJoeHRhYk1vQzNCdVpyWXMxWjFEa3c?oc=5) ⭐️ 6.0/10

巴黎政治学院发布了一篇分析文章，梳理《欧盟人工智能法案》如何监管先进人工智能系统，并区分了法案中既有的规则、新引入的条款以及在实际落地中遇到的现实困难。文章重点讨论了法案法律文本与欧盟当前实际执行之间存在的合规落差。 《欧盟人工智能法案》是全球首部全面、横向的人工智能法律，因此它对先进模型和前沿模型的监管方式将影响全球开发者和部署者的合规预期。执行层面的模糊之处，既可能抬高欧洲中小型 AI 企业的成本，也可能形成被其他司法辖区效仿的事实全球标准。 该法案分阶段生效：不可接受风险做法的禁令与 AI 素养义务自 2025 年 2 月 2 日起适用，通用人工智能（GPAI）模型义务自 2025 年 8 月 2 日起适用，大多数高风险系统要求自 2026 年 8 月 2 日起适用，嵌入受监管产品中的 AI 则推迟至 2027 年。训练算力超过约 10^25 FLOP 的 GPAI 模型被推定具有系统性风险，违规最高可处 3500 万欧元或全球年营业额 7%的罚款。

rss · GoogleNews-欧盟监管 · 10月16日 07:53

**背景**: 《欧盟人工智能法案》于 2024 年 7 月 12 日刊登在《欧盟官方公报》上，并于 2024 年 8 月 1 日正式生效。它采用基于风险的分级监管思路：对低风险系统仅施加较轻的透明度义务，对招聘、信用评分和关键基础设施等高风险用途施加严格义务，并直接禁止社会评分、操纵性技术等做法。通用模型与前沿模型——即通常所说的“先进 AI”——则需遵守单独的透明度、文档记录与系统性风险义务，这正是巴黎政治学院这篇分析的重点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe ’s digital future</a></li>
<li><a href="https://artificialintelligenceact.eu/the-act/">The Act Texts | EU Artificial Intelligence Act</a></li>

</ul>
</details>

**标签**: `#EU AI Act`, `#AI regulation`, `#AI governance`, `#AI policy`, `#advanced AI`

---