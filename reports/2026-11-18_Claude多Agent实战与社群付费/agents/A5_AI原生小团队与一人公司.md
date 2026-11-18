# A5 · AI 原生小团队与一人公司：怎样用 agent 跑起一家公司或一个项目

> 编制：A5（R1 取证）｜日期：2026-11-18
> 检索记录：WebSearch 用了 14 次。WebFetch 用了 2 次，都失败了：techcrunch.com 和 leanaileaderboard.com 不在本会话网络白名单里，域名无法解析。
> 因此本文没有 E1 级原文，来源多为 E3（只读到检索摘要），关键数字留待 R3 复核。
> 另有三项为转引：S14 转引本仓库 10-19 报告，S17、S18 转引 10-17 报告。

## 1. 一句话结论

小团队靠 agent 把人效做到传统软件公司的数倍，已有一批可查证据（Gamma 约 50 人做到年化经常性收入〔ARR〕1 亿美元，Base44 被收购时只有 6–8 人），但"一人十亿美元公司"至今没有经核实的实例。能复制的模式是由一个人当"agent 管理者"：采集、初稿、核数这类机器能验证的环节交给定时 agent；判断、对外发布和涉钱涉法的环节留给人；每周把错误写回规则。

## 2. 关键发现

1. **人效差距是真的，但集中在产品本身就是 AI 的公司。** Lean AI 榜单要求入榜公司 ARR 超过 500 万美元、员工少于 50 人、成立不满 5 年。2025 年中的快照里，Midjourney 人均收入约 1,250 万美元，Cursor 约 500 万 [S5]。Gamma 约 50 人、Lovable 约 45 人时，ARR 都过了 1 亿美元（厂商自报）[S4]。这些公司吃到的是 AI 需求红利，不能直接证明 agent 能顶替全部职能（推断）。
2. **个人创始人在变多，但"一个人"多半只是起点。** Carta 数据显示，新公司中个人创始人的占比从 2019 年的 23.7% 升到 2025 上半年的 36.3%。但 2024 年个人创始的公司只拿到定价轮融资额的 14.7%，首次招人的中位时间是 399 天 [S2]。Base44 一个人起步，2025-06 被 Wix 以约 8,000 万美元收购时已有 6–8 名员工 [S3]；Lovable 从 45 人涨到了 146 人 [S4]。
3. **工程是最先被 agent 接管的职能。** YC 合伙人称，2025 冬季批次中约四分之一的公司，95% 的代码由 AI 生成（不含引入的库）[S6]。Every 用 Claude Code 维护 5 条产品线，基本每条只有 1 名工程师 [S1]。
4. **能持续下去，靠的是"复利"：每次出错都写成规则。** Every 的循环是计划 → 执行 → 评审 → 沉淀。每个修复、每个失败的测试都要写成文档，供后续的 agent 使用 [S1]。
5. **让 agent 自己经营时，结构比模型更重要。** Anthropic 的 Project Vend 第二期让一个 agent 当店长，给它接上 CRM 和成本数据，再加一个 CEO agent 审批，亏损的周基本消失了（厂商自报）[S7]。但同一模型互相监督，盲区也相同。店长 agent 还把"给 CEO agent 起名"的投票当成了"选举真人 CEO"，要人介入才收回控制 [S7]。
6. **"一人独角兽"仍是预测。** Anthropic CEO 在 2025-05 的开发者大会上预测，2026 年会出现第一家只有一名员工的十亿美元公司 [S8]。被引用最多的例子是 Medvi，自称 2 人、2025 年收入 4.01 亿美元，但只有二手转述，而且有报道称其存在未决的法律与监管问题 [S8]。本轮没有找到经核实的实例。
7. **长链条任务会漂移。** 记账基准 AccountingBench 让模型连续给一家真实公司做月结。Claude 4 和 Grok 4 头几个月准确率在 95% 以上，Grok 到第 5 个月骤降，另外三个模型连一个月都没做完。错误会逐月累积 [S10]。
8. **媒体的普遍做法是 AI 提速、由人发布。** 彭博 2025-01 起在文章上方加 AI 摘要，到 3 月底至少更正了 36 条，错误包括日期和财务表述 [S9]。路透用 AI 做转写这类提速工作，所有 AI 内容发布前都由记者核验 [S9]。受众也很谨慎：英国只有 11% 的人能接受"主要由 AI 制作、由人监督"的新闻 [S12]。
9. **无人值守的成本和限额会反过来约束你。** 因为部分用户让 Claude Code "24/7 在后台连续运行"，Anthropic 从 2025-08-28 起加了周限额 [S11]。2026-04-14 上线的云端定时运行功能（Routines）在预览期也有每小时触发上限 [S13]。

