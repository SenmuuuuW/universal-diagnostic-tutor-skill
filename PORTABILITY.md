# Cross-Platform Portability

`universal-diagnostic-tutor` is a Markdown-based Tutor Skill. Different AI
environments can use different packaging levels, but they do not all support
native Skill loading.

Use the strongest pack your environment can actually load.

## Four Usage Packs

### Full Skill Version

Use the full `skills/universal-diagnostic-tutor/` directory when the agent can
read a Skill folder, project files, references, and examples.

Best for:

- OpenAI Codex / Codex-style Skill workflows.
- Claude Code / Claude Code-style agents when they can use a Skill folder or
  project instructions with files.
- Local or IDE agents that can read Markdown instructions from a repo.

This is the strongest version because the agent can route from `SKILL.md` into
references and examples as needed.

### Custom Bot Version

Use compact instructions for platforms such as ChatGPT GPTs, Gemini Gems, or
Coze / Doubao-style bots. These platforms may allow custom instructions and
optional knowledge files, but they do not automatically behave like a Codex
Skill.

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
| ChatGPT GPTs | Custom GPT instructions | Medium-high | Copy instructions; optionally upload selected docs |
| ChatGPT Projects | Project instructions | Medium | Use project instructions and selected files |
| Gemini Gems | Gem instructions | Medium | Copy Gem instructions; no full repo auto-loading |
| Coze / Doubao-style bots | Bot prompt | Medium | Use bot prompt and optional knowledge files |
| DeepSeek / API models | API system prompt | Medium | Developer must pass system prompt and context manually |
| Ordinary ChatGPT / Gemini / DeepSeek / 豆包 / Kimi / Qwen chat | Lite Prompt | Light | Manual copy-paste; not full Skill |
| Local / IDE agents | Depends | Medium to full | Depends on whether the agent can read Markdown instructions and project files |

## Adapter Files

- Full Skill for Codex: `platforms/codex/README.md`
- Full Skill / project-instruction guidance for Claude Code-style agents:
  `platforms/claude-code/README.md`
- Custom GPT instructions: `platforms/chatgpt-gpt/INSTRUCTIONS.md`
- ChatGPT Project instructions: `platforms/chatgpt-project/PROJECT_INSTRUCTIONS.md`
- Gemini Gem instructions: `platforms/gemini-gems/GEM_INSTRUCTIONS.md`
- Coze / Doubao bot prompt: `platforms/coze-doubao/BOT_PROMPT.md`
- API system prompt: `platforms/deepseek-api/SYSTEM_PROMPT.md`
- Generic chat Lite Prompt: `platforms/generic-chat/TUTOR_LITE_PROMPT.md`
- Generic chat Ultra-Lite Prompt: `platforms/generic-chat/TUTOR_ULTRA_LITE_PROMPT.md`

## Portability Rules

- Do not overclaim native support. If a platform cannot load Skill folders, use
  copied instructions instead.
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
