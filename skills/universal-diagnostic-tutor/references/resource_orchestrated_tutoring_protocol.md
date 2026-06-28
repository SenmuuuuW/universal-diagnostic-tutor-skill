# Resource-Orchestrated Tutoring Protocol

Use this protocol when resources come from autonomous web/search discovery,
curated source packs in this repo, or user-provided materials. User-provided
materials are useful when available, but they are not the default assumption.

Resource-orchestrated tutoring means turning sources into teaching. It is not
link collection.

## Core Principle

Start from the learner's question, not from the source.

The tutor should:

1. Diagnose the learner's current question and likely gap.
2. Select one to three resources only when they add value.
3. Identify each resource's teaching role.
4. Translate source material into learner-friendly explanation.
5. Connect the source to the current problem.
6. Give a stop point, check, or practice task.
7. Mention next resources only if they help the learner continue.

## Teaching Roles For Sources

For each resource, decide its role before using it:

- **Concept definition:** Provides a reliable definition or terminology.
- **Intuition builder:** Offers a visual, concrete, or beginner-friendly model.
- **Formal explanation:** Gives theorem, proof, derivation, or exact rule.
- **Worked example:** Shows a solved pattern the tutor can adapt.
- **Practice source:** Provides exercises, labs, or problem sets.
- **Exam-pattern source:** Shows how the topic is tested.
- **Implementation reference:** Gives official behavior for code, APIs, tools,
  protocols, or systems.
- **Verification source:** Confirms a technical claim or current behavior.

## How To Integrate Sources

- Use official documentation when teaching programming, tools, APIs, protocols,
  or technical specifications.
- Use university notes, open textbooks, or course materials for stable
  foundations.
- Use public problem sets or past exams to identify common patterns and traps.
- Compare multiple sources only when it helps level-match or resolve a
  disagreement.
- Explain what the resource is for: "This source is for practice," not only
  "read this."
- Turn source examples into one small practice item rather than summarizing the
  whole source.
- Keep source notes short enough that the teaching remains the center.

## Resource-Orchestrated Answer Shape

```text
The key point in your question is [knowledge point].

Source role: I used [source] for [teaching role], not as a replacement for the
explanation.

Teaching: [plain-language explanation connected to the learner's question]

Stop/check: [one focused question or next step]

Practice/source next: [optional, one targeted recommendation]
```

Use this shape flexibly. Do not force visible labels when a natural paragraph
is clearer.

## Anti-Patterns

- Listing many links with no diagnosis.
- Starting the answer by summarizing sources before naming the learner's gap.
- Treating a problem set as an answer bank.
- Recommending advanced sources before checking prerequisites.
- Letting official docs replace a plain-language explanation.
- Comparing sources when one good source is enough.
- Citing a source broadly without explaining how it helps this learner.
