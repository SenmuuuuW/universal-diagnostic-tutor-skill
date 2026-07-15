# Claude Code-Style Usage

Use the full `skills/universal-diagnostic-tutor/` directory if your Claude
Code-style environment supports Skill folders or repo-backed project
instructions.

Exact discovery behavior varies by Claude Code setup, project configuration,
and whether the environment supports native Skills, custom instruction folders,
or project instructions. Do not assume every client shows the same skill picker
or slash UI.

## What To Install Or Reference

For the strongest setup, keep the main Skill folder and focused entrypoint
folders together in the location your environment reads:

```text
skills/universal-diagnostic-tutor/
skills/tutor-learn-path/
skills/tutor-practice/
skills/tutor-state-card/
skills/tutor-resource-scan/
skills/tutor-visualize/
```

Depending on your environment, these may be copied, symlinked, or referenced
from a project instructions location. Follow your tool's own documentation for
the exact path.

## Focused Entrypoints

- `universal-diagnostic-tutor`: general diagnosis-first tutoring.
- `tutor-learn-path`: broad learning goals, study plans, and exam routes.
- `tutor-practice`: practice, grading, mistake review, gap diagnosis, and readiness.
- `tutor-state-card`: Learning State / Profile / Task Cards.
- `tutor-resource-scan`: topic scan and trusted resource guidance.
- `tutor-visualize`: visual explanations, diagrams, tables, and traces.

Older shortcuts such as `/study-plan`, `/exam-track`, `/mistake-review`, and
`/diagnose-gap` remain text intent aliases; they are not separate folders.

For a user-facing overview, see [../../COMMAND_SURFACE.md](../../COMMAND_SURFACE.md).

## If Native Skill Discovery Is Not Available

If your environment does not expose the focused entrypoints, adapt
`skills/universal-diagnostic-tutor/SKILL.md` plus a small set of relevant
references as project instructions.

Ordinary text shortcuts still work as intent signals when included in the
prompt, such as:

```text
/learn-anything 我想学机器学习，但是数学很弱，不知道从哪里开始。
/study-plan 我想系统入门机器学习，但数学弱。给我一个学习计划。
/exam-track 我高数级数判别法总不会选，帮我诊断。
/state-card 帮我生成下次继续用的学习状态卡。
/practice 给我一道关于梯度下降的基础题，做完后帮我批改并判断能不能继续。
```

These are prompt shortcuts, not guaranteed native slash commands.

For practice, use one targeted exercise at a time unless the learner requests
a set. Wait for the answer, grade qualitatively, diagnose mistakes, and decide
whether to advance or review. Use one to three Knowledge Link Cards only when
a strongly related concept blocks the task.

## Suggested Files

- `skills/universal-diagnostic-tutor/SKILL.md`
- `skills/universal-diagnostic-tutor/references/skill_routing_architecture.md`
- `skills/universal-diagnostic-tutor/references/trigger_mode_matrix.md`
- `skills/universal-diagnostic-tutor/references/brief_study_plan_protocol.md`
- `skills/universal-diagnostic-tutor/references/learning_efficiency_optimization_loop.md`
- `skills/universal-diagnostic-tutor/references/learning_state_card_protocol.md`
- `skills/universal-diagnostic-tutor/references/learning_task_loop_protocol.md`
- `skills/universal-diagnostic-tutor/references/no_internal_tool_leakage_protocol.md`

## Notes

- Full behavior is available only when the agent can read the Skill folder and
  references.
- Project-instruction adaptation is useful but may be weaker than a full Skill
  workflow.
- If focused entrypoints do not appear, confirm the `skills/tutor-*` folders
  were copied or referenced alongside the main Skill folder.
- After updating the repo or copied Skill directory, open a new session or
  reload instructions if the agent still behaves like an older version.
- Use Learning State Cards when continuing across chats or sessions.
