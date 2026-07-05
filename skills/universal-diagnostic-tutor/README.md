# universal-diagnostic-tutor｜Skill 使用指南

`universal-diagnostic-tutor` 是一个诊断型智能导师 Skill，当前最适合大学理科 / STEM / AI-CS 学习场景。它让 AI 助手先判断学科、知识系统、主题、前置知识和知识漏洞，再选择合适的解释、练习和反馈方式。

这个文件是 Skill 目录内的使用指南，重点说明什么时候使用这个 Skill、怎样提问、各类参考文件有什么作用，以及未来维护时应注意什么。

如果你是第一次了解这个项目，建议先看根目录的 [GitHub README](../../README.md)。根 README 更像项目 landing page，包含平台概览、Core Reasoning Flow 和质量评估入口；本文件更偏 Skill 使用和维护指南。

想快速看效果，可以先看根目录 [EXAMPLES.md](../../EXAMPLES.md)。

安装和更新请看根目录的 [INSTALL.md](../../INSTALL.md)。这个 Skill 目录本身是 `skills/universal-diagnostic-tutor/`。

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

它主要面向大学层级 STEM / AI-CS：数学、编程、算法、AI / ML、系统、网络、物理、电子、信号和工程基础等。它仍保留跨学科诊断式教学能力，但不应被介绍成泛泛的全科答题助手。

## 兼容性说明

这个目录是 Markdown-based Skill directory，主要面向 Codex-style Skill workflow。Claude Code-style agents 或其他支持 project instructions / custom instructions 的 agent 可以参考适配。普通网页聊天环境可以手动复制提示词或核心说明，但通常不会自动加载 `references/` 和 `examples/`。

非 agent 平台请看根目录 [PORTABILITY.md](../../PORTABILITY.md) 和 [platforms/](../../platforms/)。本 README 说明的是完整 Skill 版本；Lite Prompt、Custom GPT、Gemini Gem、Coze / 豆包和 API prompt 是下游适配包，能力通常弱于完整 Skill。

## V1.7 Skill Pack 用法

V1.7 增加了短的 user-invoked flows，方便学习者在普通聊天或 Full Skill 环境里快速表达意图。这些 slash-style 名称是提示词约定，不是命令行工具：

- `/tutor`：开始诊断式教学。
- `/diagnose-gap`：先判断缺哪个概念、符号、方法或推理。
- `/study-plan`：根据当前状态和目标生成短学习计划。
- `/exam-track`：进入 STEM Exam Track / 理科备考 Track。
- `/state-card`：生成或继续使用 Learning State / Profile / Task Cards。
- `/resource-scan`：先定位知识点，再在有用时推荐可信资源。
- `/visualize`：用简单图示、表格、流程图或概念图辅助理解。
- `/mistake-review`：分析错因并映射到针对性修复。

这些流程不应让普通回答变成模板。Tutor 仍然要保持自然教师表达、next-best-step、teach-check-stop、数学格式和无内部泄漏。

## Related sub-skill entrypoints

V1.8.1 增加了轻量 `tutor-*` folders，方便 Codex-style skill discovery。它们不是
独立产品，也不复制完整主 Skill；它们只是进入同一套 Tutor System 的 focused doors。

- `../tutor-learn-anything/`：大目标学习入口。
- `../tutor-study-plan/`：短学习计划入口。
- `../tutor-exam-track/`：STEM / 理科备考入口。
- `../tutor-state-card/`：Learning State / Profile / Task Cards 入口。
- `../tutor-resource-scan/`：Topic scan + trusted resources 入口。
- `../tutor-visualize/`：简单学习可视化入口。
- `../tutor-mistake-review/`：错因分析入口。
- `../tutor-diagnose-gap/`：知识缺口诊断入口。

完整 command surface 说明见根目录 [COMMAND_SURFACE.md](../../COMMAND_SURFACE.md)。

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

