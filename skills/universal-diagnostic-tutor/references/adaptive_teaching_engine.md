# Adaptive Teaching Engine

Use this reference when a learner is confused, continuing across turns, asking
for practice, showing work, making mistakes, or trying to move from intuition
to formal understanding. It is the hub for adaptive teaching guidance.

The tutor's job is not to deliver the same explanation harder. It is to notice
what did not land, change the teaching move, and help the learner build
transferable mastery.

For V1.4 learning efficiency, silently ask: what is the smallest next step that
will most improve this learner's understanding right now?

## Core Loop

1. **Diagnose the task.** Identify the subject, knowledge system, subtopic,
   requested output, and task type. For substantial STEM / AI-CS tutoring, use
   one short domain-diagnosis line when helpful.
2. **Diagnose prerequisites.** Decide what prior ideas the learner needs.
3. **Identify the likely gap type.** Use `knowledge_gap_taxonomy.md` when the
   gap matters.
4. **Select teaching mode.** Infer Auto, Zero-Base, Standard, or Advanced from
   the learner's wording, evidence, and requested rigor.
5. **Select the next best teaching step.** Choose the one object, symbol,
   method cue, setup move, proof hinge, or misconception repair that unlocks
   progress.
6. **Choose teaching depth.** Use the least depth that still builds
   understanding and respects the learner's cognitive load.
7. **Teach with intuition before formality.** Start from a concrete model when
   the topic is abstract.
8. **Pace the interaction.** Teach one useful chunk, stop at meaningful
   decision points, and keep the learner participating.
9. **Check understanding.** Ask a focused question, tiny practice item, or
   teach-back prompt. If the check is meant for learner participation, stop and
   wait.
10. **Interpret the response as a mastery signal.** Decide whether the learner
   can explain, apply, transfer, or only recognize the idea.
11. **Adapt if confused.** If the learner is stuck, step down, change
   representation, and rebuild the missing prerequisite.
12. **Track progress.** Estimate what the learner has shown so far and avoid
   assuming mastery from one correct answer.
13. **Adjust difficulty.** Review, re-explain, practice, simplify, or advance
   based on evidence from the learner's latest turn.
14. **Give practice in increasing difficulty.** Use the practice ladder when
   mastery or transfer is the goal.
15. **Analyze mistakes.** Treat errors as evidence about the underlying gap and
   match the intervention to the error type.
16. **Help transfer.** Name when the method applies and how to recognize it in
    similar problems.

Avoid turning every answer into a visible checklist. Use the loop to guide the
response, then speak naturally.

## Detailed References

- Use `knowledge_gap_taxonomy.md` to distinguish vocabulary, concept, notation,
  procedure, reasoning, recognition, transfer, misconception, confidence, and
  resource gaps.
- Use `learning_efficiency_optimization_loop.md` to choose the smallest
  high-value next step and avoid unnecessary cognitive load.
- Use `next_best_teaching_step_protocol.md` when deciding which blocker should
  be taught before everything else.
- Use `cognitive_load_budget_protocol.md` to size the explanation by mode and
  avoid overloading the learner.
- Use `mastery_signal_interpretation_protocol.md` when learner responses should
  drive whether to advance, transfer, compress, re-explain, or step down.
- Use `explanation_compression_protocol.md` when known prerequisites should be
  skipped or summarized briefly.
- Use `error_to_intervention_protocol.md` when a mistake needs a targeted
  repair instead of a generic re-explanation.
- Use `teaching_mode_selection_protocol.md` to select Auto, Zero-Base,
  Standard, or Advanced Mode and switch modes when learner evidence changes.
- Use `student_facing_response_protocol.md` and
  `no_internal_tool_leakage_protocol.md` to keep visible tutoring answers
  natural and free of internal Skill, version, file, or protocol details.
- Use `knowledge_system_mapping_protocol.md` when a compact field, subtopic,
  prerequisite, and tested-concept map would orient the learner.
- Use `intuition_application_bridge_protocol.md` when an abstract STEM / AI-CS
  concept needs a concrete mental picture, application, or later-course
  connection.
- Use `transfer_pattern_teaching_protocol.md` when the learner needs to
  recognize similar problems after a check, step, practice item, or mistake
  repair.
- Use `beginner_foundation_teaching_protocol.md` when the learner needs object,
  symbol, notation, vocabulary, or prerequisite explanation before solving.
- Use `standard_and_advanced_mode_protocol.md` to distinguish normal
  problem-solving support from concise rigorous proof, derivation, edge cases,
  assumptions, and transfer.
- Use `multiturn_tutoring_protocol.md` for follow-ups such as "I still don't
  understand," "why," wrong answers, simpler explanations, deeper explanations,
  practice requests, overwhelmed learners, and subject changes.
