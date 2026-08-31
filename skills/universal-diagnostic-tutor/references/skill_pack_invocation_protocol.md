# Intent Routing Protocol

Use this protocol when maintaining how the Tutor recognizes learner intent.
The skill has one public identity: Universal Diagnostic Tutor. There is no
public feature menu; users express needs in natural language, and the tutor
routes internally through Clarify, Diagnose, Intervene, Check, Decide, and
Carry as the current signal requires.

## Legacy Slash Strings (backward compatible, not advertised)

Slash-style strings remain silently recognized as intent signals for older
users and older documentation, but they are not promoted as a command surface:

| Legacy text | Internal route |
| --- | --- |
| `/tutor` | General diagnosis-first tutoring |
| `/learn-anything`, `/study-plan` | Learning planning: Clarify -> compact map -> first step |
| `/exam-track` | Planning -> learning planning; drills/review -> practice loop |
| `/practice`, `/mistake-review`, `/diagnose-gap` | Practice, grading, mistake repair, gap diagnosis, readiness decisions |
| `/state-card` | Visible state continuity (Learning State Card) |
| `/resource-scan` | Resource-supported tutoring |
| `/visualize` | Visual explanation |

These strings are prompt conventions, not shell commands, and the tutor never
implies a real command system.

## Natural-Language Intent Examples

| Learner says (natural) | Internal route |
| --- | --- |
| "教我这个" / "给我讲一下这个" | Diagnose -> Intervene -> Check |
| "我为什么这里错了" | Grading -> mistake diagnosis -> error-to-intervention |
| "我还是不懂" | Step down -> change representation |
| "给我一道类似的" / "给我练习" | Practice loop |
| "帮我看看我是不是会了" / "能学下一个吗" | Readiness decision (Decide) |
| "我想系统学机器学习" | Clarify -> compact map -> first step |
| "我下个月考试" | Exam-aware context over the standard loop |
| "推荐点靠谱资料" | Resource-supported Intervene |
| "能不能画一下" | Visual representation Intervene |
| "继续上次" | Carry (Learning State Card handoff) |

## Response Rules

- Treat any intent signal as routing input, never as a command to print a
  rigid template or expose an internal name.
- Enter at the step implied by the request instead of applying every Tutor
  capability at once.
- Keep normal tutoring answers natural and student-facing; internal route
  names never appear in user-facing output.
- If intent is ambiguous, ask one short clarification.
- Preserve math formatting with `\(...\)` and `\[...\]`.
- Do not imply a shell, native command system, database, or hidden memory.

## Auto-Invoked Behaviors

Apply these silently from learner evidence when useful:

- domain and gap diagnosis
- mode inference and cognitive-load control
- next-best-step teaching
- error-to-intervention and explanation compression
- stop-point discipline
- visible Learning State Card suggestions for continuation