- **诊断主题**：先判断学科 -> 知识系统 -> 子主题 -> 核心概念，例如离散数学 -> 图论 -> 边染色，或线性代数 -> 向量 / 矩阵 / 线性方程组。
- **诊断知识漏洞**：判断是 vocabulary gap、concept gap、notation gap、procedure gap、reasoning gap、recognition gap、transfer gap、misconception gap、confidence gap 还是 resource gap。
- **选择解释深度**：在超短、短答、标准解释和深入解释之间校准。
- **选择学习模式**：根据学习者状态使用零基础、普通、进阶或 Auto Mode。
- **先讲直觉**：尤其在 STEM 中，先给 mental picture、具体例子或物理 / 几何 / 计算意义。
- **解释符号和步骤**：说明公式、代码、图、单位或系统层级分别代表什么。
- **检查理解**：用一个小问题、teach-back、错误识别或近迁移题判断下一步。
- **控制节奏**：一次推进一个问题或子问题，在关键步骤停下来让学习者参与。
- **优化下一步**：选择当前最小但最有价值的教学动作，而不是一次讲完所有背景。
- **跨聊天接续**：如果学习者要稍后继续，生成或使用 Learning State Card，而不是依赖隐藏记忆。
- **管理认知负荷**：根据零基础、普通或进阶状态控制每轮新概念、符号和证明密度。
- **解释掌握信号**：把学习者的正确、错误、猜测、部分正确或困惑回应转化成下一步教学决策。
- **压缩已知内容**：如果学习者已经知道某个前置知识，就简短带过，把时间用在真正的卡点上。
- **分析错误**：定位表层错误和底层误解，解释为什么错误路径看起来合理。
- **调整难度**：根据学习者表现增加、保持或降低抽象度、符号密度、步骤数和证明严谨度。
- **推进掌握**：从识别到理解、从带提示应用到独立应用，再到迁移。
- **主动找资源**：当环境有 web/search 能力且资源能改善教学时，搜索权威学习资源，并把资源转化成解释、练习、错题修复和考试题型分析。
- **Topic Scan + Trusted Resources**：对较大的 STEM / AI-CS 问题先简短定位 subject -> module -> concept -> prerequisite，再决定是否需要资源。
- **Brief Study Plan**：当学习者有当前状态和目标时，给短计划，不输出庞大课程路线图。
- **STEM Exam Track**：支持大学理科、考研数学和 CS 专业课复习，强调概念修复、题型识别、错因分析和练习顺序，不承诺分数或押题。
- **可视化辅助**：当文字不够时，用简单图示、表格、Mermaid、trace table 或概念图帮助理解，但不为了好看而画图。
- **自然教师表达**：普通教学回答不暴露 Skill 名称、版本号、协议名或内部文件，而是直接像老师一样讲。
- **知识系统映射**：用简短语言说明题目属于哪个领域、子主题、核心概念和前置知识。
- **迁移线索**：在合适时提炼“以后遇到类似题该看什么线索”。
- **学习架构**：对“我想学机器学习”“我想补线代”这类大目标，先澄清目标、确认方向、建小知识地图，再选择第一步和对应子流程。

## V1.8 Learning Architecture 用法

V1.8 把完整 Skill 理解为一个 Learning Orchestrator：先判断学习者到底想学什么，再决定下一步该调用哪个子流程。它不是课程生成器，也不是长期数据库。

适用场景：

- 用户给出很大的学习目标。
- 用户想补基础，但没有说清是考试、项目还是一般学习。
- 用户想知道一个概念在更大知识结构中的位置。
- 用户已经学了一个节点，但相关节点是否掌握还不确定。

推荐流程：

```text
Goal Clarification -> Goal Confirmation -> Knowledge Map -> Learning Path
-> Sub-skill Routing -> Mastery Check -> State Update
```

普通教学时不要暴露这些内部名称；用自然老师语言问 1-3 个关键问题，确认目标，然后给第一步。

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
我是零基础，请先判断这题属于哪个领域，再从概念和符号开始讲。
```

```text
请先告诉我这是离散数学、线性代数、微积分还是机器学习里的什么知识点。
```

```text
请先告诉我这题属于哪个领域和知识点。
```

```text
我是零基础，请先把符号翻译成人话。
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

```text
数学公式不要用代码块，请用正常公式格式。
```

```text
讲完这个小步骤后，请告诉我以后遇到类似题该看什么线索。
```

