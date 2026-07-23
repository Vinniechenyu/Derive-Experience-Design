# Derive Experience Design

面向 Codex、Claude Code 及其他支持目录式 Skill / Agent Instructions 的体验设计推导 Skill，用于从模糊产品问题、具体 UI 截图或设计稿中，提炼可论证的体验策略、设计点、用户收益与汇报话术。  
An experience-design reasoning skill for Codex, Claude Code, and other agents that can load directory-based skills or instructions. It turns fuzzy product problems, UI screenshots, and mockups into defensible experience strategies, concrete design points, user benefits, and presentation-ready narratives.

它不是一套固定 UX 原则清单，也不是看到界面后泛泛描述“布局清晰”或“提升效率”。它提供一条可复用的推导链：从背景变化和行为矛盾出发，识别根本体验问题，形成体验目标与策略，再映射到具体设计表达、用户收益和验证信号。  
It is neither a fixed checklist of UX principles nor a tool for generic claims such as “the layout is clearer” or “efficiency is improved.” It provides a reusable reasoning chain—from context change and behavior tension to root experience problem, experience goal, strategy, concrete design expression, user benefit, and validation signal.

## 适用场景 / Use cases

- 从模糊的产品趋势、痛点或想法中推导体验设计策略 / Derive experience strategies from fuzzy product trends, pain points, or ideas
- 根据 UI 截图、设计稿或原型提炼体验设计点 / Extract experience-design points from UI screenshots, mockups, or prototypes
- 检查设计方案是否真正回应了前置问题 / Test whether a design actually answers the stated problem
- 为作品集、设计评审和汇报整理“为什么这样设计” / Build the “why this design” narrative for portfolios, reviews, and presentations
- 区分体验目标、体验策略、设计点、系统支撑机制与视觉表达 / Separate experience goals, strategies, design points, support mechanisms, and visual expression
- 输出中文、英文或中英对照的设计分析 / Produce Chinese, English, or aligned bilingual design analysis

不适用于像素级视觉还原、没有真实流程证据的完整可用性审计、替代用户研究，或凭静态截图宣称无障碍合规。  
It is not intended for pixel-perfect visual reproduction, full usability audits without live-flow evidence, replacing user research, or claiming accessibility compliance from static screenshots.

### 搭配使用 / Pairs with

