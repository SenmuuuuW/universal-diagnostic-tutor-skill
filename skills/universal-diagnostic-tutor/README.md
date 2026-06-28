# universal-diagnostic-tutor｜Skill 使用指南

`universal-diagnostic-tutor` 是一个诊断型智能导师 Skill。它让 AI 助手在学习场景中先判断学科、主题、前置知识和知识漏洞，再选择合适的解释、练习和反馈方式。

这个文件是 Skill 目录内的使用指南，重点说明什么时候使用这个 Skill、怎样提问、各类参考文件有什么作用，以及未来维护时应注意什么。

如果你是第一次了解这个项目，建议先看根目录的 [GitHub README](../../README.md)。根 README 更像项目 landing page；本文件更偏 Skill 使用和维护指南。

## Skill 名称

```text
universal-diagnostic-tutor
```

## 这个 Skill 做什么？

它定义一套可复用的 tutor behavior：

- 诊断学习问题属于哪个学科和主题。
- 判断学习者可能缺少的概念、词汇、符号、步骤、推理或迁移能力。
- 根据学习者状态决定直接解释、提问引导、降低难度、给练习或推进到迁移。
- 在当前对话内轻量跟踪学习进度，但不保存持久记忆。
- 用可靠资源辅助学习，同时保持“教学先于链接”。

它适用于所有学习相关问题，但当前最强的方向是大学层级 STEM / AI-CS：数学、编程、算法、AI / ML、系统、网络、物理、电子和信号等。

## 什么时候使用？

适合在这些场景使用：

- 用户想学懂一个概念，而不是只要最终答案。
- 用户说“我不懂”“还是没懂”“能不能讲简单点”。
- 用户给出错误答案、部分正确答案或自己的解题过程。
- 用户需要练习、复习、考试准备或迁移训练。
- 用户被符号、公式、证明、代码、系统抽象或资源选择卡住。
- 用户希望 AI 帮忙诊断自己到底缺哪块知识。

典型触发请求：

```text
请用诊断型导师方式教我。
```

```text
不要直接给答案，先帮我找出我哪里没懂。
```

```text
我做对了，但我说不出为什么。
```

## 什么时候不要使用？

不适合把它当成：

- 只输出答案的 homework bot。
- 固定课程路线图或大学培养方案生成器。
- 医疗、法律、金融、税务、安全等专业建议工具。
- 永久学习档案、数据库或记忆系统。
- 链接收集器、教材搬运器或答案库。
- 代码自动修复工具；如果涉及代码，也应解释 mental model 和 bug 原因。

如果用户明确要求极短回答，可以先给答案，再给最小必要理由，不必强行套完整教学模板。

## 主要教学行为

这个 Skill 要求 tutor 在回答前后持续做这些事：

- **诊断主题**：先判断是数学、编程、AI、系统、写作、法律常识、历史、文学等哪类问题。
- **诊断知识漏洞**：判断是 vocabulary gap、concept gap、notation gap、procedure gap、reasoning gap、recognition gap、transfer gap、misconception gap、confidence gap 还是 resource gap。
- **选择解释深度**：在超短、短答、标准解释和深入解释之间校准。
- **选择学习模式**：根据学习者状态使用零基础、普通、进阶或 Auto Mode。
- **先讲直觉**：尤其在 STEM 中，先给 mental picture、具体例子或物理 / 几何 / 计算意义。
- **解释符号和步骤**：说明公式、代码、图、单位或系统层级分别代表什么。
- **检查理解**：用一个小问题、teach-back、错误识别或近迁移题判断下一步。
- **控制节奏**：一次推进一个问题或子问题，在关键步骤停下来让学习者参与。
- **分析错误**：定位表层错误和底层误解，解释为什么错误路径看起来合理。
- **调整难度**：根据学习者表现增加、保持或降低抽象度、符号密度、步骤数和证明严谨度。
- **推进掌握**：从识别到理解、从带提示应用到独立应用，再到迁移。
- **主动找资源**：当环境有 web/search 能力且资源能改善教学时，搜索权威学习资源，并把资源转化成解释、练习、错题修复和考试题型分析。

## STEM / AI-CS 强项

这个 Skill 对这些技术学习场景有专门参考：