### 2.1 案例表

| # | 案例 | 人数 | 收入 / 用户 | agent 用在哪 | 来源 |
|---|---|---|---|---|---|
| 1 | Base44（以色列） | 一人起步，被收购时 6–8 人 | 2025-06 被 Wix 以约 8,000 万美元收购，另有到 2029 年的业绩对赌；用户 10 万–25 万（各家说法不一）；创始人自称单月利润 18.9 万美元 | 产品就是"对话生成应用"；没有外部融资 | S3 |
| 2 | Every | 5 条产品线，基本每条 1 名工程师 | 未披露 | 用 Claude Code 写代码，按复利工程运作 | S1 |
| 3 | Gamma | 约 50 人 | 2025-11 宣布 ARR 达到 1 亿美元并盈利 | 产品就是 AI 演示文稿 | S4，厂商自报 |
| 4 | Lovable（瑞典） | 45 人 → 146 人 | ARR 1 亿美元（2025-07）→ 4 亿美元（2026-02） | 产品就是建站 agent | S4，厂商自报 |
| 5 | Cursor | 约 300 人（2025） | 年化收入超过 20 亿美元 | 产品就是编码 agent | S4 |
| 6 | Midjourney、Cal AI、Mercor | 都少于 50 人 | 人均收入约 1,250 万、300 万、250 万美元（2025 年中快照） | AI 产品 | S5 |
| 7 | Medvi（美国远程医疗） | 自称 2 人 | 二手转述的 2025 年收入为 4.01 亿美元 | 自称用 AI 工具承担运营 | S8，E4，有争议 |
| 8 | Project Vend 第二期 | 多个 Claude agent，加人类监督 | 一个办公室小卖部，亏损的周基本消失 | agent 当店长，CEO agent 审批 | S7，厂商自报 |
| 9 | YC 2025 冬季批次 | 约 160 家公司 | 约四分之一的公司 95% 的代码由 AI 生成 | 工程 | S6 |

## 3. 可以直接照做的做法

### 3.1 按职能拆

标记含义：●已经靠谱，有人抽检即可；◐能用，但每次都要人把关；○还不能无人值守。判断是本文的推断，依据列给出佐证。

| 职能 | 判断 | 人工把关点 | 依据 |
|---|---|---|---|
| 工程 | ● | 合并前看改动、跑测试；AI 写的代码可能带安全漏洞 | S1、S6 |
| 产品与用户研究 | ◐ | agent 可以整理访谈、给反馈归类；定义问题和做取舍由人负责 | 推断 |
| 内容与营销 | ◐ | 人要核事实、数字、口吻和 AI 标识；发布按钮留在人手里 | S9、S12 |
| 销售线索 | ◐ | agent 可以筛选线索、起草回复；对外发出前由人审 | 推断 |
| 客服 | ◐ | Klarna 的 AI 助手能解决约 81% 的客服聊天，但 2025-05 因质量下降又重新招了人工；退款、投诉和情绪激动的对话要转人工 | S14 |
| 财务记账 | ○ | agent 只做分类和对账草稿；月结对账由人签字 | S10 |
| 法务合同 | ○ | 只做条款初筛；签字前由人或律师审 | 推断 |
| 招聘 | ◐ | agent 可以写职位描述草稿、做简历初筛；筛选标准和录用决定由人做 | 推断 |
| 数据分析 | ● | 口径和异常值要人核；给 agent 接上真实的成本和销售数据后，效果明显变好 | S7 |