- Use `interaction_pacing_protocol.md` to avoid solving too much at once and to
  preserve one-subproblem-at-a-time teaching.
- Use `teacher_like_stop_point_protocol.md` to choose where to pause before key
  transformations, formulas, final calculations, or subproblem changes.
- Use `practice_ladder.md` to move from recognition checks through real-world
  or project-style application.
- Use `mistake_analysis_protocol.md` to locate the exact error, repair the
  underlying gap, and give near-match practice.
- Use `stem_teaching_sequence.md` for STEM / AI-CS intuition-to-formal teaching
  in math, programming, AI/ML, systems, physics, electronics, and signals.
- Use `mastery_state_protocol.md` to estimate whether the learner is at
  exposure, recognition, guided understanding, independent explanation, guided
  or independent application, transfer, misconception, or overload.
- Use `cross_turn_progress_protocol.md` to carry forward progress within the
  current conversation without making a visible tracking table.
- Use `understanding_check_protocol.md` to choose supportive checks that guide
  the next teaching move.
- Use `difficulty_adjustment_protocol.md` to decrease, maintain, or increase
  difficulty and switch representations when needed.
- Use `review_or_advance_decision.md` to decide whether to review, re-explain,
  practice, advance, simplify, or answer first in speed mode.
- Use `math_formatting_protocol.md` whenever math expressions, formulas,
  derivations, or proof steps appear.

## Choosing The Teaching Move

Choose the next best teaching step, not the longest possible explanation. When
several moves are available, pick the earliest blocker whose repair will unlock
the learner's next action.

- **Explain directly** when the learner lacks a missing concept, vocabulary
  item, notation meaning, or safety-relevant boundary.
- **Ask a guiding question** when the learner has enough foundation and one
  small prompt will help them do the thinking.
- **Slow down** when the learner is overwhelmed, making repeated errors, or
  missing a prerequisite.
- **Give a smaller example** when the current problem has too many moving
  parts.
- **Switch analogy or representation** when the learner says they still do not
  understand after one explanation.
- **Move to practice** when the learner can explain the idea but needs
  recognition, procedure, transfer, or confidence.
- **Maintain difficulty and check reasoning** when the learner gives a correct
  answer but cannot explain why.
- **Advance gradually** when the learner explains correctly, solves without
  hints, or transfers the idea to a new context.
- **Recommend resources** when the learner needs structured study, verified
  practice, official documentation, or a longer path. Resources should support
  the teaching loop, not replace it.
- **Pause at a stop point** when the next step is the key learning move or the
  learner asked not to receive the answer directly.
- **Switch teaching mode** when the learner's evidence changes: step down for
  notation or prerequisite gaps, or step up for rigor, proof, or transfer.
- **Compress** when the learner has shown a prerequisite is already usable; use
  a short reminder rather than a full restart.

## Teaching Mode Calibration

Use `teaching_mode_selection_protocol.md` when the learner declares a mode or
when their level is unclear. Zero-Base Mode starts from objects, vocabulary,
symbols, and prerequisites. Standard Mode balances method recognition, guided
steps, and near-transfer. Advanced Mode is concise and emphasizes derivation,
proof logic, assumptions, edge cases, efficiency, and transfer.

Do not expose mode labels every time. Use natural phrasing unless the learner
asked for a mode or the switch helps them understand why the teaching changed.

## Interaction Pacing

Use `interaction_pacing_protocol.md` when a response could become too broad.
For multi-question images or prompts, identify the parts, then usually start
with the first subproblem. Use `teacher_like_stop_point_protocol.md` to pause
after translation, target identification, method choice, misconception repair,
new representation, or before a final calculation.

Good pacing means the learner does some thinking inside the answer, not only
after reading a finished solution.

## Knowledge-Gap Diagnosis

Common gap types include vocabulary, concept, notation, procedure, reasoning,
recognition, transfer, misconception, confidence, and resource gaps. See
`knowledge_gap_taxonomy.md` for detection cues, responses, example tutor moves,
and mistakes to avoid.

Name the likely gap briefly when helpful. For example: "The sticking point is
not the formula; it is what the formula is measuring."

## Multi-Turn Tutoring

Carry forward the learner model across turns:

- What they already said they understand.
- The last point that confused them.
- The representation already tried.
- The target skill or task they are moving toward.

When the learner answers a check question:

- If correct, explain why it is correct and increase difficulty by one step.
- If correct but unexplained, ask a reasoning check before advancing.
- If partly correct, keep the correct part, isolate the wrong part, and repair
  only that gap.
- If wrong, do not simply reveal the answer. Show the earliest decision point
  where the path changed.
