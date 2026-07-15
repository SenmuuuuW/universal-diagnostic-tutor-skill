# Codex 技能入口使用教程

[English README](README.md) | [中文 README](README.zh-CN.md)

V1.9.2 将 Universal Diagnostic Tutor 的公开 Command Surface 收敛为 6 个入口。
能力没有删除，只是把相近任务合并到更容易记住的入口。

## 1. 六个公开入口

1. Universal Diagnostic Tutor
2. Tutor Learn Path
3. Tutor Practice
4. Tutor State Card
5. Tutor Resource Scan
6. Tutor Visualize

它们不是六套独立产品，而是进入同一套 Tutor System 的六扇门。主 Skill 负责
通用教学，其他入口帮助 Codex 更快识别当前意图。

| 你的需求 | 选择 | 示例 |
| --- | --- | --- |
| 不确定入口，或一般 STEM / AI-CS 学习问题 | Universal Diagnostic Tutor | “我是零基础，矩阵乘法到底在做什么？” |
| 学一个大主题、做学习计划或安排备考路线 | Tutor Learn Path | “我想从零学机器学习，帮我安排三个月路线。” |
| 练题、批改、错因分析、卡点诊断或判断能否进阶 | Tutor Practice | “给我一道链式法则题，做完帮我分析。” |
| 保存进度、跨 chat 继续或生成学习摘要 | Tutor State Card | “帮我生成下次继续用的状态卡。” |
| 找可信课程、文档、教材或 topic scan | Tutor Resource Scan | “我想补线代，有哪些靠谱资源？” |
| 用图、表、流程或空间结构理解概念 | Tutor Visualize | “画图解释两个向量为什么平行。” |

## 2. Universal Diagnostic Tutor

**适合：** 不知道选哪个入口，或直接提出一个学习问题。

它会判断学科、知识点、前置知识和当前卡点，再选择最小但最有价值的下一步。

```text
我是零基础，不懂 Ax=b 里的 b 是什么。请先解释对象和符号。
```

拿不准时始终可以选它。

## 3. Tutor Learn Path

**适合：** 大目标、学习路线、学习计划、系统学习、备考路线和复习安排。

它合并了过去 Tutor Learn Anything、Tutor Study Plan 和 Tutor Exam Track 中的
规划能力。它会先确认目标与基础，再给小型知识地图、现实顺序、第一步和检查点，
不会默认生成庞大课程表。

```text
我会一点 Python，但数学弱，想系统入门机器学习。请给我一条可开始的学习路线。
```

```text
我三个月后考研数学，线代薄弱，帮我安排复习顺序和本周第一步。
```

## 4. Tutor Practice

**适合：** 练习、出题、批改、判答案、错因分析、知识缺口诊断、备考练习和
readiness 判断。

它合并了过去 Tutor Diagnose Gap、Tutor Mistake Review 和 Tutor Exam Track 中的
练习与复盘能力。默认一次给一道针对性练习，等待作答后再定性批改、修复卡点并
决定进阶、复习、降一步或继续练习。

```text
我刚学导数，先给我一道基础题。等我作答后再批改和判断能不能继续。
```

```text
这是我的错误解法。请保留正确部分，分析第一个关键错误，再给一道近迁移题。
```

它不会声称官方分数、预测考试、保证提分、使用泄题材料或押题。

## 5. Tutor State Card

**适合：** 保存当前学习状态、跨 chat 继续、handoff 或进度摘要。

状态卡是用户可见、可复制的短摘要，不是隐藏记忆或数据库。

```text
帮我生成一张学习状态卡，下次从链式法则漏乘内层导数这个卡点继续。
```

## 6. Tutor Resource Scan

**适合：** 查找课程、官方文档、教材方向、练习资源或快速定位知识主题。

它应该说明资源为什么适合当前阶段，而不是只堆链接。无法搜索时也不能假装已经
验证过链接。

```text
我想系统补线性代数，请推荐适合初学者的可信课程和练习方向。
```

## 7. Tutor Visualize

**适合：** 用函数图、向量图、流程图、概念图、trace table 或清晰的文字图像
理解结构关系。

```text
用一个简单图示解释矩阵乘法为什么可以看成空间变换。
```

可视化只服务当前卡点，不代表平台一定有真实绘图工具。

## 8. 旧入口现在怎么用？

如果你在旧截图、旧教程或复制版 Skill 中看到以下名称，请按这张表选择：

| 旧入口 | 现在使用 |
| --- | --- |
| Tutor Learn Anything | Tutor Learn Path |
| Tutor Study Plan | Tutor Learn Path |
| Tutor Exam Track | 规划路线用 Tutor Learn Path；刷题、复盘用 Tutor Practice |
| Tutor Diagnose Gap | Tutor Practice |
| Tutor Mistake Review | Tutor Practice |

旧能力没有删除。V1.9.2 只移除了重复的公开 wrapper folders，底层教学协议仍由主
Tutor System 使用。

## 9. 文字快捷方式仍然可用

这些 slash-style 名称是手动输入的意图提示，不保证是 Codex 或其他平台的原生
slash command：

| 文字别名 | 路由到 |
| --- | --- |
| `/tutor` | Universal Diagnostic Tutor |
| `/learn-anything`, `/study-plan` | Tutor Learn Path |
| `/exam-track` | 规划用 Tutor Learn Path；练习或复盘用 Tutor Practice |
| `/practice`, `/mistake-review`, `/diagnose-gap` | Tutor Practice |
| `/state-card` | Tutor State Card |
| `/resource-scan` | Tutor Resource Scan |
| `/visualize` | Tutor Visualize |

普通聊天用户可以继续手动输入这些别名；Codex skill picker 中只推广六个 canonical
entrypoints。

## 10. 普通聊天 AI 怎么用？

普通 ChatGPT、Gemini、DeepSeek、豆包、Kimi 或 Qwen 通常不会显示这些 Skill
入口。请复制 [Lite Prompt](platforms/generic-chat/TUTOR_LITE_PROMPT.md)，然后用
自然语言或上述文字别名表达需求。

不要把文字别名理解成菜单、CLI 或平台原生命令。

## 11. 常见问题

**不知道选哪个怎么办？**

选 Universal Diagnostic Tutor。

**为什么更新后少了几个 Tutor 入口？**

V1.9.2 主动将十个公开入口合并为六个，减少选择负担。旧入口对应的能力仍在 Learn
Path、Practice 和主 Tutor 中。

**为什么看不到 Tutor Learn Path？**

确认 `skills/tutor-learn-path/SKILL.md` 和其余 canonical `skills/tutor-*` folders
已经同步到 Codex 实际读取的 skills 目录，然后新开 session 重新加载。

**Tutor Practice 能做错因分析和卡点诊断吗？**

能。它现在统一处理练习、批改、错误复盘、知识缺口诊断和 readiness。

**Tutor Learn Path 能做备考规划吗？**

能。备考路线和复习顺序由 Learn Path 处理；具体练习和错题复盘由 Practice 处理。

**这些入口会自动记住我的学习状态吗？**

不会。跨 chat 继续请使用 Tutor State Card，并在新 chat 粘贴可见卡片。
