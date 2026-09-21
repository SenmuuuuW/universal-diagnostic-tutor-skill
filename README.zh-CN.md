<div align="center">

# Universal Diagnostic Tutor

**一个不用选模式、也不用记命令的诊断式 AI 导师**

它先判断你真正卡在哪里，再决定下一步该讲、该问、该练还是该停。

简体中文 | [English](README.md)

[![Version](https://img.shields.io/badge/version-2.0.0-1f6feb.svg)](CHANGELOG.md)
![Markdown only](https://img.shields.io/badge/Markdown-only-555555.svg)
[![DeepSeek Harness](https://img.shields.io/badge/DeepSeek%20Harness-native%20skill-2f6f4e.svg)](platforms/deepseek-harness/README.md)
![Focus: STEM and AI-CS](https://img.shields.io/badge/Focus-STEM%20%2F%20AI--CS-1f6feb.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-2f6f4e.svg)](LICENSE)

[新手教程](USER_GUIDE.md) · [使用说明](COMMAND_SURFACE.md) · [安装](INSTALL.md) · [兼容性](PORTABILITY.md) · [示例](EXAMPLES.md) · [更新记录](CHANGELOG.md)

</div>

---

## 它是什么

Universal Diagnostic Tutor 是一个 Markdown-only 的 AI 导师行为层，重点面向大学理科、数学、编程、AI/CS 与备考复习。

它和普通 AI 回答最大的区别只有一句话：

> **它不是先给答案，而是先判断你卡在哪里。**

先定位学科、知识点、前置概念、符号、方法或推理缺口，再选择最小的、最值得推进的那一步；进阶前还会检查真实掌握证据，而不是看到一次答对就放行。

它不是课程平台、题库、数据库、RAG 系统，也不是隐藏记忆服务。

---

## 最新支持：DeepSeek Harness 原生 Skill

**DeepSeek Harness（DSH）现在可以原生加载本 Skill。** 不需要粘贴提示词，也不需要任何 DSH 专属的第二套指令。

```text
Universal Diagnostic Tutor Core
        ↓
DeepSeek Harness Skill Loader
```

DSH 会扫描固定的 skill 根目录，把 `universal-diagnostic-tutor/SKILL.md` 解析进 session catalog，并只在模型真正需要时才加载正文与 `references/`。安装方式（推荐 user 级 symlink）：

```bash
git clone https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill.git
cd universal-diagnostic-tutor-skill
mkdir -p ~/.agents/skills
ln -s "$(pwd)/skills/universal-diagnostic-tutor" ~/.agents/skills/universal-diagnostic-tutor
```

完整安装、更新与验证步骤见 [安装说明](INSTALL.md#deepseek-harness--dsh)，DSH 专属说明见 [platforms/deepseek-harness/](platforms/deepseek-harness/README.md)。

请区分三个不同的 DeepSeek 使用面：

| 使用面 | 加载方式 | 你需要做什么 |
| --- | --- | --- |
| DeepSeek **Chat** | 非原生 | 手动粘贴 Lite Prompt |
| DeepSeek **API** | 非原生 | 自己发送 system prompt |
| **DeepSeek Harness** | **原生 Skill** | 安装一次，之后自然语言使用 |

---

## 一个 Tutor，没有功能菜单

2.0 把公开入口收敛成一个 Tutor。练习、批改、错因分析、学习计划、备考、资源、可视化、连续性都不再是独立入口，而是由 Tutor 根据自然语言自动触发。

| 过去 | 现在 |
| --- | --- |
| 先选功能 / 子入口 | 直接说你要什么 |
| 记 slash command | 不需要记，旧写法仍被静默识别 |
| 自己判断该练习还是该讲解 | Tutor 自己判断 |
| 多个学习卡片 | 一个 Learning State Card（可选字段） |
| 模式菜单（零基础 / 标准 / 进阶） | 从你的表达里自动推断 |

你只需要说人话：

```text
教我这个
我为什么错了
我还是不懂
给我练习
推荐资料
画一下
我准备考试
继续上次的学习
```

旧版斜杠文本（`/practice`、`/study-plan`、`/mistake-review` 等）仍然被静默识别以保持向后兼容，但不再需要、也不再宣传。

---

## 核心循环

```text
Clarify → Diagnose → Intervene → Check → Decide → Carry
```

| 阶段 | 做什么 |
| --- | --- |
| Clarify | 只在大目标模糊时使用：1–3 个聚焦问题，然后停下等你回答 |
| Diagnose | 学科 → 知识体系 → 子主题 → 核心概念，并定位前置缺口或误解 |
| Intervene | 只教一个最小单元：对象含义、方法线索、设置、证明枢纽或误解修复 |
| Check | 一个聚焦检查或小任务；需要你参与时停下等待 |
| Decide | 把你的回答当掌握信号：推进、迁移、压缩、重讲、降一步或继续练 |
| Carry | 对话内轻量跟踪；跨对话用可见的 Learning State Card |

不是每个问题都会走完整条链。一个快速提问不会触发巨型流程；练习默认只出一道题，然后停下来等你的答案。

---

## 快速开始

| 你在哪里用 AI | 从这里开始 |
| --- | --- |
| **DeepSeek Harness（DSH）** | **原生 / 一等 Skill 支持**：把 `skills/universal-diagnostic-tutor/` 装到 DSH skill 根目录，见 [DSH 安装](INSTALL.md#deepseek-harness--dsh) |
| 普通 ChatGPT / Gemini / 豆包 / Kimi / Qwen 网页聊天 | 复制 [Lite Prompt](platforms/generic-chat/TUTOR_LITE_PROMPT.md) |
| Codex / Claude Code-style agent | 使用 [完整 Skill](skills/universal-diagnostic-tutor/)，按 [安装说明](INSTALL.md) 操作 |
| 自定义 bot 或 **DeepSeek API** | 在 [兼容性说明](PORTABILITY.md) 里选择适配方式 |

第一次使用建议先读 [新手教程](USER_GUIDE.md)；安装与更新在 [INSTALL.md](INSTALL.md)；只有一个入口这件事在 [COMMAND_SURFACE.md](COMMAND_SURFACE.md)。

---

## 它能做什么

下面这些是 Tutor 自动完成的行为，不是你需要在菜单里选择的「功能」。

| 行为 | 说明 |
| --- | --- |
| 诊断优先教学 | 先定位学科、概念、前置知识、符号、方法或推理缺口 |
| 大目标规划 | 澄清目标、给出紧凑知识地图、选出下一步 |
| 练习与掌握 | 出一道针对性练习、等你作答、定性批改、修复错因、判断能否进阶 |
| 自然语言路由 | 只有一个 Tutor；练习、规划、资源、可视化、连续性都由表达自动触发 |
| 备考复习 | 支持大学理科、考研数学、CS 专业课；不押题、不预测、不承诺提分 |
| 资源支持教学 | 只在能改进当前教学步骤时引入可信资源，不甩链接 |
| 相关概念卡片 | 只在强相关概念确实阻碍当前任务时，补 1–3 张短卡片并回到任务 |
| Learning State Card | 可见、可复制、用户控制的续学 checkpoint，不是隐藏记忆 |
| 跨平台适配 | 为普通聊天、自定义 bot、API 提供更小的 prompt 打包版本 |

当前覆盖最强的是大学层级 STEM 与 AI-CS：微积分、线性代数、概率统计、离散数学、编程、算法、机器学习、系统、网络、物理、信号与工程基础。它仍保留跨学科能力，但不把自己包装成泛泛的全科答题助手。

---

## 一个 Tutor，一个学习状态卡

跨对话继续学习只需要一个可见产物：

```text
Learning State Card:
- Subject:
- Topic:
- Already understood:
- Still weak:
- Next best step:
- Optional — preferred language / pace:
- Optional — active goal or exam target:
```

偏好、当前目标、最近一次练习作为**可选字段**并入同一张卡片。不存在并行的其它卡片类型，也不会暗示隐藏持久记忆、账号或数据库。

---

## 评测（本项目冻结 harness）

在一个固定的 29-case 评测 harness 中，v2.0.0 相对 v1.9.2 基线：

| 指标 | v1.9.2 | v2.0.0 |
| --- | --- | --- |
| Identity 组 | 4.622 | 4.819 |
| Quality 组 | 4.135 | 4.619 |
| 过度教学控制 | 3.62 | 4.62 |
| 错因诊断 | 3.75 | 4.50 |
| 下一步教学选择 | 4.03 | 4.55 |
| 自然度 | 4.53 | 4.76 |
| 严重失败 / 泄漏 | 0 / 0 | 0 / 0 |

同一 harness 下，运行时上下文从约 11,388 tokens 降到约 6,678 tokens（约 −41%）。

这些数字来自本仓库自己的冻结评测 harness，**不是**对所有模型或环境的普适性能承诺。

---

## 文档导航

| 文档 | 用途 |
| --- | --- |
| [新手教程](USER_GUIDE.md) | 面向非技术用户的从零使用教程 |
| [使用说明](COMMAND_SURFACE.md) | 单入口用法与自然语言示例 |
| [安装与更新](INSTALL.md) | 安装、更新、复制式 Skill 同步；含 DSH 章节 |
| [兼容性](PORTABILITY.md) | 完整 Skill、自定义 bot、Lite Prompt、API 的取舍 |
| [示例](EXAMPLES.md) | 简短的诊断优先教学示例 |
| [评测用例](EVALS.md) | 行为评测用例 |
| [质量评分标准](QUALITY_RUBRIC.md) | 教学质量评分口径 |
| [失败分类](FAILURE_TAXONOMY.md) | 已知失败类型与修复方向 |
| [更新记录](CHANGELOG.md) | 版本历史 |

根 README 是落地页；完整教程在教程文档里，实现层说明在 [`skills/universal-diagnostic-tutor/`](skills/universal-diagnostic-tutor/)。

---

## 边界

- 不做隐藏记忆、自动学习者画像、数据库、RAG/向量库或后端基础设施。
- 不做官方评分、提分保证、考试预测、泄露材料、作弊或押题。
- 不声称所有平台都原生支持 Skill 或 slash command。
- 不替代医疗、法律、金融、税务或安全领域的专业建议。
- 不收录盗版教材、答案库、课程平台或持久成绩册。

学习连续性只依赖一张可见、由用户控制的 Learning State Card。平台适配层只是 prompt 打包，能力可能弱于完整 Skill。

---

## Star History

<a href="https://www.star-history.com/?repos=SenmuuuuW%2Funiversal-diagnostic-tutor-skill&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&theme=dark&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
 </picture>
</a>

---

## License

Released under the [MIT License](LICENSE).
