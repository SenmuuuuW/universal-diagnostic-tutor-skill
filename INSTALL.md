# 安装与更新指南

这个项目目前是一个 Markdown-based Tutor Skill，不是网站、App、npm 包或自动安装器。最安全的使用方式是 clone 仓库，然后按你的 agent 环境引用、复制或同步真正的 Skill 目录。

如果你不是技术用户，只想知道普通 ChatGPT / 豆包 / DeepSeek / Kimi / Qwen 怎么用，请先看 [USER_GUIDE.md](USER_GUIDE.md)。Lite Prompt 不需要安装，只需要复制到普通 AI chat。

## 这到底要下载什么？

这个仓库包含一个主要 Skill：

```text
skills/universal-diagnostic-tutor/
```

通常你需要 clone 整个仓库，然后使用、复制或引用这个 Skill 目录。根目录里的 `README.md`、`CHANGELOG.md` 和 `AGENTS.md`，以及 Skill 目录里的 `references/` 和 `examples/`，用来帮助用户和 agent 理解这个 Skill 的行为、版本和维护规则。

真正给 agent 使用的 Skill 文件夹是：

```text
skills/universal-diagnostic-tutor/
```

## 适用于哪些环境？

| 环境 | 适配方式 | 说明 |
| --- | --- | --- |
| OpenAI Codex / Codex-style Skill workflows | 推荐 / 主要适配 | 使用 `skills/universal-diagnostic-tutor/` 作为 Skill 目录。 |
| Claude Code / Claude Code-style agents | 可参考适配 | 如果环境支持 Skills、project instructions 或自定义 instruction 文件夹，可以把该 Skill 作为教学行为层使用。 |
| 其他 instruction-based coding agents | 可手动适配 | 可引用 `SKILL.md`、README 和相关 references 作为项目 / agent instructions。 |
| 普通 ChatGPT / 网页聊天 | 非原生 Skill | 可以手动复制提示词或核心说明，但不会自动加载整个 Skill 目录。 |
| 本地模型 / IDE Agent | 取决于环境 | 需要该环境能读取 Markdown instructions、项目文件和自定义规则。 |

不要过度理解成“所有平台都原生支持”。不同工具的 Skill 路径、加载方式、缓存机制和权限模型都不一样，请以各自工具文档为准。

如果你的平台不支持 Skill 文件夹，请使用根目录 [PORTABILITY.md](PORTABILITY.md) 和 `platforms/` 里的平台适配提示词。Lite Prompt 不需要安装，只需要手动复制；完整 Skill 安装仍推荐用于 Codex / Claude Code-style 工作流。

## 方法一：让 Codex / Claude Code-style agent 帮你安装

如果你不确定该复制到哪里，推荐让当前 agent 帮你定位环境。复制下面这段给你的 Codex / Claude Code-style agent：

```text
请帮我安装或更新这个 Markdown-based Tutor Skill：
https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill

要求：
1. 如果本地没有这个仓库，请 clone 它；如果已经有，请进入仓库并运行 git pull。
2. 找到真正的 Skill 目录：skills/universal-diagnostic-tutor/
3. 判断当前 agent 环境期望的 custom skills / project instructions 位置。
4. 如果环境支持直接读取 Skill 文件夹，请复制或引用 skills/universal-diagnostic-tutor/。
5. 如果环境只支持 project instructions，请使用 SKILL.md、README.md 和必要 references 作为项目指令来源。
6. 不要删除我已有的 skills 或自定义指令。
7. 如果你不确定正确的 skill 位置，请先问我，不要擅自覆盖文件。
8. 安装或同步后，请用 CHANGELOG.md 和 git log --oneline -1 确认当前版本。
9. 完成后提醒我新开一个 agent chat/session，让最新 Skill instructions 重新加载。
```

这个提示词的重点是安全：先识别环境，再复制或引用；不确定位置时先问用户。

## 方法二：手动下载 / clone

如果你还没有下载仓库：

```bash
git clone https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill.git
cd universal-diagnostic-tutor-skill
```

Skill 目录是：

```text
skills/universal-diagnostic-tutor/
```

接下来按你的 agent 环境要求，把这个目录放到、复制到或引用到对应的 skills / instructions 位置。

## 方法三：已经 clone 过，如何更新？

如果你已经有本地仓库，通常不需要重新 clone：

```bash
cd path/to/universal-diagnostic-tutor-skill
git pull
git log --oneline -1
```

- `git pull` 更新本地仓库副本。
- `git log --oneline -1` 查看本地当前最新 commit。
- 最新 commit 应该和 `CHANGELOG.md` 里的最新版本对应。

## 如果你的 agent 使用的是复制出去的 Skill

`git pull` 只会更新这个 repo 的本地副本。如果你的 agent 实际读取的是另一个位置里的复制版 Skill，你还需要把更新后的：

```text
skills/universal-diagnostic-tutor/
```

同步到 agent 真正读取的 skills 目录。

如果 agent 仍然表现得像旧版本，常见原因是：

- agent 读取的是旧的复制版 Skill 目录。
- 电脑上有多个 `universal-diagnostic-tutor-skill` 副本。
- 当前 chat/session 缓存了旧 instructions。

更新后建议新开一个 agent chat/session，让它重新加载最新 Skill instructions。

如果你用 V1.5 的 Learning State Card 跨 chat 继续学习，请把卡片复制到新 session；它不会通过 `git pull` 或 Skill 安装自动变成隐藏记忆。

## 为什么现在不是 npx 一键安装？

这个项目目前是 Markdown-based Skill，不是 npm package。真正的 `npx` 安装器需要 package setup、安装脚本、npm 发布、路径检测、跨平台兼容和额外维护。

目前最稳妥的方式是：

1. `git clone` 或 `git pull` 更新仓库。
2. 使用 agent-assisted install prompt 帮你定位真实 skill 路径。
3. 按当前环境复制、引用或同步 `skills/universal-diagnostic-tutor/`。

如果未来有足够需求，可以再考虑正式安装器；在那之前，本仓库不会为了“一键安装”加入 package setup 或脚本。

## 常见问题

**我需要重新下载吗？**

通常不需要。如果已经 clone 过，用 `git pull` 更新。

**为什么 GitHub 是新版，但 Codex / agent 还是旧版？**

agent 可能正在读取旧的复制版 Skill 目录，或者当前 session 缓存了旧 instructions。

**我到底复制哪个文件夹？**

复制或引用这个目录：

```text
skills/universal-diagnostic-tutor/
```

**普通 ChatGPT 能直接用这个 Skill 吗？**

不能自动加载整个 Skill 目录。你可以手动复制 README 里的提示词或 `SKILL.md` 的核心指令，但这不是原生 Skill 使用方式。

**更新后需要重新开 chat 吗？**

推荐。新开 agent session 更容易确保最新 instructions 被重新加载。