```text
不要提工具或版本，直接像老师一样教我。
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

数学公式应显示成数学，而不是代码块。普通代数、微积分、线性代数、概率和证明步骤应优先使用 Markdown / LaTeX math。面向学习者的回答推荐使用 `\(...\)` 和 `\[...\]`，例如 \(Ax=b\) 或：

\[
\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}
\]

代码块只用于真正的代码、命令、路径，或必须保留空格的 literal text。

## 目录里的文件有什么用？

### `SKILL.md`

Skill 的核心入口。它包含触发说明、诊断优先工作流、教学深度、主题模式、输出格式路由、参考文件路由和守则。维护时应保持简洁，不把所有细节塞进这里。

### `references/`

详细教学协议和维护资料。常用文件包括：

- `skill_pack_invocation_protocol.md`：`/tutor`、`/study-plan`、`/exam-track` 等 user-invoked flows 的调用约定。
- `learning_orchestrator_architecture.md`：V1.8 主编排层，连接目标澄清、知识地图、路径选择、子流程和状态更新。
- `goal_clarifier_protocol.md`：大目标、弱基础、考试或项目目标的短澄清问题。
- `goal_confirmation_loop_protocol.md`：澄清后先确认目标，再开始建路径。
- `knowledge_map_builder_protocol.md`：小而目标相关的知识地图，不生成庞大课程图。
- `learning_path_selector_protocol.md`：根据目标、基础、紧迫度和掌握信号选择下一步。
- `concept_mastery_map_protocol.md`：区分 explained、practiced、checked、confirmed、unconfirmed、weak 和 blocked，避免过早假设掌握。
- `adaptive_teaching_engine.md`：自适应教学总枢纽。
- `skill_routing_architecture.md`：维护和评估 Skill 内部路由层次，帮助 agent 选择最小相关协议集。
- `trigger_mode_matrix.md`：把常见用户信号映射到教学模式、协议和应避免行为。
- `learning_efficiency_optimization_loop.md`：选择最小高价值下一步，降低不必要认知负荷。
- `next_best_teaching_step_protocol.md`：判断下一步该教概念、符号、方法线索、设置、证明枢纽还是误解修复。
- `cognitive_load_budget_protocol.md`：按学习模式控制每轮解释量。
- `mastery_signal_interpretation_protocol.md`：把学习者回应解释成推进、迁移、压缩、重讲或降难度的信号。
- `explanation_compression_protocol.md`：学习者已懂前置知识时避免重复讲解。
- `error_to_intervention_protocol.md`：把错误类型映射到对应干预方式。
- `learning_state_card_protocol.md`：生成可复制的学习状态卡，用于稍后或跨 chat 继续学习。
- `context_handoff_protocol.md`：从 Learning State Card 或简短摘要继续，不从零重讲。
- `context_compression_checkpoint_protocol.md`：把长对话压缩成可继续的学习 checkpoint。
- `stateless_recovery_protocol.md`：没有上下文时快速重新定位，而不假装记得旧 chat。
- `learner_profile_task_card_protocol.md`：可复制的 Learner Profile Card 和 Learning Task Card，保持可见、用户控制、无隐藏记忆。
- `student_facing_response_protocol.md`：让普通教学回答像自然老师，而不是协议或工具执行记录。
- `no_internal_tool_leakage_protocol.md`：避免在教学回答里暴露 Skill、版本、文件或协议等内部细节。
- `knowledge_system_mapping_protocol.md`：把题目简洁定位到领域、子主题、核心概念和前置知识。
- `intuition_application_bridge_protocol.md`：把抽象 STEM 概念连到直觉、现象、技术系统或应用。
- `transfer_pattern_teaching_protocol.md`：讲完步骤后提炼可迁移的问题线索、方法和陷阱。
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
- `topic_scan_trusted_resources_protocol.md`：简短 topic scan 和可信资源建议，不把每个回答变成资源列表。
- `brief_study_plan_protocol.md`：根据当前状态和目标生成短学习计划。
- `stem_exam_track_protocol.md`：STEM Exam Track / 理科备考 Track，覆盖大学理科、考研数学和 CS 专业课复习。
- `basic_stem_visualization_protocol.md`：函数图、向量图、流程图、概率树、trace table 等基础 STEM 可视化指导。
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
- `evaluation_checklist.md` 和 `manual_test_matrix.md`：人工验收和测试。根目录的 [EVALS.md](../../EVALS.md)、[QUALITY_RUBRIC.md](../../QUALITY_RUBRIC.md)、[FAILURE_TAXONOMY.md](../../FAILURE_TAXONOMY.md) 和 [FEEDBACK_TO_IMPROVEMENT.md](../../FEEDBACK_TO_IMPROVEMENT.md) 用于更系统的质量评估和改进。

### `references/source_packs/`

轻量资源包，用于 STEM / AI-CS 学习资源选择。它们只记录资源名称、用途、可信度、注意事项和适用场景，不复制教材、不保存 PDF、不作为答案库。

### `examples/`

示例回答和教学场景，用来展示 Skill 的理想行为。未来新增示例时，应保持短、具体、可代表真实学习场景，并包含诊断、教学动作和检查或练习。

## 维护注意事项

- 保持 Skill 通用，不要改成只服务数学、CS、AI 或某个考试。
- STEM / AI-CS 是当前重点；保留跨学科能力，但不要把 Skill 主要描述成泛泛的全科助手。
- STEM tutoring should usually begin with a short domain diagnosis: subject ->
  knowledge system -> subtopic -> core concept.
- 普通教学回答不要暴露 Skill 名称、版本号、协议名、文件名或仓库内部细节；除非用户明确问项目本身。
- 用知识系统映射来帮助学习者定位，不要把一个题目扩展成很长的课程路线图。
- 抽象 STEM 概念需要时加入直觉 / 应用桥梁，但不要让应用喧宾夺主。
- 学习者完成一个检查或小步骤后，适当提炼迁移线索：看什么 clue、用什么 method、避开什么 trap。
- 不要用“讲更多”解决所有问题；如果更小的干预能解决，就优先选择下一步最有效教学动作。
- 把学习者回应当作掌握信号，判断应该推进、迁移、压缩解释、换讲法还是降难度。
- 学习者已经掌握的前置知识要压缩处理；只在证据显示薄弱时局部修复。
- 错误反馈要按错误类型选择干预方式，不要每次都泛泛重讲。
- 不要把 source packs 变成教材库、链接堆或课程地图。
- Slash-style flows 是用户意图快捷方式，不是 shell commands，也不代表平台真的实现了命令系统。
- Learner Profile / Task Cards 必须可见、可复制、由用户控制；不要暗示隐藏持久记忆。
- STEM Exam Track 不得承诺提分、预测考试、押题、使用泄露材料或帮助作弊。
- Topic Scan 要短；资源只在有用时加入，不要把每次回答变成资料列表。
- 可视化必须服务当前学习缺口，不要为了装饰而添加图。
- V1.8 是学习架构层，不是 assignment generation、grading、course
  generation、真实 graphing tools、数据库或隐藏记忆系统。
- 大目标要先澄清并轻量确认；知识地图要小、目标相关、服务下一步。
- 不要因为解释了一个节点，就把后续节点标成已掌握；需要证据和检查。
- 优先路由到已有子流程，不要把所有子流程塞进一个回答。
- 保留学习模式校准：不要假设零基础学习者懂符号，也不要让进阶学习者被不必要的基础解释拖慢。
- 可以根据学习者回答切换模式，但不要过度暴露模式标签。
- 数学公式不要放进代码块；面向学习者的数学优先使用 `\(...\)` 和 `\[...\]`，避免 raw `$...$`；代码块只用于真正的代码、命令、路径或 literal text。
- 零基础模式下先解释对象和符号，再进入证明、定理或完整解法；每次最多引入一两个新概念，然后提问并停下等回答。
- 不要假设用户会上传材料；如果有 web/search 能力且资源有帮助，可以主动搜索权威学习资源。
- 使用资源时要编排进教学，不要堆链接，也不要编造资源或引用。
- 如果学习者要求不要直接给答案，至少保留一个有意义的步骤让学习者完成。
- 不要加入网站、脚本、API、包管理、数据库、持久记忆或基础设施。
- 不要让 mastery-state tracking 变成评分表或学习者标签系统。
- 维护 `SKILL.md` 时保持 routing-oriented；复杂细节放到 `references/`。
- 不要把 `SKILL.md` 写成所有协议的复制版；优先提升路由清晰度，而不是堆叠新规则。
- 学习者要跨聊天继续时，使用 Learning State Card；不要暗示 agent 有隐藏记忆或持久学习档案。
- 对重复出现的失败，补 eval case，再做最小协议、示例或文档改动。
- 修改教学行为时，同时更新示例、评估清单和人工测试矩阵。
- 可用 `evaluation_checklist.md` 和 `manual_test_matrix.md` 做人工验收。
- 如果外部 `quick_validate.py` 因缺少 PyYAML 无法运行，不要为此在本仓库新增 package setup；可在本地环境安装依赖或使用已有 YAML 工具验证 front matter。

## 如何更新 Skill

完整步骤见根目录 [INSTALL.md](../../INSTALL.md)。如果你已经 clone 过仓库，通常只需要在仓库目录运行 `git pull`，然后用 `git log --oneline -1` 确认最新 commit。

如果你把 `skills/universal-diagnostic-tutor/` 复制到了另一个 agent 的 skills 目录，`git pull` 只会更新仓库副本，不会自动更新那个复制版。请把更新后的 `skills/universal-diagnostic-tutor/` 同步到 agent 实际读取的位置。

如果更新后 agent 仍然使用旧行为，建议重启或新开一个 agent session，让它重新加载最新 Skill instructions。

## 版本与变更

本文件说明当前 Skill 的使用方式，不重复完整版本历史。详细变更见根目录 [CHANGELOG.md](../../CHANGELOG.md)。

| Version | Focus |
| --- | --- |
| V1.8.x | Learning architecture: goal clarification, compact maps, path selection, and concept mastery maps |
| V1.7.x | Skill-pack invocations, STEM Exam Track, topic scan, cards, and visual learning |
| V1.6.x | Cross-platform prompt adapters and README / portability polish |
| V1.5.x | Skill reliability, evals, failure taxonomy, and Learning State Cards |
| V1.4.x | Learning Efficiency Optimization Loop and next-best-step tutoring |
| V1.3.x | Teacher-like response style, no internal leakage, and transfer bridges |
| V1.2.x | Teaching modes, math formatting, STEM-first positioning |
| V1.1.x and earlier | Pacing, adaptive tutoring, source support, examples, and evaluation foundations |
