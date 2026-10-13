---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 21 条内容中筛选出 6 条重要资讯。

---

1. [黑客远程触发欧洲超市冷柜自动除霜](#item-1) ⭐️ 8.0/10
2. [开发者将 WiFi 7 路由器芯片改造为 320 Msps 软件无线电接收机](#item-2) ⭐️ 8.0/10
3. [Codex CLI 默认静默安装常驻自更新后台守护进程](#item-3) ⭐️ 8.0/10
4. [Z.ai 发布面向法律工作流的智能体模型 GLM-Legal](#item-4) ⭐️ 7.0/10
5. [用 C 构建现代 Web 应用引发低依赖技术栈讨论](#item-5) ⭐️ 7.0/10
6. [Reddit 测试称 Meta 购物 AI Muse 偏袒知名商家](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [黑客远程触发欧洲超市冷柜自动除霜](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

一场网络攻击利用了欧洲多家连锁超市中联网的制冷控制器，波及包括 Intermarché 在内约 400 家法国门店，强制触发自动除霜循环，使冷柜温度升至约 50°C，扰乱了门店运营。报道称该事件还影响了配送物流和门店定价。 这是一起备受关注的现实案例，展示了 OT/ICS 攻击如何在零售场景中造成物理层面的破坏，表明保障食品安全的冷链基础设施也可能被用来对付运营方。它凸显出运营技术安全已不再只是工厂或公用事业的问题，而是影响到普通消费者的零售与供应链议题。 Danfoss 表示，被劫持的控制器大多是运行过时固件的旧型号，社区分析指向已有 15 至 20 年历史的设备，例如 SM800（2021 年停止支持）和 SC355（2016 年停止支持）。Claroty 的 Team82 此前已披露过 Danfoss 制冷控制器中的漏洞，Danfoss 也为受影响产品提供协同漏洞披露和安全公告。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**背景**: Danfoss 等厂商生产的商用制冷控制器负责管理超市陈列柜和冷库的温度、除霜循环与能效。厂商常鼓励将这些设备联网，以便远程诊断问题、无需派遣维修工程师即可启动除霜，并对整个门店群的性能进行基准比较。OT（运营技术）或 ICS（工业控制系统）安全专注于保护运行此类设备的物理过程装置，而这些设备往往缺乏现代安全功能，部署后也难以打补丁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybernews.com/security/danfoss-refrigeration-hack-france-supermarkets/">Refrigeration Cyberattack Hits French Supermarkets | Cybernews</a></li>
<li><a href="https://www.msn.com/en-us/technology/cybersecurity/danfoss-says-hacked-controllers-behind-50c-french-supermarket-fridges-ran-old-firmware/ar-AA2e6nkW">Danfoss says hacked controllers behind 50C French ... - MSN</a></li>
<li><a href="https://en.wikipedia.org/wiki/IoT_security_device">IoT security device</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者将可能的根源追溯到已有 15 至 20 年历史、已停产支持的 Danfoss 控制器，并争论为何不安全设备会联网，提到厂商的远程管理功能以及需付费订阅才能运行测试的实验室设备。还有人将此事件与 2026 年 8 月美军军营商店冷柜遭入侵的事件联系起来，猜测是否为同一攻击者、模仿者，还是完全无关。

**标签**: `#cybersecurity`, `#ICS-OT-security`, `#IoT`, `#supply-chain`, `#infrastructure`

---

<a id="item-2"></a>
## [开发者将 WiFi 7 路由器芯片改造为 320 Msps 软件无线电接收机](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

开发者 h0m3us3r 逆向工程了 W1700K WiFi 7 路由器所用的芯片组，使其能够作为软件无线电（SDR）接收机工作，在 5 GHz 频段实现 320 Msps 的采样率，并将成果以开源项目形式发布在 GitHub 上。 这表明消费级 WiFi 7 硬件能够以远低于专用设备的成本实现高带宽 SDR 接收，可能让爱好者、研究人员和小型实验室获得廉价的射频实验能力。如果该技术能推广到常见的 WiFi 网卡上，普通笔记本电脑也可能兼作宽带接收机。 该方案实现的是仅接收的 SDR，采样率为 320 Msps，中心频率位于 5 GHz 频段，并非覆盖从直流到极高频的通用接收机；由于针对同一芯片组，有评论者认为它也应能在带有内置 PCIe（可接 NVMe）的 Banana Pi R4 上运行。

hackernews · djfergus · 10月12日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=50055593)

**背景**: 软件无线电（SDR）用运行在通用处理器上的软件取代传统模拟射频器件，如混频器、滤波器和解调器，通常由射频前端后的模数转换器提供信号输入。这样同一套硬件只需更换软件即可接收多种不同的无线协议。WiFi 7（IEEE 802.11be）是最新的 WiFi 标准，工作在 2.4、5 和 6 GHz 频段，其宽信道和高吞吐特性使其前端芯片组成为 SDR 实验中颇具吸引力的原始采样硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software-defined_radio">Software-defined radio</a></li>
<li><a href="https://en.wikipedia.org/wiki/WiFi_7">WiFi 7</a></li>

</ul>
</details>

**社区讨论**: 评论者反应热烈，指出该开发者此前还用 ESP32 微控制器做出过 SDR 项目（eSpDR），并希望这类技巧能普及到常见 WiFi 网卡，让任意笔记本都能变成廉价 SDR。也有人指出它很可能兼容 Banana Pi R4，称这是获得 5 GHz、320 Msps 接收机最便宜的方式，并畅想了手机中的软件无线电，以及用桌面 CNC、廉价 PCB 和通用元件自制现代服务监视器的可能性。

**标签**: `#SDR`, `#WiFi 7`, `#hardware-hacking`, `#RF`, `#embedded-systems`

---

<a id="item-3"></a>
## [Codex CLI 默认静默安装常驻自更新后台守护进程](https://github.com/openai/codex/issues/48195) ⭐️ 8.0/10

一个被广泛讨论的 GitHub issue（openai/codex \#48195）指出，OpenAI 的 Codex CLI 默认会安装一个常驻且自更新的后台守护进程，且没有公开的关闭方式。该 issue 在 Hacker News 上引发了 488 分、249 条评论的讨论，起因是社区报告了数 GB 的磁盘占用、权限损坏以及隐蔽的后台行为。 Codex CLI 是一款广受欢迎的开发者工具，默认安装常驻自更新守护进程会在用户未明确同意的情况下影响大量机器的磁盘占用和安全态势。这也引发了更广泛的行业问题：AI 编码代理究竟应在后台静默安装多少基础设施，而传统 CLI 又应遵循怎样的行为预期。 该守护进程目前位于一个功能开关之后，可通过在 ~/.codex/config.toml 的 \[features\] 下设置 daemon\_auto\_start = false 来关闭，但官方并未提供设置界面或文档来暴露这一点。用户报告该守护进程会向 ~/.codex 写入 pid 和锁文件，并且有用户测量出旧版本累积占用约 12 GB 磁盘空间。

hackernews · whimblepop · 10月12日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=50060694)

**背景**: Codex CLI 是 OpenAI 推出的本地终端编码代理，与当年驱动 GitHub Copilot 的原始 Codex 语言模型并非同一事物。守护进程是指在后台持续运行的进程，而非随终端窗口启停；自更新守护进程则会自行拉取新版本。用户通常期望通过 NPM 等包管理器安装的 CLI 只在被调用时运行，而不会静默地常驻或自行更新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openai/codex/issues/48195">CLI: make ` daemon _auto_start` opt-in — a persistent, self - updating ...</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28language_model%29">OpenAI Codex (language model)</a></li>

</ul>
</details>

**社区讨论**: 评论区的意见总体上偏批评：有人指出该守护进程缺乏文档，但可通过功能开关关闭；有人报告旧版本累积占用约 12 GB 磁盘；还有人描述自更新会破坏文件权限、使 .git 变为只读的 bug。也有用户对通过 NPM 安装的 CLI 竟然启动常驻后台进程感到不满，少数用户则提到极简的裸机式 harness 替代方案，认为它相较过度工程的代理令人耳目一新。

**标签**: `#Codex CLI`, `#OpenAI`, `#background daemon`, `#privacy`, `#software engineering`

---

<a id="item-4"></a>
## [Z.ai 发布面向法律工作流的智能体模型 GLM-Legal](https://z.ai/blog/glm-legal) ⭐️ 7.0/10

Z.ai 发布了 GLM-Legal，这是一款面向法律领域的智能体（agentic）大语言模型，官方从复杂任务执行、专业法律推理和真实法律工作流三个维度对其进行了评测。公司称该模型在 Harvey LAB 上取得 19.2% 的全部通过率，并在 LegalBench 和 PLawBench 上追平前沿闭源模型，同时参数量显著更小。 此次发布表明前沿模型厂商正在向高风险的专业领域推进，而在这类领域出错会带来真实的法律与财务后果；与此同时，业界正在激烈争论 AI 系统是否可以在没有合格人类审核者的情况下介入法律事务。较低的全流程通过率也为“智能体 AI 距离独立交付可直接给客户使用的法律成果还有多远”提供了一个具体的数据点。 Harvey LAB 上 19.2% 的全部通过率意味着该模型在绝大多数端到端法律任务上仍然失败，厂商自己也把这视为智能体法律工作尚不成熟的证据。Z.ai 还表示其评测框架与模型训练是协同迭代的，生产环境反馈会被转化为具体的工程优化信号。

hackernews · ilreb · 10月12日 16:11 · [社区讨论](https://news.ycombinator.com/item?id=50058507)

**背景**: Z.ai 是智谱 AI（Zhipu AI）的国际化品牌，这家中国公司由清华大学的研究人员于 2019 年创立，开发开放权重的 GLM（General Language Model，通用语言模型）系列，该系列首个模型于 2021 年发布，并在 2023 年以 ChatGLM 聊天机器人的形式广为人知。GLM-Legal 是该系列面向法律实务的领域专用变体，采用 LegalBench、PLawBench 和 Harvey LAB 等法律基准进行评测，这些基准考察的是推理与任务完成能力而非普通闲聊。这里的“智能体（agentic）”指模型被期望自主执行多步骤工作流，而不仅仅是回答单个问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://z.ai/blog/glm-legal">GLM-Legal: Advancing Agentic Legal Intelligence</a></li>
<li><a href="https://www.unite.ai/z-ai-unveils-glm-legal-an-agentic-model-for-legal-workflows/">Z.ai Unveils GLM-Legal, an Agentic Model for Legal Workflows</a></li>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z.ai - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者整体持怀疑态度：一位律师表示基准测试 20% 的通过率并不令人印象深刻，因为诉讼实务的关键在于应对全新情形，而不是重复处理过去已经见过的案件。其他人则提出信任方面的担忧，指出此前有报道称 Z.ai 在每次提示前会对整个工作区做快照，还有评论者引用 Anthropic 的政策更新，指出在涉及法律权利等用途时必须配备合格的“人类在环”审核者。也有反对观点认为，LLM 仍可帮助清理大量积压案件，例如印度 5800 万件待审案件中事实清晰的案件。

**标签**: `#AI`, `#legal-tech`, `#LLM`, `#benchmarks`, `#privacy`

---

<a id="item-5"></a>
## [用 C 构建现代 Web 应用引发低依赖技术栈讨论](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

一篇题为《A Modern Web App in C》的文章演示了如何使用 C 语言构建现代 Web 应用，主张采用简单、低依赖的服务端架构。该文在 Hacker News 上引发热烈讨论（426 分，175 条评论），话题涵盖 CGI、FastCGI、权限分离以及各种替代性 Web 技术栈。 这篇文章及其讨论反映了对重量级、高依赖 Web 框架日益增长的反向思潮，表明像 CGI 这样的数十年前技术在许多场景下依然可行。这对重视简洁性、安全性和运维极简主义的系统程序员与小型团队开发者而言意义重大，也引发人们对生态潮流之外的替代方案的思考。 讨论中的实践者强调了诸如 pledge 和 chroot 之类的降权机制，并指出 BusyBox 内置了 cgi-bin 支持；也有读者质疑通过 nginx 为每个请求调用一个二进制文件（经典 CGI 模型）是否优于有状态的后端进程。

hackernews · prophittcorey · 10月12日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50058528)

**背景**: 通用网关接口（CGI）是一种接口规范，允许 Web 服务器执行外部程序来处理 HTTP 请求，是生成动态内容的基础方式之一。FastCGI 是后来出现的二进制协议变体，旨在减少 CGI 每次请求产生的进程开销。权限分离是一种安全技术，将程序拆分为多个组件，每个组件只被授予完成任务所需的最小权限，从而限制漏洞可能造成的损害。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Common_Gateway_Interface">Common Gateway Interface - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/FastCGI">FastCGI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Privilege_separation">Privilege separation</a></li>

</ul>
</details>

**社区讨论**: 整体氛围积极且带有怀旧色彩，实践者纷纷分享 CGI 与 FastCGI 的实战经验：有人 22 年前基于 C/FastCGI 技术栈创办了 Web 开发公司，有人用 C++/WebAssembly 客户端加 C++服务端开发了类似《文明》的游戏，还有人提到 BusyBox 的 cgi-bin 支持。不过在架构上存在分歧，一些人更青睐有状态的 Rust/SQLite 后端（如 Tokio、Actix、Diesel），让进程常驻内存，而非每次请求都启动一个进程。

**标签**: `#C`, `#web-development`, `#systems-programming`, `#CGI`, `#hacker-news`

---

<a id="item-6"></a>
## [Reddit 测试称 Meta 购物 AI Muse 偏袒知名商家](https://www.reddit.com/r/ecommerce/comments/1x40wwd/metas_shopping_ai_is_stacked_against_you_if_you/) ⭐️ 6.0/10

据称一家分析公司拿到了 Meta 购物 AI 智能体 Muse 的内部指令，其中写明“必须”让排名前五的商品来自知名商家，随后该公司做了 50 次搜索来验证这一点。测试结果显示，Shopify 目录中的店铺贡献了 Muse 所考察商品的 94%，却只拿到约三分之一的展示位，其余位置被 Muse 自行找到的两个网站占据。 如果购物智能体成为人们网购的主要入口，那么写进智能体里的排序规则实际上就决定了哪些商家能被发现，而内置的对知名品牌的偏好可能会挤压目前充斥市场的小型独立店铺的生存空间。这让 Muse 内部的一个技术设计选择，变成了智能体电商中公平性与“守门人”角色的更大议题。 证据相当薄弱：结论仅来自一家分析公司的 50 次搜索测试，Meta 未作回应，也没有公布方法或原始数据，因此这些发现只能算个例观察，而非已被证实的偏见。Meta 对 Muse 的公开介绍强调它会搜索零售网站、追踪价格并为用户准备好待批准的购买，但并未披露商品排序的具体机制。

reddit · r/ecommerce · /u/BaptisteNo · 10月12日 12:46

**背景**: Muse 是 Meta 推出的个人 AI 智能体，其公布的用途之一就是购物：它可以搜索零售网站、推荐优惠、追踪价格，并准备好结账流程，等用户批准后才真正下单。与传统市场中按相关性或广告排序的搜索不同，AI 智能体是代替用户做选择，因此它内部的指引实际上就相当于一套排序政策。Shopify 的商品目录是一个规模庞大且结构化的商品数据源，Muse 这类智能体可以直接取用，这正是该平台上的商家如此关心自家商品会被如何对待的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.meta.com/muse/shopping/">Muse for Shopping: Deals, Price Tracking, Returns | AI at Meta</a></li>
<li><a href="https://www.cnbc.com/2026/10/03/meta-muse-shopping-ai-agent.html">Meta Muse shopping: How checkout, payments and privacy work</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#ecommerce`, `#Meta`, `#recommendation bias`, `#Shopify`

---