# Cross-Platform Portability

[English](README.md) | [中文](README.zh-CN.md)

`universal-diagnostic-tutor` is a Markdown-based Tutor Skill. Different AI
environments can use different packaging levels, but they do not all support
native Skill loading.

For a step-by-step Chinese beginner tutorial from GitHub entry to each platform
choice, see [USER_GUIDE.md](USER_GUIDE.md).

Use the strongest pack your environment can actually load.

## Native Skill Environment: DeepSeek Harness

DeepSeek Harness (DSH) loads the Skill folder itself. It is a native Skill
environment, not a prompt-pasting target, so it needs no adapter prompt and no
second copy of the tutoring instructions.

```text
Universal Diagnostic Tutor Core
        ↓
DeepSeek Harness Skill Loader
```

The canonical behavior stays in exactly one place:

```text
skills/universal-diagnostic-tutor/
```

DSH discovers `<skill-root>/universal-diagnostic-tutor/SKILL.md` from its
project and user skill roots, reads the frontmatter into a session catalog, and
loads the body plus `references/` on demand. Installation, update, and
verification steps live in
[INSTALL.md](INSTALL.md#deepseek-harness--dsh); the platform notes live in
[platforms/deepseek-harness/](platforms/deepseek-harness/README.md).

Do not treat DSH as a fifth prompt pack. Anything DSH-specific is installation,
discovery, loading, or packaging — never a second set of tutoring rules.

## Four Usage Packs

### Full Skill Version

Use the full `skills/universal-diagnostic-tutor/` directory when the agent can
read a Skill folder, project files, references, and examples.

In Codex / Claude Code-style environments that support skill discovery, use
the single Skill folder `skills/universal-diagnostic-tutor/`. There is one
public entrypoint; practice, planning, resources, visuals, and continuity are
triggered automatically from natural-language intent, and legacy slash-style
text remains silently recognized for backward compatibility.

Best for:

- OpenAI Codex / Codex-style Skill workflows.
- Claude Code / Claude Code-style agents when they can use a Skill folder or
  project instructions with files.
- Local or IDE agents that can read Markdown instructions from a repo.

This is the strongest version because the agent can route from `SKILL.md` into
references and examples as needed.

Full Skill environments handle broad goals with clarify-first handling: ask one
to three focused questions, confirm the target in one sentence, build a compact
knowledge map, and select one next step before teaching. All routes stay inside
the one tutor.

For usage examples with one tutor, see [COMMAND_SURFACE.md](COMMAND_SURFACE.md).

### Custom Bot Version

Use compact instructions for platforms such as ChatGPT GPTs, Gemini Gems, or
Coze / Doubao-style bots. These platforms may allow custom instructions and
optional knowledge files, but they do not automatically behave like a Codex
Skill.

Custom GPTs, Gems, Projects, and bots do not show a feature menu. Use
their instruction field and ask with natural language; legacy shortcuts such
as `/study-plan` still work as silent intent signals.

Best for:

- Custom GPT instructions.
- Gemini Gem instructions.
- Coze / Doubao bot prompts.
- ChatGPT Projects with project instructions and selected uploaded docs.

### Lite Prompt Version

Use the Lite Prompt when the platform is an ordinary chat AI and cannot load a
repo, Skill folder, or reference files.

Best for:

- Ordinary ChatGPT, Gemini, DeepSeek, Doubao, Kimi, Qwen, and similar chat apps.

The Lite Prompt is not the full Skill. It preserves the core tutoring style,
but it cannot automatically access the full reference system.
For broad goals, it should still clarify and confirm before giving a small
map and one next step.
Ordinary chat platforms should use the Lite Prompt and natural language
rather than expecting any discoverable skill entries.

### API Prompt Version

Use the API system prompt when a developer calls an OpenAI-compatible,
DeepSeek-compatible, or similar chat completion API.

The developer must pass the system prompt and relevant conversation context
manually. Normal chat completion APIs are stateless between calls unless the
developer sends prior messages, summaries, or a Learning State Card.

## Compatibility Table

| Platform / environment | Recommended pack | Expected strength | Notes |
| --- | --- | --- | --- |
| OpenAI Codex | Full Skill | Full | Uses Skill directory and references |
| Claude Code / Claude Code-style agents | Full Skill | Full | Use Skill folder or project instructions depending on environment |
| Codex / Claude Code-style agents with skill discovery | Full Skill (single `universal-diagnostic-tutor` folder) | Full | Natural-language routing; no feature menu |
| ChatGPT GPTs | Custom GPT instructions | Medium-high | Copy instructions; no feature menu |
| ChatGPT Projects | Project instructions | Medium | Use project instructions and selected files; no guaranteed entrypoint picker |
| Gemini Gems | Gem instructions | Medium | Copy Gem instructions; no full repo auto-loading or skill menu |
| Coze / Doubao-style bots | Bot prompt | Medium | Use bot prompt and optional knowledge files; commands are prompt text |
| DeepSeek-compatible / OpenAI-compatible API models | API system prompt | Medium | Developer must pass system prompt and context manually |
| Ordinary ChatGPT / Gemini / DeepSeek / 豆包 / Kimi / Qwen chat | Lite Prompt | Light | Manual copy-paste; not full Skill |
| Local / IDE agents | Depends | Medium to full | Depends on whether the agent can read Markdown instructions and project files |

## Adapter Files

- Full Skill for Codex: `platforms/codex/README.md`
- Single-tutor usage examples: `COMMAND_SURFACE.md`
- Full Skill / project-instruction guidance for Claude Code-style agents:
  `platforms/claude-code/README.md`
- Custom GPT instructions: `platforms/chatgpt-gpt/INSTRUCTIONS.md`
- ChatGPT Project instructions: `platforms/chatgpt-project/PROJECT_INSTRUCTIONS.md`
- Gemini Gem instructions: `platforms/gemini-gems/GEM_INSTRUCTIONS.md`
- Coze / Doubao bot prompt: `platforms/coze-doubao/BOT_PROMPT.md`
- API system prompt: `platforms/deepseek-api/SYSTEM_PROMPT.md` keeps DeepSeek
  visible as a common target, but the prompt is also for OpenAI-compatible or
  similar chat completion APIs.
- Generic chat Lite Prompt: `platforms/generic-chat/TUTOR_LITE_PROMPT.md`
- Generic chat Ultra-Lite Prompt: `platforms/generic-chat/TUTOR_ULTRA_LITE_PROMPT.md`

## Portability Rules

- Do not overclaim native support. If a platform cannot load Skill folders, use
  copied instructions instead.
- The single Skill is useful only where the environment can discover or
  select Skill folders.
- Lite Prompt is not the full Skill; it is a manual, reduced behavior layer.
- Custom bots may vary in how much context, files, or instructions they retain.
- API usage requires the developer to send the system prompt and context on
  each relevant call.
- Learning State Cards help non-agent platforms continue across chats without
  hidden memory.
- Platform behavior may vary; test with a few realistic tutoring prompts before
  relying on the adapter for serious study.

## Choosing Quickly

- If your tool can read `skills/universal-diagnostic-tutor/`, use Full Skill.
- If your tool lets you create a custom bot, use the matching custom
  instruction file.
- If your tool is a normal chat box, use the Lite Prompt.
- If you are a developer calling an API, use the API system prompt and pass
  conversation history or a Learning State Card manually.