### 3.2 运营节奏

**按"需不需要人守在电脑前"，工具分四档：**

1. **会话内轮询（`/loop`）**：会话开着时才运行 [S13]。
2. **本机定时**：用系统 cron 调用无头模式 `claude -p`，或者用桌面版的定时任务。电脑要一直开着，调度自己负责 [S13]。
3. **GitHub Actions**：适合"每次提交都自动跑检查"的仓库流程 [S13]。
4. **云端**：Claude Code Routines（2026-04-14 起为研究预览）把提示词、仓库和连接器存成一份配置，可以按定时、API 调用或 GitHub 事件在 Anthropic 云端运行，电脑可以关机 [S13]。
   - API 层还有 Managed Agents（beta）的两项功能：定时部署，以及 outcomes，即由一个独立的评分器按评分标准反复改到达标 [S15]。
   - 夜间不着急的批量任务可以走 Batch 接口，价格减半 [S15]。
   - n8n、Zapier 这类方案本轮没有检索。

**每日循环（以内容团队为例，推断）：**
- 开盘前：采集 → 提炼初稿 → 机器核数 → 人审签发 → 人工发布。
- 收盘后：agent 汇总当天的数据和异常。

**每周循环：**
- 周一：agent 出数据简报和候选选题，由人定选题。
- 周五：复盘，把本周的错误和人工改动写进 CLAUDE.md 或 skill。这就是 Every 循环里的"沉淀"一步 [S1]。

**"agent 管理者"每天做什么（推断）：**
- 早上约 15 分钟，看各个 agent 的产出和失败清单。
- 白天把时间花在定选题、抽检核数和签发上。
- 晚上约 10 分钟，把当天的错误写成规则。

Every 把这个角色描述为"同时调度多个 agent 做计划、编写和评估"[S1]。YC 创始人的说法更直白："我不怎么写代码，只思考和评审"[S6]。

**质量闸门分三层：**
- **机器闸门**：数字回查到原文页码，检查来源链接是否存在，扫描禁用词，检查 AI 标识。
- **人工闸门**：设在发布、对外承诺、涉钱涉法之前。
- **复盘闸门**：每周抽检一批，错误分类后写回规则。

Project Vend 的教训是，同一模型互相监督，盲区也相同 [S7]。所以检查要换一种方法：用脚本、换一个模型，或者由人来查。

### 3.3 财经内容与研究类业务的流水线

| 环节 | 能否自动化 | 必须人审的点 | 依据 |
|---|---|---|---|
| 采集 | 可以全自动：行情接口、公告、研报收件、去重 | 每周抽查信源 | 推断 |
| 提炼 | 自动出初稿 | 观点有没有被歪曲。彭博的 AI 摘要出过日期错误，还把顺差写成了逆差 | S9 |
| 核数 | 机器先核，人再抽检 | 时效性。财联社 2026-06 报道过一份券商研报的 AI 幻觉：把两年前的地产政策"嫁接"到了当下。受访者的共识是要保留人工审核 | S16 |
| 合规审查 | 用词表预筛 | 终审由人签发；AI 生成的内容必须显式标识 | S17 |
| 多格式改写 | 自动出小红书图文、抖音口播稿、社群短讯 | 口吻和标题 | 推断 |
| 分发 | 不自动化 | 全部由人操作。小红书 2026-03 起封禁两类账号：由 AI 工具直接注册、发布、互动的账号，以及公开笔记全部由 AI 托管代发的账号 | S18 |
| 数据复盘 | 后台数据导出后由 agent 汇总 | 下周选题由人定 | 推断 |

