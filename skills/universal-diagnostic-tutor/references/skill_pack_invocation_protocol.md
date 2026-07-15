# Skill Pack Invocation Protocol

Use this protocol when the learner uses a slash-style text shortcut or when
documentation needs to explain the public Tutor command surface.

The canonical Tutor System remains `skills/universal-diagnostic-tutor/`.
Focused entrypoints are thin public doors into that system; they do not own
separate Tutor behavior or duplicate the main `SKILL.md` and references.

## Canonical Command Surface

| User need | Canonical entrypoint | Text aliases |
| --- | --- | --- |
| General tutoring | `universal-diagnostic-tutor` | `/tutor` if documented |
| Learning path / study plan / exam route | `tutor-learn-path` | `/learn-anything`, `/study-plan`, `/exam-track` |
| Practice / grading / mistakes / gap diagnosis | `tutor-practice` | `/practice`, `/mistake-review`, `/diagnose-gap` |
| Learning state | `tutor-state-card` | `/state-card` |
| Resources | `tutor-resource-scan` | `/resource-scan` |
| Visualization | `tutor-visualize` | `/visualize` |

`/exam-track` routes by task: planning and review-order requests use
`tutor-learn-path`; drills, submitted work, mistake repair, and mastery checks
use `tutor-practice`.

These aliases are prompt conventions, not guaranteed native slash commands.
Ordinary chat users can type them manually, while Skill-capable environments
should promote only the six canonical entrypoints.

## Response Rules

- Treat aliases as intent signals, not commands to print a rigid template.
- Preserve the behavior behind older aliases; only the visible wrapper list is
  simplified.
- Enter at the step implied by the request instead of applying every Tutor
  capability at once.
- Keep normal tutoring answers natural and student-facing.
- If an alias is ambiguous, ask one short clarification.
- Preserve math formatting with `\(...\)` and `\[...\]`.
- Do not imply a shell, native command system, database, or hidden memory unless
  a host platform separately provides it.

## Auto-Invoked Behaviors

Apply these silently from learner evidence when useful:

- domain and gap diagnosis
- mode selection and cognitive-load control
- next-best-step teaching
- error-to-intervention and explanation compression
- stop-point discipline
- visible Learning State Card suggestions for continuation
