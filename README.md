# Research-backed Tutor · 研究型知识导师

**把“从基础讲清楚”变成一套可复用的学习流程：多轮查资料、核对证据、逐步推导，再用例题和自测检查理解。**

这是一个面向 Codex 的跨学科教学 skill。它引导 AI 先建立知识地图，再结合论文、教材、专家公开讲解和相关项目资料，为初学者生成有来源、有推理过程、有练习答案的学习手册。

[查看主 skill](research-backed-tutor/SKILL.md) · [下载原始安装包](https://github.com/Pavel-Embeded/research-backed-tutor/raw/refs/heads/main/dist/research-backed-tutor.zip) · [反馈问题](https://github.com/Pavel-Embeded/research-backed-tutor/issues)

## 一句话开始

安装后，在 Codex 中输入：

```text
使用 $research-backed-tutor，从基础讲清这个知识点，并附来源、例题和自测答案。
```

把“这个知识点”替换成具体主题，并补充你的基础和学习目的。例如：

```text
使用 $research-backed-tutor，给一个刚学数字电路的学生讲清异步 FIFO：
从时钟域、亚稳态和格雷码开始，逐步解释读写指针与空满判断，
附可靠来源、具体例子、常见错误、自测题和详细答案。
```

## 它会引导 AI 做什么

| 环节 | 具体要求 | 对学习者的价值 |
| --- | --- | --- |
| 明确目标 | 确认主题、已有基础、应用场景与所需深度；只澄清会影响教学的重要信息 | 讲解从合适的起点开始 |
| 建立知识地图 | 列出前置知识、核心概念、相邻概念、应用与争议 | 知道各部分为什么要学、如何连接 |
| 多轮研究 | 使用中英文关键词、同义词、参考文献追踪和缺口检索 | 减少只看一次搜索结果造成的遗漏 |
| 核对来源 | 区分全文、章节、摘要、预览、元数据和搜索片段 | 清楚哪些结论有直接证据 |
| 从基础推导 | 按前提、步骤、推论、假设与边界解释；保留关键中间过程 | 学会推理，而非只记结论 |
| 例题与迁移 | 先给简单例子，再改变条件；比较易混概念与错误解法 | 检查能否在新情境中使用知识 |
| 自测与补课 | 提供练习、详细答案和自评标准；针对错误补前置知识 | 发现自己具体卡在哪一步 |

这些是 skill 对执行过程的要求，实际完成情况取决于模型、可用工具、资料访问权限和任务规模。

## 适合哪些场景

- **数学与理工科**：定义、定理、推导、工程原理、条件与反例。
- **编程与项目学习**：沿输入、状态、输出和失败情形理解机制，结合代表性源码与测试。
- **跨学科学习**：梳理术语、背景、证据、解释与不同观点。
- **已有材料的深入学习**：结合你提供的教材章节、PDF、代码或题目，建立概念之间的联系。读取文件需要运行环境具备相应工具。

如果只需要一句定义、简单翻译或一个确定事实，通常不需要启动完整研究流程。

## 安装到 Codex

本仓库保留 skill 的独立目录：`research-backed-tutor/`。安装时复制这个目录，保留其中的 `agents/` 和 `references/`。

### 方法一：使用 skill-installer

在提供 `$skill-installer` 的 Codex 环境中输入：

```text
使用 $skill-installer，从 GitHub 仓库
https://github.com/Pavel-Embeded/research-backed-tutor
安装 research-backed-tutor 子目录中的 skill。
```

### 方法二：下载并手动放置

1. [下载原始 ZIP](https://github.com/Pavel-Embeded/research-backed-tutor/raw/refs/heads/main/dist/research-backed-tutor.zip)，解压得到 `research-backed-tutor/`。
2. 按使用范围，把该目录放到下面其中一个位置：

| 使用范围 | Windows | macOS / Linux |
| --- | --- | --- |
| 当前用户 | `%USERPROFILE%\.agents\skills\research-backed-tutor\` | `~/.agents/skills/research-backed-tutor/` |
| 当前项目 | `<项目目录>\.agents\skills\research-backed-tutor\` | `<项目目录>/.agents/skills/research-backed-tutor/` |

3. 确认目标目录中直接存在 `SKILL.md`，避免多嵌套一层同名文件夹。
4. 在 skill 选择器中找到“研究型知识导师”，或用 `$research-backed-tutor` 调用。如果尚未显示，重启 Codex 后再检查。

以上发现目录和调用方式依据 [OpenAI 官方 skill 文档](https://learn.chatgpt.com/docs/build-skills)。不同版本或受管理的环境可能有不同的安装配置，请以当前运行环境为准。

### 所需能力

- 能加载 Agent Skills 的运行环境；本仓库以 Codex 为主要使用对象。
- 研究任务需要联网检索和读取来源的工具。skill 本身不附带搜索引擎、账号、API 密钥或数据库权限。
- PDF、图表、代码执行或导出文档按任务需要使用环境中实际可用的工具或其他 skill。
- 支持并获准使用并行 agent 时，可分工研究不同来源；否则按顺序完成。

这是以指令和参考文件组成的 skill，包内没有必须运行的安装脚本。

## 更多调用示例

以下是可直接修改使用的提示词，**不是已完成研究或实测效果的展示**。

### 数学：从概念到解题

```text
使用 $research-backed-tutor，面向高中初学者讲清基本不等式。
从平方非负开始推导，解释正数条件、等号成立条件和常见变形，
给出基础例题与迁移题，附可核验来源、自测题和完整答案。
如果某道题的教材或考试出处无法核实，请明确标注。
```

### 编程：理解机制与失败情况

```text
使用 $research-backed-tutor，给熟悉 Python 基础的人讲清事件循环。
区分同步、并发和并行，逐步追踪示例的执行顺序，
结合官方资料解释常见错误，附自测题和详细答案。
```

### 人文：比较证据与解释

```text
使用 $research-backed-tutor，给没有经济学基础的人讲清机会成本。
从日常选择开始，给出准确定义和适用边界，
比较常见误解，结合可靠教材与公开讲解，附练习和答案。
```

## 默认学习手册应包含什么

1. 学习目标、假定基础与前置知识地图。
2. 概念出现的背景、要解决的问题、定义与适用边界。
3. 从基础出发的逐步解释或推导。
4. 简单例子、迁移例子，以及类比的适用范围。
5. 易混概念比较、常见错误、实际应用与整体关系。
6. 检查记忆、解释、应用和错误诊断的练习，配详细答案与自评标准。
7. 概念与来源的对应表、检索范围、访问限制、未解决的问题和观点分歧。

输出的数量和篇幅应随主题调整，避免为了填满结构而加入无关内容。完成一份手册不等于学习者已经掌握；自测需要检验能否迁移使用。

## 研究与证据约定

- 关键结论优先使用原始论文、可靠教材和官方文档，博客与项目资料需要交叉核对。
- 记录真实查询、日期、链接、读取范围、选取原因、冲突和缺口。
- 知网、Google Scholar、其他学术索引、GitHub、CSDN、教材和专家公开教学按相关性与实际可访问程度调查，不用无关资料凑数量。
- 专家讲解需要核实其相关贡献和实际公开内容，不能只因名气而引用。
- 摘要、目录、预览和搜索片段不能写成“已读全文”。访问不到的来源应说明限制。
- 检索停止条件是针对缺口的一轮搜索未再产生重要概念分支或纠正；不能宣称穷尽全部文献。

详细规则见 [研究方法](research-backed-tutor/references/research-method.md) 与 [教学指南](research-backed-tutor/references/teaching-guide.md)。

## 仓库结构

```text
research-backed-tutor/
├── README.md                          # 中文介绍、安装与调用示例
├── dist/
│   └── research-backed-tutor.zip       # 原始上传包，便于直接下载
└── research-backed-tutor/             # 实际安装的 skill 目录
    ├── SKILL.md                       # 触发描述与完整工作流程
    ├── agents/
    │   └── openai.yaml                # 中文显示名、简介和默认提示词
    └── references/
        ├── research-method.md         # 检索、证据、覆盖矩阵与停止条件
        └── teaching-guide.md          # 推导、例题、误区、自测与补课方式
```

## 当前版本与边界

本仓库发布的是原始 ZIP 中的 4 个 skill 文件，并补充中文 README。`dist/` 保存原始 ZIP，主 skill 和参考文件保留原文。

skill 定义的是研究和教学流程，不能保证所有来源可访问、每次回答都正确，或通过一次学习成为专家。它也不会自动获得付费数据库、绕过访问限制，或替代实际的实验与项目验证。发现证据不足时，应直接标明不确定性。

当前包未包含开源许可证，仓库暂未指定许可证。

## 反馈与改进

欢迎通过 [Issues](https://github.com/Pavel-Embeded/research-backed-tutor/issues) 提供具体学习主题、所用环境、提示词，以及实际输出中需要改进的部分。对于来源错误，请同时附上相关链接和对应结论；对于讲解问题，请指出缺失的前提或无法跟上的推导步骤。

如果这套学习流程对你有帮助，欢迎 Star，让更多学习者找到它。
