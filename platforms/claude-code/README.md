# Claude Code-Style Usage

Use the full `skills/universal-diagnostic-tutor/` directory if your environment
supports Skill folders or repo-backed project instructions.

If your environment does not support native Skills, adapt `SKILL.md` plus a
small set of relevant references as project instructions. The behavior depends
on how that environment loads and prioritizes instructions.

## Suggested Files

- `skills/universal-diagnostic-tutor/SKILL.md`
- `skills/universal-diagnostic-tutor/references/skill_routing_architecture.md`
- `skills/universal-diagnostic-tutor/references/trigger_mode_matrix.md`
- `skills/universal-diagnostic-tutor/references/learning_efficiency_optimization_loop.md`
- `skills/universal-diagnostic-tutor/references/learning_state_card_protocol.md`
- `skills/universal-diagnostic-tutor/references/no_internal_tool_leakage_protocol.md`

## Notes

- Full behavior is available only when the agent can read the Skill folder and
  references.
- Project-instruction adaptation is useful but may be weaker than a full Skill
  workflow.
- After updating the repo or copied Skill directory, open a new session or
  reload instructions if the agent still behaves like an older version.
- Use Learning State Cards when continuing across chats or sessions.