- 线性代数：矩阵、向量、变换、`Ax = b`、矩阵乘法意义。
- 微积分：导数、变化率、极限、推导、优化直觉。
- 算法：不变量、正确性证明、复杂度、模式识别。
- 编程：递归、循环、状态、调试、代码 trace。
- AI / ML：数据、模型、loss、gradient、参数更新、线性代数和微积分桥接。
- 系统：虚拟内存、进程、地址转换、抽象层、保护和隔离。
- 物理 / 电子 / 信号：传感、采样、量化、滤波、频域和时域关系。

## 如何问出更好的问题？

好的问题可以告诉 tutor 你的当前状态：

- “我知道定义，但不知道什么时候用。”
- “我能跟着例题做，但自己做不出来。”
- “我不懂这个符号代表什么。”
- “我答案对了，但不知道为什么。”
- “我又犯了同样的错。”
- “请先用简单例子讲，再给正式定义。”
- “请给我从识别到迁移的练习梯度。”

你不需要完美描述问题。这个 Skill 的目的就是让 tutor 帮你诊断。

## 示例提示词

```text
我不懂 Ax = b 里的 b 是点还是向量。请先解释符号，不要直接解方程。
```

```text
为什么 x^2 的导数是 2x？请解释推导过程里每一步为什么成立。
```

```text
我知道 binary search 的代码，但不懂为什么它一定能找到目标。
```

```text
我的 Python loop 打印出了正确数字，但是最后 list 还是空的，帮我理解原因。
```

```text
我能跟着写递归，但独立写会卡住。请给我一个练习梯度。
```

```text
我这道条件概率又错了，请分析我是概念错、公式错，还是识别错。
```

```text
我现在没时间练习，请先给我短答案和最关键的一句原因。
```

## 🎚️ 选择你的学习模式

你可以先告诉导师你希望用哪种模式学习：

- 🌱 **零基础模式**：适合完全没学过，需要从概念、符号、例子讲起。
- 📘 **普通模式**：适合学过一点，但不会做题或不会判断方法。
- 🚀 **进阶模式**：适合有基础，想要更快、更严谨、更深入。
- **Auto Mode**：如果你不选择，导师会根据你的问题、用词、错误和信心自动判断；不确定时会问一个很短的问题。

可复制示例：

```text
我是零基础，请从概念和符号开始讲。
```

```text
我学过一点，请用普通模式一步一步带我做。
```

```text
我有基础，请用进阶模式讲核心思路和证明。
```

```text
如果我答不出来，请自动降低难度。
```

```text
问我问题后请停下来，等我回答再继续。
```

## 🧮 数学公式显示

数学公式应显示成数学，而不是代码块。普通代数、微积分、线性代数、概率和证明步骤应优先使用 Markdown / LaTeX math，例如 $Ax=b$ 或：

$$
\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}
$$

代码块只用于真正的代码、命令、路径，或必须保留空格的 literal text。

## 目录里的文件有什么用？

### `SKILL.md`

Skill 的核心入口。它包含触发说明、诊断优先工作流、教学深度、主题模式、输出格式路由、参考文件路由和守则。维护时应保持简洁，不把所有细节塞进这里。

### `references/`

详细教学协议和维护资料。常用文件包括：

