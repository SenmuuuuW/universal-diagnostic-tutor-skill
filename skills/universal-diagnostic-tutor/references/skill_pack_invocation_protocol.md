# Skill Pack Invocation Protocol

Use this protocol when the learner uses short slash-style flow names or when
documentation needs a memorable way to describe the Skill's capabilities.

These names are prompt conventions, not CLI commands. Ordinary chat users can
type them manually. Full Skill environments can treat them as clear intent
signals. User-facing answers should still sound natural and should not expose
internal protocol names.

V1.8.1 also adds discoverable sub-skill entrypoint folders such as
`tutor-study-plan`, `tutor-exam-track`, and `tutor-state-card`. Prefer those
entrypoints in Codex-style Skill environments when they are available. Manual
slash-style shortcuts remain useful in ordinary chat, Custom Bot prompts, and
platforms without Skill discovery.

The canonical Tutor System remains `skills/universal-diagnostic-tutor/`.
Sub-skill entrypoints should stay thin and should not duplicate the full
`SKILL.md` or reference system.

## User-Invoked Flows

| Flow | Meaning | Use When | Output Shape | Avoid |
| --- | --- | --- | --- | --- |
| `/tutor` | Start diagnosis-first tutoring for a learning question. | The user wants help understanding a STEM / AI-CS problem or concept. | Compact topic scan, likely gap, one teaching step, one check. | Full answer dump or rigid section labels. |
| `/diagnose-gap` | Identify what is missing before teaching. | The learner says they do not know why they are stuck. | Subject, subtopic, likely gap, first repair step. | Long course roadmap or shaming the learner. |
| `/study-plan` | Make a brief plan from current state and goal. | The user has a goal, exam, or broad topic. | Current state, goal, top gaps, order, today's first step, check. | Huge curriculum map or guaranteed outcomes. |
| `/exam-track` | Use STEM Exam Track for review and practice. | The user is preparing for university STEM, 考研数学, or CS professional courses. | Topic, likely prerequisite gap, pattern, repair step, practice direction. | Cheating, leaked materials, score guarantees, or 押题 claims. |
| `/state-card` | Generate or continue from a visible card. | The learner wants to continue later or across chats. | Learning State Card, Learner Profile Card, or Learning Task Card. | Hidden-memory claims or full transcript dumps. |
| `/resource-scan` | Identify topic and suggest trusted resources when useful. | The user asks for resources, self-study, or broad topic support. | Topic scan, source roles, one or two trusted resource directions. | Link dumping or fabricated sources. |
| `/visualize` | Use a simple visual representation. | A graph, diagram, trace, map, or sketch would clarify the gap. | Short visual description, ASCII/table/Mermaid if useful, one check. | Decorative visuals or complex diagrams with no learning purpose. |
| `/mistake-review` | Analyze wrong reasoning and repair it. | The user gives an incorrect answer or process. | Surface mistake, underlying gap, why tempting, repair, near-match practice. | Only saying wrong or giving the final answer. |

## Auto-Invoked Behaviors

Apply these silently from learner evidence, even without slash-style flow names:

- domain and gap diagnosis
- mode selection
- next-best-step teaching
- cognitive-load control
- error-to-intervention
- explanation compression
- stop-point discipline
- Learning State Card suggestion when continuation would help

## Response Rules

- Treat slash flows as intent shortcuts, not as commands to print a template.
- Combine flows when natural, such as `/exam-track` plus `/mistake-review`.
- Keep normal tutoring answers student-facing and concise.
- If the flow name is ambiguous, ask one short clarification.
- Preserve math formatting with `\(...\)` and `\[...\]`.
- Do not imply the Skill has a shell, bot command system, database, or hidden
  memory unless the host platform actually implements something separately.
