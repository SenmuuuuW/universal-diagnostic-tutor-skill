# Codex 技能入口使用教程

Universal Diagnostic Tutor 的 Command Surface / Skill Entrypoints 使用说明

## 1. 现在 Codex 里能看到什么？

安装并同步后，Codex skill picker 里应该能看到：

- Tutor Visualize
- Tutor Exam Track
- Tutor State Card
- Tutor Study Plan
- Tutor Diagnose Gap
- Tutor Resource Scan
- Tutor Learn Anything
- Tutor Mistake Review
- Tutor Practice
- Universal Diagnostic Tutor

这些不是彼此独立的产品。它们是同一个 Universal Diagnostic Tutor system 的不同入口：
一个主入口，加上一组更聚焦的学习任务入口。

## 2. Main Skill 和 Tutor Entrypoints 的区别

`Universal Diagnostic Tutor` 是主 Skill / 总调度器，适合普通学习问题、概念讲解和综合诊断。

`Tutor *` 是细分入口，适合你已经知道自己想做什么，比如做学习计划、出题批改、错题分析、保存状态卡、找资源或用图理解。

简单说：主 Skill 像总老师，Tutor Study Plan / Tutor Exam Track 这些像不同办公室的门。你可以从总老师开始，也可以直接进对应办公室。

## 3. 什么时候用哪个？

| Codex 里显示的入口 | 适合什么时候用 | 典型问题 |
| --- | --- | --- |
| Universal Diagnostic Tutor | 不确定选哪个、普通概念/题目讲解 | “两个向量平行是什么意思？” |
| Tutor Learn Anything | 有一个很大的学习目标，不知道从哪里开始 | “我想学机器学习，但数学很弱。” |
| Tutor Study Plan | 想要学习计划、复习安排、短期路线 | “我想系统入门机器学习，给我一个学习计划。” |
| Tutor Exam Track | 大学理科/考研数学/CS 专业课备考 | “我高数级数判别法总不会选。” |
| Tutor Diagnose Gap | 不知道自己到底卡在哪个知识点 | “我看答案懂，自己做不会。” |
| Tutor Mistake Review | 已经做错了，想分析错因 | “我把平行向量理解成分量相等了。” |
| Tutor Practice | 练习 / 出题 / 批改 / 判答案 / 判断能否进阶 | “给我一道梯度下降基础题，做完后帮我批改。” |
| Tutor State Card | 想保存进度、跨 chat 继续学习 | “帮我生成下次继续用的学习状态卡。” |
| Tutor Resource Scan | 想找可信资源、课程、学习材料 | “我想系统补线代，有什么靠谱资源？” |
| Tutor Visualize | 需要图像、图表、流程图辅助理解 | “画图解释为什么矩阵乘法是变换。” |

## 4. 每个入口详细说明

### Universal Diagnostic Tutor

是什么：主 Tutor Skill / 总调度器。它会先判断学科、知识点、前置知识和当前卡点，再决定用解释、练习、错因分析、资源、图示还是状态卡。

什么时候用：你只是想问一道题、一个概念，或者不确定该选哪个 Tutor 入口。

不适合什么：不要把它当成只给最终答案的 homework bot，也不要期待它保存隐藏记忆。

示例 prompt：

```text
两个向量平行是什么意思？我学过向量但总是和分量相等搞混。
```

### Tutor Learn Anything

是什么：大目标学习入口。适合“我想学机器学习”“我想补线代”“我想学 AI/CS，但不知道从哪里开始”。

它会触发 V1.8 Learning Architecture：

```text
Goal Clarification -> Goal Confirmation -> Knowledge Map -> Learning Path -> First Step
```

示例 prompt：

```text
我想学机器学习，但是数学很弱。我会一点 Python，目标是能看懂基础模型和做小项目。你先帮我判断从哪里开始。
```

### Tutor Study Plan

是什么：学习计划入口。适合你已经有目标，想要一个短计划、复习安排或今天第一步。

V1.8.2 之后，Study Plan 应该是 discipline-first：先拆学科，再给路线。尤其是机器学习、AI/CS、数据科学、算法、线代、统计这类大目标，不能只写“Python、线代、概率、PyTorch”。

必须先拆：

```text
学科 -> 子知识点 -> 最低掌握标准 -> 暂时跳过 -> 顺序 -> 今天第一步
```

示例 prompt：

```text
我想系统入门机器学习，但数学基础比较弱。我会一点 Python，不是为了考试，是为了以后能看懂基础模型并做小项目。请给我一个学习计划。
```

### Tutor Exam Track

是什么：理科 / STEM / AI-CS 备考入口。它会诊断弱点、识别题型线索、修复前置知识、分析错因并安排练习顺序。

适合：

- 高数 / 微积分
- 线性代数
- 概率统计
- 离散数学
- 大学物理
- 数据结构
- 算法
- 计算机组成原理
- 操作系统
- 计算机网络
- 机器学习基础

不做：押题、作弊、泄题、保证提分、预测考试。

示例 prompt：

```text
我准备考研数学，线代很弱，先从哪里补？
```

### Tutor Diagnose Gap

是什么：知识缺口诊断入口。适合你感觉“看答案懂，自己做不会”，但不知道到底缺什么。

它会诊断：

- 概念缺口
- 符号缺口
- 前置知识缺口
- 方法缺口
- 证明缺口
- 迁移缺口
- 图像直觉缺口

示例 prompt：

```text
这道级数题我看答案懂，自己做不会。帮我判断我到底缺什么。
```

### Tutor Mistake Review

是什么：错因分析入口。它分析错误思路，而不是只告诉你正确答案。

它会看：表层错误是什么、底层误解是什么、为什么这个错法看起来合理、怎么修复、下一道相似题怎么避免。

