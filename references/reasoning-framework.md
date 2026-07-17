# 体验设计推导框架 / Experience Design Reasoning Framework

输入模糊、问题复杂或混合了产品机制与体验设计时使用本参考。  
Use this reference when the input is ambiguous, complex, or mixes product mechanisms with experience design.

## 术语对照 / Terminology

| 中文 | English |
| --- | --- |
| 体验目标 | Experience goal |
| 体验设计策略 | Experience strategy |
| 具体设计点 | Design point |
| 支撑机制 | Support mechanism |
| 视觉表达 | Visual expression |
| 渐进式信息披露 | Progressive disclosure |
| 状态可见 | Status visibility |
| 异常时介入 | Exception-based intervention |
| 结果前置 | Result-first presentation |
| 主线保护 | Mainline protection |
| 按需下钻 | Drill down on demand |
| 可恢复性 | Recoverability |
| 结果验收 | Result validation |

## 1. 识别行为变化 / Diagnose the behavior shift

从用户工作方式的变化开始，而不是从界面方案开始。  
Start with what changed in the user's work, not with the interface solution.

内部检查：/ Ask internally:

- 用户要完成什么？/ What is the user trying to accomplish?
- 用户需要理解、判断、监控或恢复什么？/ What must they understand, decide, monitor, or recover from?
- 用户角色是否发生变化，例如从操作者变成委托者或验收者？/ Has the user shifted from operator to delegator or reviewer?
- 哪些信息变得更重要，哪些成为噪音？/ What information becomes essential, and what becomes noise?

使用以下句式：/ Use this form:

> 用户需要 **A**，但当前模式迫使其 **B**，从而导致 **C**。  
> The user needs **A**, but the current model forces **B**, causing **C**.

## 2. 转化为体验目标 / Convert tension into an experience goal

描述期望用户达到的状态，而不是功能：/ Describe the desired user state, not a feature:

- 无需阅读全部信息也能理解；/ understand without reading everything;
- 中断后仍能快速恢复方向；/ regain orientation after interruption;
- 只在必要时介入；/ intervene only when needed;
- 无需重建上下文即可验收结果；/ validate results without rebuilding context;
- 理解复杂关系但不丢失主线。/ see complex relationships without losing the main thread.

“增加卡片”“采用三栏”“展示动画”属于方案，不是体验目标。  
“Add a card,” “use three columns,” and “show animation” are solutions, not goals.

## 3. 选择体验策略 / Choose an experience strategy

| 根本问题 / Root problem | 策略方向 / Strategy direction |
| --- | --- |
| 信息过载 / Information overload | 渐进披露、主线保护、先总览后细节 / progressive disclosure, mainline protection, overview before detail |
| 黑盒执行 / Black-box execution | 状态可见、里程碑说明、带证据的完成态 / status visibility, explainable milestones, evidence-backed completion |
| 监控成本高 / High monitoring cost | 异常时介入、可操作提醒、上下文可恢复 / exception-based intervention, actionable alerts, resumable context |
| 结果分散 / Fragmented results | 结果前置、集成预览、验证闭环 / result-first presentation, integrated preview, validation closure |
| 多任务并行 / Parallel tasks | 任务对象化、持久状态、任务总览 / task objectification, persistent state, portfolio overview |
| 关系复杂 / Complex relationships | 层级、同步多视图、空间或图谱总览 / hierarchy, synchronized views, spatial or graph overview |
| 恢复焦虑 / Recovery anxiety | 明确失败态、恢复路径、可逆操作 / explicit failure state, recovery path, reversible action |
| 责任不清 / Unclear responsibility | 角色可见、归属提示、升级路径 / role visibility, ownership cues, escalation path |

把这些视为起点，而不是固定分类。/ Treat these as starting directions, not a mandatory taxonomy.

## 4. 映射到可观察设计 / Map strategy to observable design

| 层级 / Layer | 检查问题 / Question |
| --- | --- |
| 信息 / Information | 展示、隐藏、分组或优先了什么？/ What is shown, hidden, grouped, or prioritized? |
| 交互 / Interaction | 用户可以打开、切换、确认、中断或恢复什么？/ What can users open, switch, confirm, interrupt, or recover? |
| 状态 / State | 如何表达进行、等待、失败、完成和待关注？/ How are progress, waiting, failure, completion, and attention needs expressed? |
| 连续性 / Continuity | 用户如何离开、返回并保留上下文？/ How do users leave, return, and retain context? |
| 结果 / Result | 用户如何查看、比较、验证或交付产物？/ How do users inspect, compare, validate, or deliver output? |

## 5. 区分 UX 与支撑机制 / Separate UX from support mechanisms

- 只描述系统内部行为的是支撑机制。/ Internal system behavior alone is a support mechanism.
- 描述用户如何理解、控制或恢复系统行为，才包含体验设计。/ It becomes experience design when it explains how users understand, control, or recover from that behavior.

| 支撑机制 / Support mechanism | 用户侧体验设计 / User-facing experience design |
| --- | --- |
| Agent 将工作路由给专家 / Agent routes work to a specialist | 显示任务归属、委派原因与状态 / show ownership, delegation reason, and status |
| 自动环境诊断 / Automatic environment diagnosis | 解释问题并提供恢复动作 / explain the problem and provide recovery action |
| 多 Agent 并行 / Parallel agents | 显示并行分支、依赖和异常 / show branches, dependencies, and exceptions |
| 自动选择轻路径 / Automatic lightweight path | 仅在影响时间、成本或产物时说明选择 / explain the choice when it affects time, cost, or output |

## 6. 评估取舍 / Evaluate tradeoffs

- 任务或节点增加后，总览是否仍可扩展？/ Does the overview scale as tasks or nodes grow?
- 装饰性视觉是否遮蔽状态和层级？/ Do decorative visuals obscure status or hierarchy?
- 折叠细节是否让风险过于隐蔽？/ Does hidden detail make risk too easy to miss?
- 多个视图是否保持同步？/ Do multiple views stay synchronized?
- 下钻后能否回到原来的上下文？/ Can users return to the exact prior context after drill-down?
- 键盘、减少动态效果和低视力场景是否可用？/ Is the design usable with keyboard navigation, reduced motion, and low vision?

不要根据静态图片宣称符合无障碍标准。说明哪些内容需要交互或实现测试。  
Do not claim accessibility compliance from a static image. State what requires interaction or implementation testing.

## 7. 区分策略与方案叙事 / Separate strategy from solution narration

- **为什么 / Why**：证据或假设 → 根本问题 → 体验目标 → 策略。
- **如何落地 / How**：页面或旅程 → 具体设计点 → 用户收益 → 验证信号。

不要在两个层级重复同一内容。/ Do not repeat the same content at both levels.

