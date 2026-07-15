<div align="center">

# 🧠 Universal Diagnostic Tutor Skill

**一个 diagnosis-first 的 STEM / AI-CS 学习 Tutor Skill：先判断你卡在哪里，再决定下一步教什么。**

[English](README.md) | 中文

[新手教程](USER_GUIDE.md) · [技能入口](COMMAND_SURFACE.md) · [使用示例](EXAMPLES.md) · [更新记录](CHANGELOG.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-2f6f4e.svg)](LICENSE)
![Markdown only](https://img.shields.io/badge/Markdown-only-555555.svg)
![Focus: STEM and AI-CS](https://img.shields.io/badge/Focus-STEM%20%2F%20AI--CS-1f6feb.svg)
![V1.9 Practice and Mastery](https://img.shields.io/badge/V1.9-Practice%20%26%20Mastery-b78300.svg)
[![GitHub stars](https://img.shields.io/github/stars/SenmuuuuW/universal-diagnostic-tutor-skill?style=flat)](https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill/stargazers)

</div>

Universal Diagnostic Tutor Skill 是一个 Markdown-only 的 AI Tutor 行为层，
重点面向大学理科、数学、编程、AI/CS 和备考复习。它先诊断学习者当前的知识
缺口，再选择最值得推进的一小步，并在进阶前检查真实掌握证据。

> **它不直接甩答案。** Tutor 会先判断学科、知识点、前置知识、符号、方法或
> 推理缺口，再选择紧凑的教学动作。它不是课程平台、数据库、RAG 系统或隐藏
> 记忆服务。

## 它适合谁

- 正在学习 STEM、大学理科或 AI-CS 的学生与自学者。
- 学习数学、编程、算法、机器学习、系统、网络、物理或信号的人。
- 准备大学理科考试、考研数学或 CS 专业课复习的人。
- 不想让 AI 只给最终答案，而希望被一步步带着理解和练习的人。

当前资料和评估覆盖最强的是微积分、线性代数、概率、离散数学、编程、算法、
机器学习、系统、网络、物理、信号与工程基础。它仍保留跨学科诊断教学能力，
但不把自己包装成泛泛的全科答题助手。

## 从哪里开始

| 我想做什么 | 去哪里 |
| --- | --- |
| 从零开始使用 | [新手教程](USER_GUIDE.md) |
| 选择 Tutor 入口 | [技能入口说明](COMMAND_SURFACE.md) |
| 在普通聊天 AI 中使用 | [Lite Prompt](platforms/generic-chat/TUTOR_LITE_PROMPT.md) |
| 安装或同步 Full Skill | [安装说明](INSTALL.md) |
| 选择跨平台适配方式 | [兼容性说明](PORTABILITY.md) |
| 看实际示例 | [使用示例](EXAMPLES.md) |
| 查看版本更新 | [更新记录](CHANGELOG.md) |

普通 ChatGPT、Gemini、DeepSeek、豆包、Kimi 或 Qwen 用户可以直接复制 Lite
Prompt。Codex / Claude Code-style agent 用户可以使用完整 Skill；如果 Codex
已经显示 `tutor-*` 入口，可以直接选择最符合当前任务的入口。

## 现在能做什么

| 能力 | 作用 |
| --- | --- |
| 诊断式教学 | 判断学科、知识点、前置知识、符号、方法或推理缺口 |
| 学习目标确认 | 把“我想学机器学习”这类大目标缩成可开始的方向 |
| 小型知识地图 | 只展示当前目标真正相关的依赖关系 |
| 学习计划 | 给出学科优先、可执行的短计划，而不是庞大路线图 |
| 练习与批改 | 一次生成一道针对性练习，等待作答后做定性批改 |
| Readiness Gate | 根据推理、独立应用和近迁移证据判断是否进阶 |
| Knowledge Link Cards | 用 1–3 张短卡解释正在阻碍当前任务的强相关概念 |
| 学习状态卡 | 用可见、可复制的卡片跨 chat 接续，不依赖隐藏记忆 |
| 可视化辅助 | 在确实有助于理解时使用简单图、表、流程或 trace |
| 跨平台 Prompt | 为普通聊天、Custom Bot 和 API-style 使用提供精简适配 |

## Codex 技能入口

| 我需要 | 选择 |
| --- | --- |
| 通用诊断式教学 | `universal-diagnostic-tutor` |
| 从大目标开始学习 | `tutor-learn-anything` |
| 制定短学习计划 | `tutor-study-plan` |
| 练习、批改、判断能否进阶 | `tutor-practice` |
| 理科或 CS 备考 | `tutor-exam-track` |
| 诊断知识缺口 | `tutor-diagnose-gap` |
| 分析错因 | `tutor-mistake-review` |
| 保存或继续学习状态 | `tutor-state-card` |
| 查找可信学习资源 | `tutor-resource-scan` |
| 用图或流程辅助理解 | `tutor-visualize` |

这些入口都回到同一套 Tutor System，不是十个互相独立的产品。`/practice`、
`/study-plan` 等写法是文字意图快捷方式，不保证是每个平台的原生 slash command。
具体选择方法见 [COMMAND_SURFACE.md](COMMAND_SURFACE.md)。

## 它怎样工作

```text
确认目标 -> 小型知识地图 -> 教一个概念 -> 针对性练习
-> 学习者作答 -> 定性批改 -> 错因修复
-> 可见状态更新 -> 进阶判断 -> 下一步
```

这条链不会被强行套在每个简单问题上。快速事实问题可以简短回答；练习回合通常
只发一道题，然后停下来等学习者作答，不会在一条消息里虚构完整闭环。

## V1.9 重点：练习与掌握闭环

V1.9 加入 Practice & Mastery Loop，让 Tutor 不只是会讲，还能根据当前概念和
掌握证据出一道针对性练习、等你作答、保留正确部分、指出关键错误、分析错因、
在有用时更新可见状态，并判断应该进阶、复习、降一步、重新诊断还是继续练习。

进阶必须有证据。“已经讲过”或一次碰巧答对都不等于掌握。Knowledge Link
Cards 只用于真正阻碍当前任务的强相关概念，通常限制在 1–3 张，并在解释后回到
原任务。

## 一个简短例子

面对向量题，普通 answer-first 回答可能直接计算。这个 Tutor 会先判断学习者是否
把“平行”误解成“每个分量相等”，补上“标量倍数”这个关键概念，只带一小步，
然后让学习者自己完成检查。更多对比见 [EXAMPLES.md](EXAMPLES.md)。

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=Date)](https://www.star-history.com/#SenmuuuuW/universal-diagnostic-tutor-skill&Date)

## 文档导航

| 文档 | 用途 |
| --- | --- |
| [USER_GUIDE.md](USER_GUIDE.md) | 面向普通用户的完整中文新手教程 |
| [COMMAND_SURFACE.md](COMMAND_SURFACE.md) | Tutor 入口和文字快捷方式说明 |
| [INSTALL.md](INSTALL.md) | 安装、更新与复制版 Skill 同步 |
| [PORTABILITY.md](PORTABILITY.md) | Full Skill、Custom Bot、Lite Prompt 与 API Prompt 选择 |
| [EXAMPLES.md](EXAMPLES.md) | 简短公开示例 |
| [EVALS.md](EVALS.md) | 行为评估案例 |
| [QUALITY_RUBRIC.md](QUALITY_RUBRIC.md) | 教学质量评分标准 |
| [FAILURE_TAXONOMY.md](FAILURE_TAXONOMY.md) | 已知失败类型与修复方向 |
| [CHANGELOG.md](CHANGELOG.md) | 完整版本记录 |

根目录的中英文 README 只负责项目展示和导航。完整教程保留在上述文档中，Skill
实现与维护说明位于 [`skills/universal-diagnostic-tutor/`](skills/universal-diagnostic-tutor/)。

## 使用边界

- 不提供隐藏记忆、自动学习档案、数据库、RAG/vector store 或后端基础设施。
- 不声称官方评分，不承诺提分，不预测考试，不使用泄题材料，不帮助作弊或押题。
- 不声称所有平台原生支持 Skill 或 slash command。
- 不替代医疗、法律、金融、税务或安全等专业建议。
- 不是教材仓库、答案库、课程平台或持久化成绩系统。

跨 chat 接续依赖用户可见、可复制的 Learning State / Profile / Task Cards。不同
平台的 prompt adapter 能力可能弱于完整 Skill。

## License

项目采用 [MIT License](LICENSE)。