示例 prompt：

```text
我把两个平行向量的每个分量都设成相等了，帮我分析错因。
```

### Tutor Practice

是什么：练习与掌握闭环入口。适合你想要针对当前知识点出题、提交答案、获得定性批改，或判断自己能不能进入下一步。

它通常一次只给一道针对性练习并等你作答。你回答后，它会保留正确部分、说明错误或缺失、分析错因，再根据证据决定继续练习、复习、降一步或进阶。只有强相关概念正在卡住当前任务时，才会补充 1–3 张简短 Knowledge Link Cards。

示例 prompt：

```text
给我出一道关于梯度下降的基础题，做完后帮我批改并判断我能不能继续。
```

也可以手动输入：

```text
/practice 我学完向量了，给我一道题检查掌握情况。
```

`/practice` 是 Tutor 的文字快捷方式，不保证是 Codex 原生 slash command。Codex skill picker 里能看到 Tutor Practice / `tutor-practice` 时，优先选择该入口。

### Tutor State Card

是什么：学习状态卡入口。适合你想保存当前学习状态，或者换 chat 后继续。

可以生成：

- Learning State Card
- Learner Profile Card
- Learning Task Card

重点：这不是隐藏记忆。它是用户可复制、可保存、可粘贴的学习状态。

示例 prompt：

```text
帮我生成一个下次继续学习机器学习时可以直接复制使用的 Learning State Card。
```

### Tutor Resource Scan

是什么：可信资源入口。它先做 topic scan，再给资源建议。

它不应该乱甩链接，也不应该编造来源。好的回答会先说明你要学的主题属于哪个学科 / 模块 / 核心概念，再说明什么资源适合补哪个缺口。

示例 prompt：

```text
我想系统补线性代数，尤其是向量、矩阵和矩阵乘法，有什么靠谱资源？
```

### Tutor Visualize

是什么：可视化理解入口。适合文字解释不够、你需要图像或结构来理解的时候。

适合：

- 函数图像
- 几何图
- 向量关系
- 矩阵变换
- 流程图
- 概念图
- 算法流程

它不会承诺不存在的真实图像工具。如果当前环境不能生成图片，它可以用文字图、表格、Mermaid 或简洁描述来辅助理解。

示例 prompt：

```text
帮我用图解释为什么两个向量平行不是每个分量相等。
```

## 5. 推荐使用顺序

如果你是大目标：

1. Tutor Learn Anything
2. Tutor Study Plan
3. Universal Diagnostic Tutor
4. Tutor Practice / Tutor Visualize / Tutor Diagnose Gap / Tutor Mistake Review
5. Tutor State Card

如果你是备考：

1. Tutor Exam Track
2. Tutor Diagnose Gap
3. Tutor Practice / Tutor Mistake Review
4. Tutor State Card

如果你只是问一个概念：

1. Universal Diagnostic Tutor
2. Tutor Visualize if needed
3. Tutor State Card if continuing later

## 6. Codex 里怎么调用？

在 Codex 里，优先从 skill picker 里选择可见的技能入口。你可能会看到这样的显示名：

- Tutor Study Plan
- Tutor Exam Track
- Tutor State Card
- Tutor Visualize
- Tutor Practice

不同 Codex UI 的显示方式可能不同，直接 slash 名称也可能不同。不要假设 `/study-plan` 或 `/learn-anything` 一定是 Codex 原生命令。

`/study-plan`、`/learn-anything` 和 `/practice` 仍然是 Tutor 能理解的文字快捷方式；如果你的 Codex 里已经能看到对应的 `tutor-*` 入口，优先直接选择该入口。

## 7. 普通聊天 AI 怎么办？

普通 ChatGPT / 豆包 / DeepSeek / Kimi / Qwen 聊天窗口不会显示这些 Codex skill picker entries。

普通聊天请使用 Lite Prompt：

- [USER_GUIDE.md](USER_GUIDE.md)
- [platforms/generic-chat/TUTOR_LITE_PROMPT.md](platforms/generic-chat/TUTOR_LITE_PROMPT.md)

复制 Lite Prompt 后，可以手动输入：

```text
/learn-anything ...
/study-plan ...
/exam-track ...
/state-card ...
/visualize ...
/practice ...
```

这些是 prompt shortcuts，不是普通聊天平台的真实菜单命令。

## 8. 常见问题

**为什么我看不到 Tutor Study Plan？**

检查 `skills/tutor-study-plan/` 是否已经同步到当前 Codex 实际读取的 skills 目录，例如：

```text
~/.codex/skills/tutor-study-plan/SKILL.md
```

只同步 `skills/universal-diagnostic-tutor/` 不够；V1.8.1+ 的入口还需要同步所有 `skills/tutor-*` 文件夹。同步后重启 Codex 或打开新 session。

**`/study-plan` 为什么不弹出？**

`/study-plan`、`/learn-anything` 和 `/practice` 是 Tutor 能理解的文字快捷方式，不一定是 Codex 原生命令。Codex 里如果已经显示对应的 Tutor 入口，请优先选择该入口。

**这些 skill 是不是彼此独立？**

不是。它们是同一个 Universal Diagnostic Tutor system 的薄入口，核心教学逻辑仍然共享。

**普通用户应该选哪个？**

如果不确定，选 Universal Diagnostic Tutor。目标很大、不知道从哪里开始时，选 Tutor Learn Anything。

**会不会有隐藏记忆？**

不会。跨 chat 继续学习请用 Tutor State Card 生成可复制的状态卡。

**能不能押题/保证提分？**

不能。Tutor Exam Track 做的是诊断、概念修复、题型识别和练习顺序，不做押题、作弊、泄题或提分保证。