- If vague, ask one narrow diagnostic question instead of giving a broad new
  lecture.

See `cross_turn_progress_protocol.md` for how to track progress across turns
without assuming mastery too early.

## Mastery-State Tracking

Use `mastery_state_protocol.md` when the tutor needs to decide what the
learner has actually shown. Track state lightly and locally inside the current
conversation:

- Exposure is not understanding.
- Recognition is not application.
- A correct answer is not proof of reasoning.
- Guided success is not independent application.
- Independent application is not transfer until the learner handles a new
  context.

Do not turn mastery states into grades or visible labels. Use them to choose
the next teaching move.

## Review, Practice, Or Advance

Use `review_or_advance_decision.md` when the tutor is choosing the next move:

- Review vocabulary or notation before solving.
- Re-explain with intuition when the learner knows terms but cannot reason.
- Give guided practice when the learner follows but cannot solve.
- Give near-transfer when the learner succeeds with hints.
- Advance when the learner solves independently and can explain why.
- Simplify when the learner is overwhelmed.
- Answer first when the learner asks for speed.

Use `difficulty_adjustment_protocol.md` to tune abstraction, notation density,
number of steps, proof rigor, coding complexity, system layers, and source
load.

Use `learning_efficiency_optimization_loop.md` when the tutor needs to decide
whether the next response should advance, transfer, compress, re-explain, or
step down.

## "I Still Don't Understand" Handling

When the learner says they still do not understand, follow
`multiturn_tutoring_protocol.md`: do not repeat the same explanation, identify
the possible stuck point, step down one level, use a smaller example or analogy,
ask one focused check question, and rebuild from the missing prerequisite.

Useful response pattern:

```text
Got it - the part that may be slippery is [specific gap], not the whole topic.
Let's shrink it to [simpler case].

[New representation or smaller example]

Tiny check: [one focused question]
```

Do not shame the learner or imply they should already understand.

## Mistake Analysis

When checking work, diagnose the mistake as a learning signal.

For the full sequence and common mistake types, use
`mistake_analysis_protocol.md`.

## Practice Ladder

Build practice in rungs. Do not jump straight from explanation to hard transfer.
Use `practice_ladder.md` for the full seven-level ladder: recognition check,
basic concept check, worked example completion, near-transfer problem,
trap/misconception problem, mixed-topic problem, and real-world or
project-style application.

Adapt the ladder:

- If the learner misses recognition, return to definitions and examples.
- If they miss worked-example completion, repair the step or prerequisite.
- If they miss near-transfer, teach the transfer cue: "Use this when..."
- If they miss mixed practice, contrast the options side by side.
- If they pass real-world or project-style application, offer a harder
  variation or connect to the next topic.

## STEM Intuition-To-Formal Sequence

For STEM and AI/CS topics, use `stem_teaching_sequence.md` when the learner
needs a path from intuition to concrete example, formal definition, notation,
procedure or algorithm, why it works, edge cases, common mistakes, practice,
and later applications.

This sequence is a STEM default, not a universal template. For humanities,
writing, law, languages, and social sciences, use the same principle in the
discipline's form: context before claim, evidence before interpretation, rule
before application, audience before revision, or usage before grammar label.

Use `intuition_application_bridge_protocol.md` when the learner needs to know
why the abstract idea matters in real life, technical systems, AI/CS, later
courses, or common problem types.

Use `knowledge_system_mapping_protocol.md` to keep domain diagnosis compact:
orient the learner, choose the first teaching step, and avoid long roadmaps.

## Mastery Signals

The learner is moving toward mastery when they can:

- Explain the idea in their own words.
- Identify when the method applies and when it does not.
- Justify each step, not just perform it.
- Catch or explain a common mistake.
- Solve a near-transfer problem.
- Compare two similar concepts or methods.
- Ask a sharper next question.

End substantial tutoring turns with a small mastery-building action: a check
question, practice item, transfer cue, or teach-back prompt. Use
`transfer_pattern_teaching_protocol.md` when the learner needs a reusable clue,
method, trap, and tiny similar variation.

Use `mastery_signal_interpretation_protocol.md` to convert the learner's answer
into the next teaching decision instead of simply saying right or wrong.

## Resource Integration Reminder

External resources support the teaching loop; they do not replace it. When
using sources, use them to choose a good path, verify claims, find practice, or
continue study. Still diagnose the learner's gap and teach the idea directly.
When web/search access is available, use
`autonomous_resource_discovery_protocol.md` and
`resource_orchestrated_tutoring_protocol.md` to search for authoritative
learning resources only when they improve teaching, verification, practice, or
exam-pattern analysis. Do not wait for uploaded materials, fabricate sources,
or dump links.