**同行实例：**
- **彭博**：AI 摘要放在记者稿件的上方 [S9]。
- **路透**：一个月内用 AI 转写了近 7,000 分钟、涉及 70 种语言的视频素材 [S9]。
- **财联社**：参与成立的财跃星辰推出了金融深度研究智能体"AI 小财神 Pro"[S16]。
- **Every**：本身是一家通讯媒体，同时用 agent 做软件产品 [S1]。
- **Axios、第一财经**：本轮没有找到具体的流程证据。

## 4. 反例、失败与局限

1. **质量漂移。** 长链条任务的错误会累积：AccountingBench 的月结准确率几个月后明显下滑 [S10]；Project Vend 的 agent 会误解一次投票的含义 [S7]。
2. **事实和口吻失守。** 彭博三个月内至少更正了 36 条 AI 摘要 [S9]。财经内容错一个数，伤的是付费用户的信任（推断）。
3. **AI 低质内容的反噬。** 在一项六国调查中，只有 12% 的人能接受完全由 AI 制作的新闻；有人把关时，这个比例也只升到 21% [S12]。Klarna 的客服回调说明，质量一下降，用户就会用脚投票 [S14]。
4. **平台封禁。** 小红书封禁 AI 托管账号 [S18]；AI 内容不做标识同样违规 [S17]。
5. **成本和限额失控。** 无人值守、24/7 运行，正是 Anthropic 加周限额的原因 [S11]。云端定时运行同样有触发上限 [S13]。
6. **幸存者偏差。** 高人效的公司大多卖的就是 AI 产品；Medvi 这样的"一人公司"带着监管疑问 [S8]；个人创始的公司拿到的融资占比也偏低 [S2]。

## 5. 对委托人的启示

1. **把"有活时集中对话"改成"每天两个定时任务"：盘前简报和研报收件分拣。**
   - 先用本机 cron 加 `claude -p` 跑通，稳定两周后再迁到云端 Routines。
   - 示例写法（需按本地配置调整）：`30 7 * * 1-5 cd <仓库> && claude -p "按 briefing 模板生成今日素材包" --allowedTools "mcp__Longbridge__quote,mcp__Longbridge__news"`。
   - 适用条件：模板和闸门已经固定下来。
   - Longbridge MCP 能不能在云端调用，需要实测（推断）。
2. **把现有 skill 的 PDF 回查和覆盖报数脚本抽出来，放进 GitHub Actions。**
   - 回查不通过，就不进 main。CI 里不用调用 Claude，只跑现有的脚本。
   - 同时把复制了 22 份的字体和二维码合并到一个共享素材目录。
   - 这是从"会用"走到"有系统"最小的一步（推断）。
3. **无人值守的任务只开放只读工具。** 据本会话可见的工具清单，Longbridge MCP 里有发帖、提醒、自选股写操作和账户查询等工具。定时 agent 只应允许行情、新闻、日历这类工具（推断）。
4. **坚持"agent 写、人发"。**
   - 分发和互动全部由人操作。
   - 合规 agent 只做预筛：扫描荐股措辞、买卖建议、大段复制原文、联系方式、缺少 AI 标识这几类问题。
   - 最后由人签发。
5. **每周五花 30 分钟复盘，把错误写回 skill。** 这一步成本最低，复利最大 [S1]。

**agent 团队编制表：**

