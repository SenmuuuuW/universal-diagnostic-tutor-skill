# Universal Diagnostic Tutor Skill 使用教程

这是一份面向普通学生、群友和自学者的完整使用教程。你不需要先懂 GitHub、Codex 或编程工具，也可以从普通 AI chat 开始使用这个诊断式导师。

## 0. 这个教程适合谁？

适合你，如果你：

- 想用 AI 学理科 / STEM / AI-CS。
- 不想只让 AI 直接给答案。
- 想让 AI 先判断你卡在哪里，再一步步教。
- 只会用普通 ChatGPT / Gemini / DeepSeek / 豆包 / Kimi / Qwen 聊天窗口。
- 或者你会用 Codex / Claude Code-style agents，想使用完整 Skill。

这个 Tutor 的核心不是“答案快递”，而是先诊断：这题属于什么知识点，你缺的是概念、符号、方法、推理，还是题型识别。

## 1. 点进 GitHub 后先看哪里？

打开 GitHub 仓库后，你会看到很多文件。普通用户先不用慌，重点看这几个：

| 文件或文件夹 | 作用 |
| --- | --- |
| `README.md` | 项目首页，先了解这个 Tutor 是什么 |
| `USER_GUIDE.md` | 你正在看的完整新手教程 |
| `INSTALL.md` | 安装、更新、复制 Skill 的说明 |
| `PORTABILITY.md` | 不同 AI 平台应该选哪种用法 |
| `GROUP_GUIDE.md` | 适合发到微信群 / 社群的短版说明 |
| `EXAMPLES.md` | 看 answer-first 和 diagnosis-first 的区别 |
| `platforms/` | 不同平台可复制的 prompt adapters |
| `skills/universal-diagnostic-tutor/` | Full Skill 文件夹，适合 Codex / Claude Code-style agents |

如果你不是程序员，不需要先 clone repo。你可以直接使用 Lite Prompt。

## 2. 先判断你属于哪种用户

| 你现在用什么 | 推荐方式 |
| --- | --- |
| Codex / Claude Code-style agent | Full Skill |
| ChatGPT Custom GPT | Custom GPT instructions |
| ChatGPT Project | Project instructions |
| Gemini Gem | Gem instructions |
| Coze / 豆包智能体 | Bot prompt |
| 普通 ChatGPT / Gemini / DeepSeek / 豆包 / Kimi / Qwen 聊天 | Lite Prompt |
| API / 开发者 | System Prompt |

简单理解：

- Full Skill 最强，因为 agent 可以读取 `SKILL.md`、references 和 examples。
- Lite Prompt 最简单，复制到普通 AI chat 就能用。
- 普通 AI chat 不是满血版，但仍然能使用核心教学逻辑：先诊断，再教学，只讲下一小步，检查后再继续。

## 3. 最简单用法：普通 AI Chat / 豆包 / DeepSeek / Kimi / Qwen

这是普通用户最推荐的入口。

步骤：

1. 打开 GitHub 仓库。
2. 打开这个文件：
   `platforms/generic-chat/TUTOR_LITE_PROMPT.md`
3. 复制里面的整个 Lite Prompt。
4. 打开你常用的 AI chat app，例如 ChatGPT / Gemini / DeepSeek / 豆包 / Kimi / Qwen。
5. 把 Lite Prompt 作为第一条消息粘贴进去。
6. 然后再问你的学习问题。

可以直接复制这些第一题问法：

```text
我是零基础，请先判断这题属于哪个知识点，不要直接给完整答案。
```

```text
我会一点但卡在第一步，请先找我缺的概念。
```

```text
我做错了，这是我的思路，帮我分析错在哪里。
```

```text
请用 /study-plan 帮我根据当前基础和目标安排一个短计划。
```

```text
请用 /state-card 帮我生成下次继续用的学习状态卡。
```

如果 chat 很长，或者你准备下次继续学习，就让 Tutor 生成 Learning State Card。换到新 chat 时，先粘贴这张卡，再说：

```text
根据这个状态卡继续，不要从头讲。
```

## 4. 豆包 / Coze-style Bot 怎么用？

如果你只是打开普通豆包聊天窗口，用 Lite Prompt 就可以。

如果你在创建豆包 / Coze-style bot，可以使用：

```text
platforms/coze-doubao/BOT_PROMPT.md
```

把这个 bot prompt 复制到 bot 的角色说明、系统提示或 instruction 区域里。保存后，用一道学习题测试它是否会先诊断、再教学、问一个检查题后停。

注意：这只是 prompt adapter 用法，不是官方平台上架，也不代表平台原生支持这个 Skill。

## 5. ChatGPT GPTs 怎么用？

如果你可以创建 Custom GPT：

1. 打开 ChatGPT。
2. 创建一个 custom GPT。
3. 打开并复制：
   `platforms/chatgpt-gpt/INSTRUCTIONS.md`
4. 粘贴到 GPT instructions 区域。
5. 如果平台允许上传知识文件，可以选择少量文档，例如：
   - `USER_GUIDE.md`
   - `EXAMPLES.md`
   - `QUALITY_RUBRIC.md`
   - `EVALS.md`
6. 用一道学习题测试，例如：

```text
我是零基础，两个向量平行是什么意思？不要直接给完整答案。
```

Custom GPT 不等于 Full Skill。它可以模仿核心教学风格，但通常不能像 Codex Skill 那样自动读取完整 references。

## 6. ChatGPT Projects 怎么用？

如果你使用 ChatGPT Projects：

- 打开：
  `platforms/chatgpt-project/PROJECT_INSTRUCTIONS.md`
- 把内容放入 project instructions。
- 如果平台允许，可以添加少量相关文档作为项目文件。
- 跨 chat 或跨 session 继续时，使用 Learning State Card。