本 skill 负责「想清楚」，[report-deck-skill](https://github.com/Vinniechenyu/report-deck-skill) 负责「讲出来」：把这里推导出的体验策略与设计点交给它，落成 16:9 决策汇报 deck。两者术语一致，焊缝见 report-deck 的 `references/design-argument.md`。  
This skill does the thinking; [report-deck-skill](https://github.com/Vinniechenyu/report-deck-skill) does the telling—hand it the strategy and design points derived here to build a 16:9 decision deck. The two share terminology; the seam lives in report-deck's `references/design-argument.md`.

## 核心能力 / What it provides

### 1. 从模糊问题建立因果链 / Causal reasoning from fuzzy problems

将不完整的问题整理为：  
Turn incomplete inputs into:

```text
背景变化或用户信号 / Context change or user signal
→ 行为矛盾 / Behavior tension
→ 根本体验问题 / Root experience problem
→ 期望用户状态 / Desired user state
→ 体验设计策略 / Experience strategy
→ 具体设计点 / Concrete design point
→ 用户收益 / User benefit
→ 产品价值或验证信号 / Product value or validation signal
```

缺少信息时明确最小假设，不虚构用户证据、行为或指标。  
When information is missing, it states the smallest reasonable assumptions instead of inventing user evidence, behavior, or metrics.

### 2. 从设计图反向推导体验价值 / Reason backward from design visuals

先识别画面中可见的结构、层级、控件、状态、标签和关系，再把每个设计点绑定到具体区域、状态或交互入口。可见证据与交互推断会被明确区分。  
The skill first identifies visible structure, hierarchy, controls, states, labels, and relationships, then ties each design point to a specific region, state, or interaction entry. Visible evidence is kept separate from inferred behavior.

### 3. 体验策略与技术机制分层 / Separate experience strategy from technical mechanisms

Skill 将内容分为五层：  
The skill classifies claims into five layers:

- **体验目标 / Experience goal**：用户希望达到的状态 / the user state to achieve
- **体验设计策略 / Experience strategy**：改变用户与任务关系的可复用原则 / a reusable principle that changes the user's relationship with the task
- **具体设计点 / Design point**：可观察的界面或交互选择 / an observable interface or interaction choice
- **支撑机制 / Support mechanism**：Agent 编排、路由、诊断或数据处理等系统能力 / system capabilities such as orchestration, routing, diagnosis, or data processing
- **视觉表达 / Visual expression**：布局、颜色、动效、角色或空间隐喻 / layout, color, motion, characters, or spatial metaphor

布局、系统能力和视觉样式不会被直接包装成体验策略；只有当它们让系统行为变得可见、可控、可恢复或可验证时，才形成用户侧体验价值。  
Layout, system capability, and visual styling are not treated as experience strategies by themselves. They become user-facing experience value when they make system behavior visible, controllable, recoverable, or verifiable.

### 4. 可复用的设计点表达 / Reusable design-point framing

每个设计点按四部分组织：  
Every design point is expressed through four parts:

1. **设计选择 / Choice**：界面或交互做了什么 / what the interface or interaction does
2. **对应问题 / Problem**：解决了什么用户困难 / what user difficulty it addresses
3. **作用机制 / Mechanism**：为什么能改变理解、成本、控制感或信心 / why it changes understanding, effort, control, or confidence
4. **用户收益 / Benefit**：什么因此变得更容易、更清楚、更安全或更高效 / what becomes easier, clearer, safer, or more efficient

```text
通过 [设计选择]，解决 [问题]，借助 [作用机制]，让用户能够 [收益]。
By [choice], the design addresses [problem], enabling [mechanism], so users can [benefit].
```

### 5. 面向汇报的结构化输出 / Presentation-ready output

Skill 可根据交付场景选择以下输出结构：  
The skill can shape its response for different deliverables:

- 模糊问题 → 体验目标与策略 / Fuzzy problem → experience goals and strategies
- 设计图 → 设计点映射 / Design image → design-point mapping
- 问题＋设计 → 方案有效性验证 / Problem plus design → solution validation
- 作品集或汇报 → “为什么”与“如何落地”分层叙事 / Portfolio or report → separate “why” from “how it appears in the design”

### 6. 中英文一致输出 / Aligned Chinese-English output

默认跟随用户的主要语言。用户要求“双语”或 bilingual 时，中文在前、英文在后，并保持结构、结论、术语和信息量一致。  
The skill follows the user's primary language by default. When bilingual output is requested, it presents Chinese first and English second while keeping structure, conclusions, terminology, and information density aligned.

## 安装 / Installation

不同 Agent 的 Skill 发现方式可能不同。仓库仅包含 Markdown 和 Agent 元数据，可放入相应的 skills 目录，或由 Agent 直接读取 `SKILL.md`。  
Skill discovery differs across agents. This repository contains only Markdown and agent metadata, so it can be installed in the relevant skills directory or loaded directly through `SKILL.md`.

### Codex

```bash
git clone https://github.com/Vinniechenyu/Derive-Experience-Design.git \
  ~/.codex/skills/derive-experience-design
```

在任务中调用 `$derive-experience-design`。  
Invoke `$derive-experience-design` in your task.

### Claude Code

```bash
git clone https://github.com/Vinniechenyu/Derive-Experience-Design.git \
  ~/.claude/skills/derive-experience-design
```

也可以克隆到项目级 skills 目录，让它只在当前项目中生效。  
You may also clone it into a project-level skills directory so it applies only to that project.

### 其他 Agent / Other agents

将仓库加入 Agent 的技能或指令搜索路径；如果没有自动发现机制，要求 Agent 完整读取 `SKILL.md`，并按其中的路由加载 `references/`。  
Add the repository to the agent's skill or instruction search path. If automatic discovery is unavailable, instruct the agent to read `SKILL.md` completely and load the routed files under `references/`.

## 使用方式 / Usage

可以直接描述问题或提供设计图，不需要先指定 UX 框架名称。  
Describe the problem or provide a design visual directly; naming a UX framework is not required.

### 从模糊问题推导策略 / Derive strategies from a fuzzy problem

```text
使用 $derive-experience-design，分析为什么 Agent 工作空间要让任务成为一等公民，并输出体验设计策略和汇报话术。

Use $derive-experience-design to explain why tasks should become first-class objects in an agent workspace, then produce experience strategies and presentation wording.
```

### 从设计图提炼设计点 / Extract design points from a visual

```text
使用 $derive-experience-design，结合这张设计图，提炼核心体验策略、具体设计点、用户收益和风险边界。

Use $derive-experience-design to analyze this design image and extract core experience strategies, concrete design points, user benefits, and risk boundaries.
```

### 验证问题与方案是否匹配 / Validate problem-solution fit

```text
使用 $derive-experience-design，检查这个三栏方案是否真正回应了多任务监控问题，并指出缺口。

Use $derive-experience-design to test whether this three-column design actually addresses multi-task monitoring, then identify the gaps.
```

### 输出中英双语版本 / Produce bilingual output

```text
使用 $derive-experience-design，生成中英文对照的体验设计点 Markdown。

Use $derive-experience-design to create a bilingual Chinese-English experience-design-points Markdown document.
```

## 输入与输出 / Inputs and outputs

| 输入类型 / Input type | 典型输出 / Typical output |
| --- | --- |
| 模糊趋势、痛点或产品问题 / Fuzzy trend, pain point, or product problem | 核心判断、问题归因、体验目标、3–5 条策略、汇报话术 / core thesis, problem diagnosis, goals, 3–5 strategies, presentation wording |
| UI 截图、设计稿或原型 / UI screenshot, mockup, or prototype | 可见证据、设计点映射、策略归纳、风险与未知项 / visible evidence, design-point mapping, strategy synthesis, risks and unknowns |
| 问题＋设计方案 / Problem plus design | 问题到设计的追踪、有效设计点、逻辑缺口、改进建议 / problem-to-design traceability, strong points, gaps, improvements |
| 作品集或汇报材料 / Portfolio or report material | “为什么”策略层与“如何落地”方案层 / “why” strategy layer and “how” solution layer |

## 目录结构 / Repository structure

```text
SKILL.md                         Skill 入口、输入路由与核心推导流程 / entrypoint, input routing, and reasoning workflow
agents/openai.yaml              Agent 展示信息与默认调用提示 / agent metadata and default prompt
references/
  reasoning-framework.md       术语、问题诊断、策略选择与概念边界 / terminology, diagnosis, strategy selection, and boundaries
  output-patterns.md           四类输出模板与有效表达句式 / four output patterns and strong wording formulas
README.md                       仓库安装与使用说明 / repository installation and usage guide
```

## 验证 / Validation

当前 Skill 已使用 Codex Skill Creator 的 `quick_validate.py` 完成结构校验。它没有运行时脚本或第三方包依赖。  
The current skill has passed structural validation with Codex Skill Creator's `quick_validate.py`. It has no runtime scripts or third-party package dependencies.

使用时还应检查输出质量：  
When using the skill, also verify output quality:

- 每条策略都能回溯到真实问题或明确假设。 / Every strategy traces back to a real problem or explicit assumption.
- 每个设计点都包含选择、问题、机制和收益。 / Every design point includes choice, problem, mechanism, and benefit.
- 可见证据与交互推断没有混淆。 / Visible evidence is not mixed with inferred behavior.
- 体验策略、支撑机制和视觉表达保持分层。 / Experience strategies, support mechanisms, and visual expression remain distinct.
- 不虚构用户研究、行为数据或业务指标。 / No user research, behavior data, or business metrics are invented.

## 设计原则 / Design principles

- 从用户行为变化和判断任务开始，不从界面形式倒推价值。 / Start from behavior change and user judgment, not from interface form.
- 解释“为什么”，而不只描述画面上有什么。 / Explain why, not only what is visible.
- 将布局视为策略的落地，而不是策略本身。 / Treat layout as a manifestation of strategy, not the strategy itself.
- 系统机制只有在可见、可控、可恢复或可验证时才形成体验价值。 / System mechanisms become experience value when they are visible, controllable, recoverable, or verifiable.
- 默认保留三至五条相互区分的策略，避免堆砌原则。 / Prefer three to five distinct strategies instead of a pile of principles.
- 收益必须具体，但不能虚构指标。 / Make benefits specific without inventing metrics.
- 作品集与汇报中，策略页讲“为什么”，方案页讲“如何在设计图中落地”。 / In portfolios and reports, strategy pages explain why; solution pages show how the strategy appears in the design.

## About

一个将模糊问题与具体设计转化为清晰体验策略、设计点和汇报叙事的中英双语 Agent Skill。  
A bilingual agent skill that turns fuzzy problems and concrete design visuals into clear experience strategies, design points, and presentation narratives.

