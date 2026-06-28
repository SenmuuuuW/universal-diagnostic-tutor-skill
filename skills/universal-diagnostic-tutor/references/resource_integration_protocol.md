# Resource Integration Protocol

Use this protocol when a learning answer would benefit from external learning
resources. For the current primary use case, university-level STEM and AI/CS
study questions should default to resource-augmented answering when web access
is available.

This protocol adds resources to the diagnosis-first workflow; it does not
replace the tutor's responsibility to teach.

For active web/search behavior, use `autonomous_resource_discovery_protocol.md`.
For turning searched, curated, or user-provided sources into tutoring, use
`resource_orchestrated_tutoring_protocol.md`.

## When To Look Up Resources

Look up resources when the user asks about:

- University-level STEM, AI, CS, math, physics, electronics, or engineering.
- Course study plans, prerequisite chains, exams, problem sets, or exercises.
- Official documentation, standards, APIs, algorithms, or technical methods.
- A topic where current source links would help the learner continue studying.
- Conflicting explanations, named courses, named textbooks, or source requests.

When web/search access is available and resources would improve the answer, do
not wait for the learner to upload materials. Infer the knowledge point and
search for authoritative learning resources.

Use internal explanation without search when the user asks for a quick concept
check and no external source is needed. Still offer to use sources if the
learner wants a study path.

## Source Selection

Prefer sources in this order:

1. Official documentation or official course material.
2. University course pages and open courseware.
3. Textbooks and open textbooks.
4. Past exams, official question banks, and problem sets.
5. Peer-reviewed or authoritative technical sources when needed.
6. Reputable public courses and tutorials.
7. Other sources only when clearly useful and reliable.

See `source_trust_hierarchy.md` for detailed trust signals and red flags.

## Distinguish Internal And Source-Backed Explanation

When sources are used, make the separation clear:

- **Tutor diagnosis:** what the learner likely needs.
- **Source note:** which sources were used and why they are relevant.
- **Teaching path:** the tutor's synthesized explanation.
- **Source list:** links or source names for further study.

Do not present an internal explanation as if it came from a source. Do not
claim a source says something unless it was actually checked.

## Citation And Source Listing

When external resources are used:

- Cite or list source names and links when available.
- Prefer links that help the learner continue studying independently.
- Keep quotes minimal; summarize in original wording.
- If sources disagree, name the disagreement and teach the likely reason.
- If sources are insufficient, say so clearly.

## If Sources Are Unavailable

If internet access is unavailable or search fails:

- Say that external sources could not be verified in this environment.
- Answer from foundations if possible.
- Avoid pretending to have searched.
- Offer a source checklist the learner can use later.

Example wording: "I can explain this from foundations, but I could not verify
external course resources in this environment."

## No Hallucinated Sources

Never invent:

- Textbook titles or editions.
- Past exam papers.
- Course pages.
- Links.
- Papers.
- Official standards.
- Lecture notes.

If a source is uncertain, label it as uncertain or leave it out.

## Turn Sources Into A Teaching Path

Do not dump summaries. Use sources to support a path:

1. Diagnose subject, topic, and prerequisite gap.
2. Explain why the selected sources are relevant.
3. Teach the foundation in plain language.
4. Work step by step through the concept or problem.
5. Identify common exam or problem-set patterns.
6. Name common mistakes.
7. Suggest a learning path.
8. Suggest practice direction.
9. List sources.

Use `exam_pattern_resource_analysis.md` when public exams, problem sets, or
exercise sources can clarify tested concepts, traps, recognition cues, and
practice priorities.

## Exam And Problem-Set Analysis

When resources include exams or problem sets, analyze:

- Tested concept.
- Prerequisite knowledge.
- Common question pattern.
- Common traps.
- Why the correct method works.
- How to recognize similar problems.
- What to practice next.

Avoid simply giving answers. Teach the reusable method.

## STEM And AI/CS Emphasis

For STEM and AI/CS topics, connect:

- Mathematical foundations.
- Conceptual intuition.
- Formal definitions.
- Algorithmic thinking.
- Implementation meaning.
- Real-world application.
- Relation to later courses.
- Prerequisite chains.

Examples:

- Machine learning: connect linear algebra, probability, optimization, and
  programming.
- Operating systems: connect hardware, processes, memory, concurrency, and
  system design.
- Networks: connect protocols, layering, reliability, routing, and real
  applications.
- Data structures: connect abstract operations, complexity, implementation, and
  use cases.
- Calculus and linear algebra: connect formulas with geometric or computational
  meaning.
- Physics, electronics, and signal processing: connect phenomena, models,
  equations, experiments, and engineering use.
