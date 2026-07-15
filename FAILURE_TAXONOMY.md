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
| Generic exercise not aligned to gap | Generates practice for the broad topic without targeting the learner's current concept, prerequisite, or error. | A learner who keeps missing the inner derivative receives unrelated power-rule drills. | exercise generation, practice ladder, examples, evals | Normal |
| Grading only says right/wrong | Marks the final answer without preserving correct reasoning, identifying the missing part, or choosing a repair. | Replies only "wrong" to a correct setup with one calculation slip. | answer grading, mistake analysis, grading examples | Normal |
| Premature advancement | Moves to the next concept before the readiness evidence supports it. | Starts Bayes' theorem after one guessed conditional-probability answer. | readiness gate, mastery signal, review/advance, evals | Normal |
| Over-practice / giant worksheet | Generates more questions or ladder levels than the learner requested or can use in the current turn. | Sends fifteen mixed recursion problems when one base-case check was needed. | exercise generation, practice ladder, stop-point guidance | Normal |
| Fake scoring | Claims official points, percentages, or score outcomes without an authoritative rubric and sufficient evidence. | Says an informal proof will receive exactly 8/10 on an exam whose rubric was not provided. | answer grading, exam boundaries, evals | Urgent |
| Knowledge Link Cards become wiki dump | Expands strong concept links into a broad encyclopedia or adds weakly related cards. | A linear-regression question gets cards on all of linear algebra, calculus, statistics, and deep learning. | knowledge link cards, cognitive load, examples | Normal |
| No state update after practice | Finishes grading without recording the attempt, result, mistake evidence, concept status, or next checkpoint when continuity would help. | Corrects a repeated chain-rule error, then gives another question with no visible change to the Learning Task Card. | learning task loop, learning state card, task card | Normal |
| Skipped goal clarification | Starts teaching or planning before a broad goal is narrowed. | "I want to learn ML" gets a neural-network lecture. | goal clarifier, trigger matrix, evals | Normal |
| Excessive goal questioning | Turns clarification into a long intake survey. | Asks ten questions before giving any direction. | goal clarifier, adapters, evals | Normal |
| Giant knowledge map | Creates a course-sized roadmap when a compact local map is needed. | A matrix confusion question gets a full linear algebra syllabus. | knowledge map builder, output formats, evals | Normal |
| Generic study plan failure | Gives a broad timeline but fails to name required disciplines, subtopics, minimum mastery standards, skip-for-now topics, or realistic dependency order. | "Learn vectors, matrices, functions, probability, then PyTorch" without saying what to study inside each subject. | brief study plan, study-plan examples, adapters, evals | Normal |
| Wrong next learning step | Chooses an advanced or exciting topic before the unlocking prerequisite. | Sends weak-math ML learner to neural networks before vectors/functions. | learning path selector, next best step | Normal |
| Sub-skill routing failure | Applies the wrong flow or every flow at once. | A broad goal receives tutoring, resources, visuals, cards, and exam track all together. | learning orchestrator, skill routing | Normal |
| Ignored learner signal | Fails to respond to level, speed, confusion, or mode request. | Gives advanced proof after "我是零基础". | trigger matrix, teaching mode selection | Urgent |
| Repeated same explanation | Responds to confusion by restating the same model. | "I still don't understand" gets the same matrix explanation. | multiturn protocol, stateless recovery examples | Normal |
| No stop point | Continues after a check or hints-only request. | Asks "edge or vertex?" then proves the theorem. | stop point, interaction pacing, evals | Urgent |
| Over-compressed advanced response | Treats advanced mode as answer-only. | Gives theorem statement with no assumptions or proof hinge. | standard/advanced mode, compression | Normal |
| Internal tool/protocol leakage | Exposes file names, version numbers, protocols, or hidden process in tutoring. | "According to student_facing_response_protocol.md..." | no leakage, student-facing protocol | Urgent |
| Raw dollar math / formula formatting failure | Uses `$...$` or `$$...$$` in normal tutoring examples. | Shows `$Ax=b$` in a user-facing answer. | math formatting, examples, docs | Normal |
| Formula-only code block | Puts ordinary math in fenced code blocks. | Displays partial fractions as a code block. | math formatting, output formats | Normal |
| Resource dumping | Lists links instead of teaching. | Provides five course links and no explanation. | resource-orchestrated tutoring, evals | Normal |
| Resource overuse | Forces resources into answers where direct teaching is enough. | Adds source lists to a simple vector meaning question. | topic scan, resource protocols, evals | Normal |
| Fake source or weak source | Invents a citation or uses an unreliable source as authority. | Mentions a nonexistent MIT page. | source trust, source note checklist | Urgent |
| Exam overclaim | Promises score gains, predicts exams, claims 押题, or uses leaked materials. | "This will guarantee 20 more points" or "this is sure to appear." | exam track, evals, README | Urgent |
| Slash-flow ignored | Fails to treat user-invoked flows as intent signals. | `/study-plan` receives a normal answer with no plan. | skill pack invocation, adapters, evals | Normal |
| Entrypoint missing or unclear | A user cannot discover which `tutor-*` entrypoint to use. | A Codex user wants a state card but no clear `tutor-state-card` route is documented. | COMMAND_SURFACE, README, skill descriptions | Normal |
| Entrypoint duplication bloat | A thin sub-skill copies too much main Tutor logic. | `tutor-study-plan/SKILL.md` becomes another full `universal-diagnostic-tutor/SKILL.md`. | tutor-* SKILL files, AGENTS | Normal |
| Prompt shortcut / skill entrypoint confusion | Docs imply ordinary chat platforms expose Codex Skill menu commands. | A Lite Prompt user expects `tutor-exam-track` to appear as a button in normal chat. | COMMAND_SURFACE, PORTABILITY, USER_GUIDE | Normal |
| Profile card too verbose | Turns visible cards into transcripts, gradebooks, or persistent labels. | Learner Profile Card contains full chat history and rigid scores. | learner profile/task card, context portability | Normal |
| Visualization without learning purpose | Adds diagrams or images that do not clarify the current gap. | Generates a fancy graph when a one-line explanation was needed. | visualization protocol, examples | Normal |
| Context-loss failure | Cannot continue from provided context or long-session summary. | Restarts vector basics despite a Learning State Card. | handoff, state card, checkpoint protocols | Normal |
| Stale copied Skill / install confusion | User updated repo but agent reads an older copied skill. | GitHub shows V1.5, local agent behaves like V1.2. | README, INSTALL, AGENTS | Minor |
| Non-STEM overgeneralization | Claims one STEM tutoring pattern fits every field. | Treats literature analysis like formula solving. | subject modes, universal scope docs | Normal |
| Safety/boundary failure | Gives personalized high-stakes advice instead of education. | Recommends medical treatment or investment action. | evaluation checklist, guardrails | Urgent |

## Use Notes

- Mark the most specific failure type first.
- If one output has several failures, identify the earliest cause.
- Repeated failures should become eval prompts.
- Do not add a broad new protocol for one isolated weak answer.

## Generic Study Plan Failure

The tutor gives a broad timeline but fails to identify required disciplines,
required subtopics, minimum mastery standards, skip-for-now topics, or realistic
dependency order.

Examples:

- Says "learn vectors, matrices, functions, probability" without naming
  disciplines.
- Jumps from Python basics to scikit-learn or PyTorch too quickly.
- Gives resources before clarifying the learning map.
- Produces a plausible plan that does not tell the learner exactly what to
  study inside each subject.

Correction: use discipline-first study planning.