- `adaptive_teaching_engine.md`：自适应教学总枢纽。
- `teaching_mode_selection_protocol.md`：选择 Auto、零基础、普通或进阶教学模式。
- `beginner_foundation_teaching_protocol.md`：真正零基础学习者的概念、符号和对象解释。
- `standard_and_advanced_mode_protocol.md`：区分普通问题讲解与进阶证明、推导、边界和迁移。
- `math_formatting_protocol.md`：数学公式使用 Markdown / LaTeX math，不用代码块伪装公式。
- `user_mode_onboarding_guide.md`：面向用户的学习模式选择提示。
- `interaction_pacing_protocol.md`：防止一次讲太多，保持 teach-check-continue 节奏。
- `teacher_like_stop_point_protocol.md`：定义什么时候停下来让学习者参与关键步骤。
- `knowledge_gap_taxonomy.md`：知识漏洞分类。
- `multiturn_tutoring_protocol.md`：多轮对话处理。
- `practice_ladder.md`：从识别到迁移的练习梯度。
- `mistake_analysis_protocol.md`：错题分析。
- `stem_teaching_sequence.md`：STEM 从直觉到形式化的教学顺序。
- `stem_ask_vs_explain_calibration.md`：什么时候问、什么时候直接讲。
- `stem_symbol_notation_protocol.md`：符号、公式、对象类型和记号解释。
- `stem_proof_and_derivation_protocol.md`：证明和推导教学。
- `stem_problem_solving_protocol.md`：STEM 解题、建模、调试和算法问题处理。
- `mastery_state_protocol.md`：当前对话内的掌握状态判断。
- `cross_turn_progress_protocol.md`：跨轮进度跟踪。
- `understanding_check_protocol.md`：支持性的理解检查。
- `difficulty_adjustment_protocol.md`：难度调整。
- `review_or_advance_decision.md`：复习、换解释、练习或推进的决策。
- `resource_integration_protocol.md`：资源支持式教学。
- `autonomous_resource_discovery_protocol.md`：有 web/search 能力时主动寻找权威学习资源。
- `resource_orchestrated_tutoring_protocol.md`：把搜索、source packs 或用户材料编排成教学，而不是链接列表。
- `exam_pattern_resource_analysis.md`：分析常见考试题型、陷阱、识别 cue 和练习方向。
- `skill_vs_generic_ai_advantage.md`：说明本 Skill 相比普通 AI 答案的诊断、节奏、资源和掌握优势。
- `source_trust_hierarchy.md`：资源可信度层级。
- `evaluation_checklist.md` 和 `manual_test_matrix.md`：人工验收和测试。

### `references/source_packs/`

轻量资源包，用于 STEM / AI-CS 学习资源选择。它们只记录资源名称、用途、可信度、注意事项和适用场景，不复制教材、不保存 PDF、不作为答案库。

### `examples/`

示例回答和教学场景，用来展示 Skill 的理想行为。未来新增示例时，应保持短、具体、可代表真实学习场景，并包含诊断、教学动作和检查或练习。

## 维护注意事项

- 保持 Skill 通用，不要改成只服务数学、CS、AI 或某个考试。
- STEM / AI-CS 是当前重点，但不是唯一范围。
- 不要把 source packs 变成教材库、链接堆或课程地图。
- 保留学习模式校准：不要假设零基础学习者懂符号，也不要让进阶学习者被不必要的基础解释拖慢。
- 可以根据学习者回答切换模式，但不要过度暴露模式标签。
- 数学公式不要放进代码块；代码块只用于真正的代码、命令、路径或 literal text。
- 不要假设用户会上传材料；如果有 web/search 能力且资源有帮助，可以主动搜索权威学习资源。
- 使用资源时要编排进教学，不要堆链接，也不要编造资源或引用。
- 如果学习者要求不要直接给答案，至少保留一个有意义的步骤让学习者完成。
- 不要加入网站、脚本、API、包管理、数据库、持久记忆或基础设施。
- 不要让 mastery-state tracking 变成评分表或学习者标签系统。
- 维护 `SKILL.md` 时保持 routing-oriented；复杂细节放到 `references/`。
- 修改教学行为时，同时更新示例、评估清单和人工测试矩阵。
- 可用 `evaluation_checklist.md` 和 `manual_test_matrix.md` 做人工验收。
- 如果外部 `quick_validate.py` 因缺少 PyYAML 无法运行，不要为此在本仓库新增 package setup；可在本地环境安装依赖或使用已有 YAML 工具验证 front matter。

## V1.2 说明

V1.2 增加学习模式校准、零基础教学、普通/进阶模式区分和数学公式显示规范。它仍然保留 V1.1 的 teach-check-continue 节奏和关键停顿点，并且仍是 Markdown-only 教学行为更新，不新增网站、脚本、API、包管理、数据库、持久记忆、真实 RAG / vector database、PDF、课程地图或新 source packs。

## V1.2.1 说明

V1.2.1 只轻量打磨根目录 GitHub README 的展示效果、中文可读性、学习模式入口和新用户 onboarding。本 Skill 的核心行为、教学协议、示例体系和资源规则不变。
