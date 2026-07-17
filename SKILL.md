---
name: derive-experience-design
description: "从模糊产品问题、具体 UI 截图或设计稿中推导体验设计策略、交互设计点、用户收益与汇报话术；也可验证设计是否回应问题，并区分体验策略、设计点、系统支撑机制和视觉表达。Derive experience-design strategies, interaction design points, user benefits, and presentation-ready narratives from fuzzy product problems, UI screenshots, mockups, or combined problem-and-design inputs. Use for design rationale, UX strategy, portfolio storytelling, design reviews, and bilingual Chinese-English design analysis."
---

# 体验设计策略推导 / Derive Experience Design

将不完整的产品输入转化为可论证的“问题 → 体验策略 → 具体设计表达”链路，不虚构用户证据、行为或指标。

Turn incomplete product inputs into a defensible chain from problem to experience strategy to concrete design expression. Do not invent user evidence, behavior, or metrics.

## 语言规则 / Language behavior

- 默认跟随用户使用的主要语言输出。/ Match the user's primary language by default.
- 用户要求“中英文”“双语”或 bilingual 时，按“中文在前、英文在后”成对输出。/ When bilingual output is requested, present Chinese first and English second.
- 中英文版本保持结构、结论和信息量一致，不把英文缩减为摘要。/ Keep the structure, conclusions, and information density equivalent in both languages.
- 使用 [术语对照表](references/reasoning-framework.md#术语对照--terminology) 保持核心概念稳定。/ Use the terminology table to keep key concepts consistent.

## 选择输入路径 / Select the input path

分析前选择一种路径：/ Choose one path before analyzing:

1. **模糊问题 / Fuzzy problem**：只有趋势、痛点、想法或尚未说清的问题，没有设计图。
2. **具体设计 / Concrete design**：提供截图、设计稿、原型、流程或详细界面描述。
3. **问题＋设计 / Problem plus design**：同时提供问题与方案，需要验证设计是否真正回应问题。

缺少必要信息时，明确最小假设。只有不同答案会实质改变策略时才提问。

When essential context is missing, state the smallest reasonable assumptions. Ask only when different answers would materially change the strategy.

## 检查视觉证据 / Inspect visual evidence

提供图片或本地截图时：/ When an image or local screenshot is provided:

1. 先查看图片，再得出结论。/ Inspect the image before drawing conclusions.
2. 识别可见结构、层级、控件、状态、标签、关系和产物区域。/ Identify visible structure, hierarchy, controls, states, labels, relationships, and output areas.
3. 区分“画面可见”与“行为推断”，把未经验证的动效、跳转、数据流和无障碍行为标记为假设。/ Separate visible evidence from inferred behavior; mark unverified motion, transitions, data flow, and accessibility behavior as assumptions.
4. 将每个设计点对应到具体区域、状态或交互入口。/ Tie every design point to a visible region, state, or interaction entry point.

只有静态画面时，不声称完成了全流程审计。用户要求真实多步骤体验审计时，先执行适用的审计流程，再用本 Skill 提炼策略。

Do not claim a full-flow audit from one static state. For a live multi-step audit, run the applicable audit workflow first, then use this skill to synthesize strategy.

## 执行推导链路 / Run the reasoning chain

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

对于模糊问题，推断最小且合理的行为矛盾，并明确标记假设。对于具体设计，从可见选择反向推导策略，再检查策略是否连贯。

For a fuzzy problem, infer the minimum plausible behavior tension and label it as an assumption. For a concrete design, reason backward from visible choices, then test the coherence of the inferred strategy.

问题模糊、跨多个页面或混合了 UX 与系统机制时，读取 [推导框架 / reasoning framework](references/reasoning-framework.md)。

## 正确区分概念层级 / Classify each claim correctly

- **体验目标 / Experience goal**：希望用户达到的状态，例如理解进度或重新获得控制。
- **体验设计策略 / Experience strategy**：改变用户与任务关系的可复用原则，例如结果前置、状态可见、渐进披露或异常时介入。
- **具体设计点 / Design point**：任务卡片、下钻入口、预览面板、恢复操作或同步视图切换等具体选择。
- **支撑机制 / Support mechanism**：Agent 路由、任务编排、模型选择、环境诊断或依赖调度等系统能力。
- **视觉表达 / Visual expression**：角色形象、空间布局、颜色、动效或插画等表现手段。

Do not promote layout, system capability, or visual styling into an experience strategy by itself. Explain how it becomes user-facing through visibility, control, feedback, recovery, or reduced effort.

不要把布局、系统能力或视觉样式本身包装成体验策略。说明它如何通过可见性、控制、反馈、恢复或减少操作成本影响用户。

## 推导高质量设计点 / Derive strong design points

每个设计点包含四部分：/ Give every design point four parts:

1. **设计选择 / Choice**：界面或交互做了什么。
2. **对应问题 / Problem**：解决了什么用户困难。
3. **作用机制 / Mechanism**：为什么能改变理解、成本、控制感或信心。
4. **用户收益 / Benefit**：什么因此变得更容易、更清楚、更安全或更高效。

使用以下句式检查：/ Use this sentence test:

> 通过 **[设计选择]**，解决 **[问题]**，借助 **[作用机制]**，让用户能够 **[收益]**。  
> By **[choice]**, the design addresses **[problem]**, enabling **[mechanism]**, so users can **[benefit]**.

拒绝“布局更清晰”“更有沉浸感”“提升效率”等缺少因果机制的泛化表述。

Reject generic claims such as “the layout is clearer,” “the experience is more immersive,” or “efficiency is improved” unless the causal mechanism is stated.

## 保持策略精简 / Prefer a small strategy set

默认输出三至五条策略，合并重叠项，把页面或组件细节放在策略之下。/ Default to three to five strategies. Merge overlaps and place screen- or component-level details underneath.

每条策略必须：/ Each strategy must:

- 对应明确的问题；/ trace back to a named problem;
- 产生至少一个可观察的设计点；/ produce at least one observable design point;
- 描述用户结果，而不是功能名称；/ describe a user outcome rather than a feature;
- 与其他策略保持区分；/ remain distinct from the other strategies;
- 不虚构研究结果或指标。/ avoid unsupported research or metrics.

多页面流程优先按一条主用户旅程组织，不要按互不相关的功能分类堆叠。

For multi-screen flows, organize design points around one primary user journey rather than unrelated feature categories.

## 组织输出 / Shape the response

先给出一句核心设计判断，再按需求选择以下部分：/ Lead with one core design judgment, then select only the useful sections:

1. **核心判断 / Core thesis**：一句话重构问题。
2. **问题到策略 / Problem-to-strategy chain**：展示因果推导。
3. **体验策略 / Experience strategies**：三至五条可复用原则。
4. **具体设计点 / Concrete design points**：对应区域、状态、步骤或交互。
5. **优势 / Advantages**：认知成本、连续性、可控性、信任、恢复或交付价值。
6. **边界与取舍 / Tradeoffs and boundaries**：说明设计失效或沦为装饰的条件。
7. **汇报话术 / Presentation wording**：一段可以直接口述的表达。

用户准备报告、作品集或 PPT 时，读取 [输出模板 / output patterns](references/output-patterns.md)。

## 质量检查 / Quality check

交付前确认：/ Before handing off, verify:

- 解释了为什么，而不仅是画面上有什么。/ Explain why, not only what is visible.
- 每条策略都对应真实问题或明确标记的假设。/ Map every strategy to a real or explicit assumed problem.
- 每个设计点都包含选择、问题、机制和收益。/ Include choice, problem, mechanism, and benefit for every design point.
- 不混淆可见证据与推断。/ Keep visible evidence separate from inference.
- 区分体验策略、支撑机制和视觉表达。/ Separate experience strategy, support mechanism, and visual expression.
- 将布局视为策略的落地，而不是策略本身。/ Treat layout as a manifestation of strategy, not the strategy itself.
- 收益具体，但不虚构指标。/ Make benefits specific without inventing metrics.
- 区分“为什么这样设计”与“设计图里如何落地”。/ Distinguish why the design exists from how it appears in the solution.
- 双语输出的结构、结论和术语保持对应。/ Keep structure, conclusions, and terminology aligned in bilingual output.

