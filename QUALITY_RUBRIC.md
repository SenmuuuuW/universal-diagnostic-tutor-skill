# Quality Rubric

Use this rubric when reviewing tutoring outputs, acceptance tests, or real user
feedback for `universal-diagnostic-tutor`. Score each dimension from 1 to 5.

## Domain Diagnosis

- **1:** No subject or task orientation.
- **2:** Names a broad subject but misses the useful subtopic.
- **3:** Identifies the main domain, but the map is generic.
- **4:** Names subject, subtopic, and core concept compactly.
- **5:** Uses domain diagnosis to choose the right first teaching step without
  creating a roadmap.

## Knowledge Gap Diagnosis

- **1:** Gives an answer with no gap diagnosis.
- **2:** Guesses a gap but does not adapt the explanation.
- **3:** Identifies a plausible gap such as notation or concept.
- **4:** Matches the response to the gap.
- **5:** Distinguishes surface error from underlying gap and updates the next
  move from learner evidence.

## Next Best Teaching Step

- **1:** Solves everything or lectures broadly.
- **2:** Chooses a helpful topic but too much content.
- **3:** Gives a useful step but also unnecessary material.
- **4:** Chooses the main blocker and teaches it.
- **5:** Chooses the smallest step that unlocks progress and stops at the right
  place.

## Cognitive Load Control

- **1:** Overwhelms the learner.
- **2:** Adds several new ideas before checking.
- **3:** Mostly appropriate, with some extra load.
- **4:** Fits load to Zero-Base, Standard, or Advanced Mode.
- **5:** Uses exactly enough terminology, notation, and practice for the current
  learner signal.

## Student-Facing Naturalness

- **1:** Sounds like a checklist, tool, or policy document.
- **2:** Uses stiff labels or over-explains the plan.
- **3:** Understandable but templated.
- **4:** Warm, clear, and teacher-like.
- **5:** Natural, concise, and responsive to the learner's wording and language.

## Stop Point Discipline

- **1:** Gives the final answer despite hints-only or participation request.
- **2:** Asks a check but answers it immediately.
- **3:** Includes a stop point but after too much work.
- **4:** Pauses at a meaningful step.
- **5:** Stops at the highest-value diagnostic point and waits.

## Mastery Signal Interpretation

- **1:** Treats right/wrong as the only signal.
- **2:** Misreads guesses, partial answers, or overload.
- **3:** Notices the signal but response is broad.
- **4:** Uses the signal to review, advance, compress, or step down.
- **5:** Preserves correct parts, repairs weak parts, and chooses the next move
  from evidence.

## Error-To-Intervention Match

- **1:** Responds to every error with a full solution.
- **2:** Corrects the answer but not the reason.
- **3:** Identifies an error type but intervention is generic.
- **4:** Matches notation, concept, method, setup, proof, calculation, or
  transfer error to a useful repair.
- **5:** Explains why the wrong path was tempting and gives a targeted near
  practice item.

## Explanation Compression

- **1:** Ignores what the learner already knows.
- **2:** Compresses into a bare answer.
- **3:** Skips some basics but still spends time on known material.
- **4:** Trusts known prerequisites provisionally and focuses on the blocker.
- **5:** Compresses precisely while preserving the key reasoning and a check.

## Transfer Pattern Teaching

- **1:** Ends after the answer.
- **2:** Gives a vague "practice more" suggestion.
- **3:** Names a cue but not the trap or variation.
- **4:** Provides a reusable clue, method, and trap.
- **5:** Gives a concise near-transfer prompt matched to current mastery.

## Resource Use Quality

- **1:** Fabricates or uses weak sources.
- **2:** Dumps links without teaching.
- **3:** Uses acceptable sources but integration is shallow.
- **4:** Uses trusted resources to support explanation, verification, or
  practice.
- **5:** Orchestrates resources into a teaching path while keeping the tutor's
  explanation primary.

## Math Formatting

- **1:** Uses raw dollar math or formula-only code blocks throughout.
- **2:** Mixed formatting with several user-facing rendering problems.
- **3:** Mostly rendered correctly, with minor inconsistency.
- **4:** Uses `\(...\)` and `\[...\]` in normal math explanations.
- **5:** Formatting is reliable, readable, and code blocks are reserved for
  actual code or intentional bad examples.

## No Internal Leakage

- **1:** Mentions internal protocols, file names, versions, or tool execution in
  ordinary tutoring.
- **2:** Leaks one internal label that distracts from teaching.
- **3:** Mostly natural but slightly process-heavy.
- **4:** No internal leakage.
- **5:** Converts internal routing into natural teacher language.

## Context Portability

- **1:** Pretends to remember unavailable prior chats or loses context.
- **2:** Forces a full restart even when the user provides context.
- **3:** Uses some provided context but misses the next best step.
- **4:** Uses a Learning State Card or summary to continue without restarting.
- **5:** Produces or consumes compact handoff context, trusts known items
  provisionally, and checks one next step before advancing.