| agent | 职责 | 输入 | 输出 | 频率 | 人审点 |
|---|---|---|---|---|---|
| 采集 | 收集行情、公告、要闻和研报，去重并附上来源 | Longbridge 只读工具、研报收件夹 | 当日素材包 | 交易日 07:00；研报到达时 | 每周抽查信源 |
| 提炼（研报可视化 v3） | 研报 → 大纲 → 2–4 页精华 | 研报 PDF | 精华 PDF、页面地图 | 每篇研报 | 大纲回"行"后才继续（已有） |
| 核数 | 数字回查到原文页码，行情二次取数，检查时效 | 精华稿、原文、行情接口 | 通过 / 不通过清单 | 每篇发布前 | 不通过的项由人判定；另抽检 10% |
| 合规 | 扫描红线词，检查 AI 标识 | 改写稿、红线词表 | 风险标注和修改建议 | 每条发布前 | 人终审签发（必须） |
| 改写 | 一稿出三版：小红书图文、抖音 60 秒口播、社群 3 行短讯 | 核过数的精华 | 三种格式的草稿 | 每篇 | 标题和口吻 |
| 社群编辑 | 每日"30 秒早报"、每周合集目录、汇总群内问题 | 素材包、已发内容、群内问题 | 各类草稿 | 每日一次，加每周一次 | 人审过后由人发出 |
| 数据分析 | 汇总平台导出的数据，以及社群续费和活跃数据 | 手动导出的 CSV | 周报、选题建议 | 每周五 | 选题由人定 |
| 规则维护 | 把核数失败、合规失败和人工改动写成规则 | 失败记录、修改前后的差异 | 规则变更 PR | 每周五 | 由人合并 |

分发和互动不设 agent。委托人本人就是 agent 管理者，预计每天投入 45–60 分钟（推断）。

## 6. 来源表