Project instructions 是一种适配方式，不等于 Full Skill。

## 7. Gemini Gems 怎么用？

如果你可以创建 Gemini Gem：

1. 创建一个 Gem。
2. 打开并复制：
   `platforms/gemini-gems/GEM_INSTRUCTIONS.md`
3. 粘贴到 Gem instructions。
4. 用 STEM 问题测试它是否会先判断知识点和卡点。
5. 如果你只是普通 Gemini 聊天窗口，用 Lite Prompt 更简单。

## 8. Codex / Claude Code-style agent 怎么用？

这是 advanced users 的路径。

完整 Skill 目录是：

```text
skills/universal-diagnostic-tutor/
```

建议阅读：

- `INSTALL.md`
- `platforms/codex/README.md`
- `platforms/claude-code/README.md`

如果你已经 clone 了仓库，更新仓库副本通常只需要：

```bash
git pull
```

但如果你的 agent 读取的是另一个位置里的复制版 Skill，`git pull` 只会更新仓库副本，不会自动更新复制版。你还需要把新的：

```text
skills/universal-diagnostic-tutor/
```

同步到 agent 真正读取的位置。

更新后建议新开一个 agent session，让它重新加载最新 instructions。

## 9. 常用调用方式

这些 slash-style flow 是意图快捷方式，不是 shell command。普通聊天用户可以直接手动输入。

| 调用方式 | 用途 |
| --- | --- |
| `/tutor` | 开始诊断式教学 |
| `/diagnose-gap` | 先找知识缺口 |
| `/study-plan` | 做短学习计划 |
| `/exam-track` | 理科备考 Track |
| `/state-card` | 生成或继续学习状态卡 |
| `/resource-scan` | 定位知识点并找可信资源方向 |
| `/visualize` | 用简单图示、表格或流程图解释 |
| `/mistake-review` | 分析错因并修复 |

示例：

```text
/tutor 我是零基础，两个向量平行是什么意思？
```

```text
/study-plan 我想准备考研数学，但线代很弱，先从哪里补？
```

```text
/exam-track 我高数级数总是不会选判别法，帮我诊断。
```

```text
/visualize 两个向量平行为什么不是每个分量相等？
```

```text
/mistake-review 我把两个平行向量的每个分量都设成相等了。
```

```text
/state-card 帮我生成下次继续用的学习状态卡。
```

## 10. Learning State Card 怎么用？

Learning State Card 不是隐藏记忆。它是一张你能看见、复制、保存、粘贴的学习 checkpoint。

它适合用来：

- 跨 chat 继续学习。
- 从一个平台切到另一个平台。
- 防止 AI 下次从头讲。
- 让 Tutor 知道你已经懂什么、还卡在哪里。

示例：

```text
Learning State Card:
- Subject:
- Topic:
- Already understood:
- Still weak:
- Current blocker:
- Next best step:
- Suggested continue prompt:
```

使用方式：

1. 对 Tutor 说：`帮我生成一个下次继续用的 Learning State Card。`
2. 复制生成的卡片。
3. 打开新 chat。
4. 粘贴卡片。
5. 再说：

```text
根据这个状态卡继续，不要从头讲。
```

如果没有卡片，也不要让 AI 假装记得旧聊天。你可以发一句话说明：上次讲到哪个知识点、你卡在哪里。

## 11. 理科备考 Track 怎么用？

理科备考 Track 适合：

- 大学 STEM 课程复习。
- 考研数学。
- CS 专业课复习。
- 高数 / 微积分。
- 线性代数。
- 概率统计。
- 离散数学。
- 大学物理。
- 数据结构。
- 算法。
- 计算机组成原理。
- 操作系统。
- 计算机网络。
- 机器学习基础。

它会帮助你：

- 判断题目属于哪个知识点。
- 找出缺的前置概念。
- 分析错因。
- 提炼题型线索。
- 给短复习顺序和练习方向。

它不会做这些事：

- 不作弊。
- 不使用泄露考试材料。
- 不保证提分。
- 不预测考试。
- 不押题。

示例：

```text
/exam-track 我准备考研数学，线代很弱，先从哪里补？
```

## 12. 如何反馈效果不好？

如果你觉得回答不好，反馈时最好带上：

- 你用的平台。
- 你用的是 Full Skill / Custom Bot / Lite Prompt。
- 你的原始问题。
- AI 的回答。
- 你觉得哪里不好：
  - 直接给答案太快。
  - 没判断知识点。
  - 讲太多。
  - 讲太少。
  - 没停下来检查。
  - 资源乱给。
  - 公式显示错误。
  - 没法跨 chat 继续。

这样维护者可以把问题变成可测试的小案例，而不是盲目加功能。

## 13. 常见问题

**我不会 GitHub，可以用吗？**

可以。直接打开 `platforms/generic-chat/TUTOR_LITE_PROMPT.md`，把 Lite Prompt 复制到你常用的 AI chat 里。

**豆包是不是官方上架？**

不是。这里说的是 Lite Prompt / adapter 用法，不是官方平台上架。

**普通 AI chat 是满血版吗？**

不是。Full Skill 最强；普通 AI chat 使用 Lite Prompt，只能获得核心教学风格。

**它会记住我吗？**

不会声称有隐藏记忆。要跨 chat 继续，请使用 Learning State Card。

**可以用来作弊吗？**

不可以。它的目标是学习和掌握，不是绕过考试或作业规则。

**可以保证提分吗？**

不可以。它可以帮助你诊断和练习，但不能保证分数。

**可以直接给答案吗？**

如果你明确要求“直接给答案”，它可以给简短答案和最关键原因。但这个 Tutor 的主要设计是 learning-first：先判断你卡在哪里，再帮你学会。
