# Skill Routing Architecture

Use this file when maintaining or evaluating the Skill's internal routing. The
goal is to help an agent choose the smallest useful protocol set for the user's
current signal.

User-facing tutoring answers should not mention these layers. They are internal
orientation for the agent and maintainers.

## Core Rule

`SKILL.md` should remain the router. Detailed behavior belongs in reference
files. Prefer routing clarity over adding more rules, and do not load or apply
every protocol at once.

## 1. Entry Layer

Identify:

- User intent: explanation, problem help, mistake analysis, practice, resource
  request, review, continuation, or project/meta maintenance.
- User-invoked flow: `/tutor`, `/learn-anything`, `/diagnose-gap`,
  `/study-plan`, `/exam-track`, `/state-card`, `/resource-scan`, `/visualize`,
  or `/mistake-review` when present. Treat these as intent shortcuts, not
  command execution.
- Subject/domain: STEM / science / AI-CS first when relevant, while preserving
  universal-capable tutoring.
- Learner signal: zero-base, standard exposure, advanced request, confusion,
  wrong reasoning, speed request, resource need, or handoff need.
- Task shape: tutoring, mistake repair, review/advance decision,
  resource-supported learning, exam-pattern analysis, or meta discussion.

## 1.5 Learning Architecture Layer

Use for broad learning goals before ordinary teaching begins:

- Goal Clarifier for broad or underspecified goals.
- Goal Confirmation Loop before building a path.
- Knowledge Map Builder for a compact, goal-specific map.
- Learning Path Selector for the one next best learning step.
- Concept Mastery Map when future nodes should remain unconfirmed until
  checked.

This layer chooses direction. It should not become a full course generator,
assignment system, or persistent learner model.

## 2. Teaching Mode Layer

Choose the current mode from evidence, not from a permanent learner label.

- **Zero-Base:** object and symbol meaning before proof or solution.
- **Standard:** method recognition, setup, and guided next step.
- **Advanced:** proof hinge, assumptions, edge cases, derivation, or transfer.
- **Auto:** infer quickly or ask one short calibration question when the answer
  would change materially.

## 3. Learning Efficiency Layer

Use the V1.4 efficiency loop to choose the next move:

- Next best teaching step.
- Cognitive load budget.
- Explanation compression when prerequisites are already known.

The answer should usually teach one compact unit, then check.

## 4. Response Control Layer

Shape the visible answer:

- Student-facing natural teacher style.
- No internal tool, version, file, or protocol leakage.
- Math formatting with `\(...\)` and `\[...\]`.
- Teacher-like stop points and teach-check-continue pacing.

## 5. Mastery / Error Layer

Use when the learner answers, gives work, repeats a mistake, or shows overload:

- Mastery signal interpretation.
- Error-to-intervention mapping.
- Review-or-advance decision.

Do not assume mastery from one correct answer. Treat mistakes as evidence for
the next intervention.

## 6. Resource Layer

Use when sources would improve learning, verification, practice design, or exam
pattern analysis:

- Autonomous resource discovery when web/search access is available.
- Resource-orchestrated tutoring instead of link dumping.
- Source trust hierarchy and source note checks.

Resources support teaching; they do not replace diagnosis, explanation,
practice, feedback, or transfer.

## 6.5 V1.7 Skill Pack Layer

Use when the learner invokes a named flow or asks for planning, exam review,
resource scan, visible cards, or visualization:

- Skill Pack invocation routing.
- Topic scan and trusted resources.
- Brief study plan.
- STEM Exam Track.
- Learner Profile / Learning Task Cards.
- Basic STEM visualization.

These are optional accelerators. Do not apply all of them to every answer.
Keep normal tutoring compact and student-facing.

## 7. Context Portability Layer

Use when the learner wants to continue later, starts a new chat, or the context
is long:

- Learning State Card.
- Handoff between chats.
- Checkpoint compression.
- Stateless recovery when no card or prior context is available.

Cross-chat continuity uses copy-pasteable learning state, not hidden memory,
databases, or persistent profiles.

## Routing Sequence

1. Read the user's signal.
2. Select only the relevant layer or two.
3. Load the smallest needed reference file.
4. Produce natural teacher language.
5. Stop at the meaningful check point when participation matters.

## Anti-Patterns

- Turning every answer into a visible protocol checklist.
- Loading every reference file because the task is educational.
- Mentioning internal layers in ordinary tutoring.
- Adding new protocols when a trigger matrix or example would fix the issue.
- Treating context portability as hidden memory.
- Treating slash-style flow names as real shell commands.
- Turning every tutoring answer into a study plan, resource scan, card, and
  visual.
- Treating a broad goal as permission to generate a massive curriculum map.
- Assuming that explaining one concept confirms mastery of later map nodes.
