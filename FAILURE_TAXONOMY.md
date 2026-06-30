# Failure Taxonomy

Use this taxonomy to classify real tutoring failures before changing the Skill.
Prefer targeted fixes over broad feature additions.

| Failure type | Definition | Example symptom | Likely fix location | Urgency |
| --- | --- | --- | --- | --- |
| Answer-first regression | Gives the final answer before diagnosing or teaching when tutoring was requested. | Solves the whole series problem after the user asked for hints. | `SKILL.md`, pacing, output formats, evals | Urgent |
| Over-explaining | Adds unnecessary background, sources, applications, or proof. | Defines graph theory, matchings, and Vizing's theorem for a symbol question. | cognitive load, next best step, examples | Normal |
| Under-explaining | Compresses so much that the learner cannot understand why. | Says "move against the gradient" with no loss/parameter explanation. | explanation compression, output formats | Normal |
| Wrong domain diagnosis | Routes to the wrong subject or subtopic. | Treats edge coloring as vertex coloring. | subject routing, knowledge-system mapping, evals | Urgent |
| Wrong knowledge gap diagnosis | Misidentifies the blocker. | Reteaches derivatives when the learner lacks optimization meaning. | knowledge gap taxonomy, next best step | Normal |
| Fake mastery | Advances after one correct or guessed answer. | Says the learner mastered conditional probability after one formula. | mastery signal, review/advance, evals | Normal |
| Ignored learner signal | Fails to respond to level, speed, confusion, or mode request. | Gives advanced proof after "我是零基础". | trigger matrix, teaching mode selection | Urgent |
| Repeated same explanation | Responds to confusion by restating the same model. | "I still don't understand" gets the same matrix explanation. | multiturn protocol, stateless recovery examples | Normal |
| No stop point | Continues after a check or hints-only request. | Asks "edge or vertex?" then proves the theorem. | stop point, interaction pacing, evals | Urgent |
| Over-compressed advanced response | Treats advanced mode as answer-only. | Gives theorem statement with no assumptions or proof hinge. | standard/advanced mode, compression | Normal |
| Internal tool/protocol leakage | Exposes file names, version numbers, protocols, or hidden process in tutoring. | "According to student_facing_response_protocol.md..." | no leakage, student-facing protocol | Urgent |
| Raw dollar math / formula formatting failure | Uses `$...$` or `$$...$$` in normal tutoring examples. | Shows `$Ax=b$` in a user-facing answer. | math formatting, examples, docs | Normal |
| Formula-only code block | Puts ordinary math in fenced code blocks. | Displays partial fractions as a code block. | math formatting, output formats | Normal |
| Resource dumping | Lists links instead of teaching. | Provides five course links and no explanation. | resource-orchestrated tutoring, evals | Normal |
| Fake source or weak source | Invents a citation or uses an unreliable source as authority. | Mentions a nonexistent MIT page. | source trust, source note checklist | Urgent |
| Context-loss failure | Cannot continue from provided context or long-session summary. | Restarts vector basics despite a Learning State Card. | handoff, state card, checkpoint protocols | Normal |
| Stale copied Skill / install confusion | User updated repo but agent reads an older copied skill. | GitHub shows V1.5, local agent behaves like V1.2. | README, INSTALL, AGENTS | Minor |
| Non-STEM overgeneralization | Claims one STEM tutoring pattern fits every field. | Treats literature analysis like formula solving. | subject modes, universal scope docs | Normal |
| Safety/boundary failure | Gives personalized high-stakes advice instead of education. | Recommends medical treatment or investment action. | evaluation checklist, guardrails | Urgent |

## Use Notes

- Mark the most specific failure type first.
- If one output has several failures, identify the earliest cause.
- Repeated failures should become eval prompts.
- Do not add a broad new protocol for one isolated weak answer.
