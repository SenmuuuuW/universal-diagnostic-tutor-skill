# Skill Entrypoints / Command Surface

## 1. 为什么要做这个？

以前 `/study-plan`、`/exam-track`、`/state-card` 这些更像内部 prompt
约定，不一定会出现在 Codex 的技能选择里。

V1.8.1 把常用能力拆成更清楚的 sub-skill entrypoints，方便用户在支持
Skill discovery 的环境里选择。它们不是新的产品，也不是独立系统；它们只是进入
Universal Diagnostic Tutor System 的不同门口。

## 2. Main Skill vs Sub-skill

- `universal-diagnostic-tutor` = 主 Skill / orchestrator
- `tutor-learn-anything` = 大目标学习入口
- `tutor-study-plan` = 学习计划入口
- `tutor-exam-track` = 理科备考入口
- `tutor-state-card` = 学习状态卡入口
- `tutor-resource-scan` = 可信资源入口
- `tutor-visualize` = 可视化入口
- `tutor-mistake-review` = 错题分析入口
- `tutor-diagnose-gap` = 知识缺口诊断入口

主 Skill 仍然是完整系统。`tutor-*` 文件夹是轻量 entrypoints，会指向同一套
诊断、教学、检查、状态卡和资源使用规则。

## 3. 在 Codex 里怎么用？

如果你的 Codex UI 显示 skill list 或 slash skill picker，可以选择相关的
`tutor-*` skill。

如果 UI 不显示直接的 sub-skill commands，可以在 skill picker / skills list
里按名称寻找，例如 `tutor-study-plan` 或 `tutor-exam-track`。

如果你的环境只支持主 Skill，仍然可以手动输入文字快捷方式：

```text
/study-plan ...
/exam-track ...
/state-card ...
/visualize ...
/mistake-review ...
```

不同 Codex 客户端、Claude Code-style agents、IDE agents 和普通聊天平台的 UI
不完全一样，所以这里不承诺某个固定按钮或菜单名称。

## 4. 选择哪个入口？

| 你想做什么 | 选哪个 |
| --- | --- |
| 我有一个很大的学习目标，不知道从哪里开始 | `tutor-learn-anything` |
| 我想要短学习计划 | `tutor-study-plan` |
| 我要备考高数/线代/概率/CS 专业课 | `tutor-exam-track` |
| 我想保存/继续学习状态 | `tutor-state-card` |
| 我想找可信资源 | `tutor-resource-scan` |
| 我需要函数图像/几何图/流程图辅助理解 | `tutor-visualize` |
| 我做错题了，想分析错因 | `tutor-mistake-review` |
| 我不知道自己到底缺哪个知识点 | `tutor-diagnose-gap` |
| 我只是问一道题或一个概念 | `universal-diagnostic-tutor` |

## 5. 例子

Machine learning broad goal:

```text
tutor-learn-anything: 我想学机器学习，但是数学很弱，不知道从哪里开始。
```

Linear algebra study plan:

```text
tutor-study-plan: 我想系统补线代，矩阵那章很乱。帮我做一个短计划。
```

Exam track:

```text
tutor-exam-track: 我明天考高数，级数判别法不会选，帮我诊断。
```

State card:

```text
tutor-state-card: 帮我生成下次继续用的 Learning State Card。
```

Visualize vector:

```text
tutor-visualize: 帮我画图理解两个向量平行为什么不是每个分量相等。
```

Mistake review:

```text
tutor-mistake-review: 我把条件概率直接除以总样本数了，帮我分析错因。
```

## 6. 注意事项

- 这些 sub-skills 是 entrypoints，不是独立产品。
- 主 tutor 逻辑仍然共享在 `skills/universal-diagnostic-tutor/`。
- 不要声称有隐藏记忆；跨 chat 继续用 Learning State Card。
- 不承诺提分、预测考试或押题。
- 不帮助作弊，不使用泄露材料。
- 普通聊天平台可能不会显示这些菜单命令；使用 Lite Prompt 或手动输入
  `/study-plan`、`/exam-track` 等文字快捷方式即可。