| 编号 | 标题 | 作者/机构 | 日期 | URL | 证据等级 |
|---|---|---|---|---|---|
| S1 | Compound Engineering: How Every Codes With Agents；播客 How Two Engineers Ship Like a Team of 15 With AI Agents | Dan Shipper、Kieran Klaassen / Every | 2025-12；2025 | https://every.to/source-code/compound-engineering-how-every-codes-with-agents ；https://every.to/podcast/how-two-engineers-ship-like-a-team-of-15-with-ai-agents | E3 |
| S2 | Solo Founders Report 2025；2026 Founder Ownership Report | Peter Walker 等 / Carta | 2025-12-09；2026 | https://carta.com/data/solo-founders-report ；https://carta.com/data/founder-ownership-2026-full-report/ | E3 |
| S3 | Wix acquires Israeli vibe coding co Base44；Calcalist、Ynet、DesignRush 同题报道 | Globes、Calcalist 等 | 2025-06-18/19 | https://en.globes.co.il/en/article-1001513267 ；https://www.calcalistech.com/ctechnews/article/s1iflnlelx ；https://news.designrush.com/wix-buys-ai-startup-base44-for-80m-six-month-sprint-deal | E3 |
| S4 | Gamma's GTM Playbook；How Many Employees Does It Take to Reach $100M ARR Now?；Lovable、Cursor 的维基词条 | Origin Notes；Nazr；Wikipedia | 2025-11–2026 | https://originnotes.substack.com/p/gamma-gtm-playbook ；https://nazr.com/blog/how-many-employees-100m-arr ；https://en.wikipedia.org/wiki/Lovable_(company) ；https://en.wikipedia.org/wiki/Cursor_(company) | E4 |
| S5 | Launching the Official Lean AI Leaderboard；AI Startups are Dominating Traditional Software in one Key Metric | Henry Shi；Jeremiah Owyang | 2025-03；2025-05-13 | https://henrythe9th.substack.com/p/launching-the-official-lean-ai-leaderboard ；https://web-strategist.com/blog/2025/05/13/ai-startups-are-dominating-traditional-software-in-one-key-metric/ | E3 |
| S6 | A quarter of startups in YC's current cohort have codebases that are almost entirely AI-generated；"I Don't Code Much, I Just Think And Review" | TechCrunch；Implicator | 2025-03-06；2025 | https://techcrunch.com/2025/03/06/a-quarter-of-startups-in-ycs-current-cohort-have-codebases-that-are-almost-entirely-ai-generated ；https://implicator.ai/i-dont-code-much-i-just-think-and-review-how-ai-transformed-yc-startups | E3（后者 E4） |
| S7 | Project Vend: Phase two（以及 The Decoder、DEV 等二手综述） | Anthropic（与 Andon Labs 合作） | 约 2025-12（依据二手报道推断） | https://www.anthropic.com/news/project-vend-2 | E3，厂商自报 |
| S8 | The First One-Person Billion-Dollar Startup Will Be A Reality By 2026；有关 Medvi 的二手文章 | OfficeChai；Pulse.bot / Medium | 2025-05；2026 | https://officechai.com/ai/the-first-one-person-billon-dollar-startup-will-be-a-reality-by-2026-anthropic-ceo-dario-amodei ；https://www.pulse.bot/entrepreneurship/blogs/the-one-person-billion-dollar-company-is-no-longer-a-prediction-it-happened-eada1ba9-1b5c-4cae-89e4-520520b66151 | E3（Medvi 部分 E4） |
| S9 | Bloomberg's use of AI summaries leads to numerous corrections；More than 2 years after ChatGPT, newsrooms still struggle with AI's shortcomings；科技新报的相关报道 | Washington Times（转述 NYT）；CNN Business（abc17news 转载）；TechNews | 2025-03-29；2025-05-28；2025 | https://m.washingtontimes.com/news/2025/mar/29/bloombergs-use-ai-summaries-articles-leads-numerous-corrections/ ；https://abc17news.com/money/cnn-business-consumer/2025/05/28/more-than-2-years-after-chatgpt-newsrooms-still-struggle-with-ais-shortcomings/ ；https://technews.tw/?p=1465032 | E3 |
| S10 | AccountingBench 报道（原始发布方为 Penrose） | Gigazine；Ledge.ai | 2025-07-24 | https://www.gigazine.net/gsc_news/en/20250724-accountingbench ；https://ledge.ai/articles/llm_accounting_benchmark_penrose | E3 |
| S11 | Anthropic unveils new rate limits to curb Claude Code power users | TechCrunch | 2025-07-28 | https://techcrunch.com/2025/07/28/anthropic-unveils-new-rate-limits-to-curb-claude-code-power-users/ | E3 |
| S12 | Digital News Report 2025 英国部分报道；Generative AI and News Report 2025 评述 | Press Gazette；journalism.co.uk（数据来自 Reuters Institute） | 2025-06；2025 | https://pressgazette.co.uk/publishers/news-trends-2025-digital-news-report/ ；https://www.journalism.co.uk/what-the-public-wants-seven-opportunities-for-newsrooms-in-the-age-of-generative-ai/ | E3 |
| S13 | Claude Code Routines 的发布与用法（第三方指南） | Daniel Vaughan；MindStudio | 2026-04-14 起 | https://codex.danielvaughan.com/2026/04/14/claude-code-routines-launch/ ；https://www.mindstudio.ai/blog/claude-code-scheduled-tasks-cloud-routines | E3–E4 |
| S14 | Klarna 客服 AI 与人工回调（转引本仓库 2026-10-19 报告的 R119、R244） | Entrepreneur；Klarna 向 SEC 提交的 6-K 投资者材料 | 2025-05；2025 年三季度 | https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396 ；https://www.sec.gov/Archives/edgar/data/2003292/000162828025052805/exhibit992klarnapresenta.htm | E3（转引，本轮未复核） |
| S15 | Claude API 技能文档（模型价格、Batch 接口、Managed Agents 的定时部署与 outcomes） | Anthropic（随 Claude Code 分发的技能文件） | 缓存于 2026-11-03 | 无公开 URL（本地 claude-api 技能文件，对应 platform.claude.com 文档） | E1（本地读取，未经 WebFetch） |
| S16 | 券商研报 AI 幻觉报道；财跃星辰"AI 小财神 Pro"发布报道 | 财联社 | 2026-06；2025–2026 | cls.cn（检索结果中有多篇，未能确认各篇对应的 URL） | E3 |
| S17 | 四部门发布《人工智能生成合成内容标识办法》 | 新华网 | 2025-03-14 | https://www.news.cn/politics/20250314/b7a24028f2924b7681e6ed1bfbd8fade/c.html | E3（转引 10-17 报告） |
| S18 | 小红书打击 AI 托管运营账号 | 界面新闻 | 2026-03-10 | https://m.jiemian.com/article/14095143.html | E3（转引 10-17 报告） |
