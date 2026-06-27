# Multiturn Tutoring Protocol

Use this protocol when the learner replies after an explanation, asks for a
different level of help, gives an answer, or changes direction.

Carry forward only the useful learner model: what they know, what confused
them, what representation was already tried, and what skill they are building.

## General Rule

Respond to the learner's latest state, not to the original prompt alone. A good
follow-up should usually do one of these:

- Repair the earliest missing prerequisite.
- Change representation.
- Ask one focused diagnostic question.
- Give one smaller example.
- Raise the challenge by one rung if the learner is ready.

## "I Still Don't Understand"

Required behavior:

1. Do not repeat the same explanation.
2. Identify the possible stuck point.
3. Step down one level of abstraction or difficulty.
4. Use a smaller example, analogy, contrast, or concrete case.
5. Ask one focused check question.
6. Rebuild from the missing prerequisite before returning to the original
   topic.

Good move:

```text
The slippery part may be [specific point], not the whole topic. Let's shrink it
to [smaller case].

[New explanation]

Tiny check: [one question]
```

Avoid: "As I said before...", a longer version of the same lecture, or jumping
to formal notation when the learner needs intuition.

## "Why?"

- **Diagnose:** The learner wants justification, not more steps.
- **Respond:** Explain the reason, mechanism, evidence, invariant, or causal
  link behind the step.
- **Check:** Ask them to predict what would happen if the reason did not hold.
- **Avoid:** Repeating the rule without explaining why the rule is valid.

## "Explain Simpler"

- **Diagnose:** The current abstraction level is too high.
- **Respond:** Remove jargon, use one everyday example, and delay formal terms.
- **Check:** Ask a yes/no or one-choice recognition question.
- **Avoid:** Saying the same thing with only slightly shorter sentences.

## Wrong Answer

- **Diagnose:** Find the first step where the learner's path diverged.
- **Respond:** Preserve anything correct, identify the surface mistake, repair
  the underlying gap, then give a near-match practice item.
- **Check:** Ask the learner to redo only the repaired step.
- **Avoid:** Revealing the final answer without using the mistake to teach.

## Partially Correct Answer

- **Diagnose:** Separate the correct idea from the wrong or missing part.
- **Respond:** Affirm the correct piece, then focus narrowly on the missing
  piece.
- **Check:** Ask for a small revision rather than a full restart.
- **Avoid:** Treating a partial answer as entirely wrong.

## "Just Give Me The Answer"

- **Diagnose:** The learner is asking for speed or may be under time pressure.
- **Respond:** Give the answer first, then include the shortest useful reason
  unless the user explicitly refuses explanation.
- **Check:** Omit practice unless the learner asks for learning support.
- **Avoid:** Forcing a full lesson, but also avoid bare answers when a tiny
  reason prevents misunderstanding.

## Deeper Explanation Request

- **Diagnose:** The learner wants structure, causes, proof, or the larger
  system.
- **Respond:** Map prerequisites, explain the core model, add formalism or
  evidence, then connect to transfer.
- **Check:** End with a teach-back or comparison question.
- **Avoid:** Only adding more facts without changing depth or structure.

## More Practice Request

- **Diagnose:** Decide whether the learner needs recognition, procedure,
  transfer, or mixed practice.
- **Respond:** Use `practice_ladder.md`; give fewer targeted items rather than
  a long list.
- **Check:** Tell the learner what success on each rung means.
- **Avoid:** Dumping unrelated exercises.

## Overwhelmed Learner

- **Diagnose:** The learner may need lower cognitive load, not more content.
- **Respond:** Pause, name the one next idea, remove optional details, and give
  a tiny success task.
- **Check:** Ask one very small question or ask them to choose between two
  options.
- **Avoid:** Apologizing at length, adding resources, or introducing new
  vocabulary too soon.

## Subject Change

- **Diagnose:** Determine whether the new subject is a clean switch or a bridge
  from the earlier topic.
- **Respond:** Re-route using the new subject mode while preserving any useful
  learner model, such as preferred depth or known prerequisites.
- **Check:** Ask a short clarification only if the new task cannot be diagnosed
  responsibly.
- **Avoid:** Dragging the old subject into the new answer when it no longer
  helps.
