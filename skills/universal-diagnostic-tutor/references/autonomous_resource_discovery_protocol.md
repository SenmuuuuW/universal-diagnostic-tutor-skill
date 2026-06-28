# Autonomous Resource Discovery Protocol

Use this protocol when the agent environment has web or search access and
external resources would improve teaching, verification, exam-pattern analysis,
misconception repair, or practice design.

Do not depend on users uploading materials. Most learners will only ask a
question. The tutor should infer the knowledge point and decide whether
targeted resource discovery would help.

## When To Search

Search when resources would help with:

- Verifying current programming, tool, API, system, or standard behavior.
- Finding authoritative definitions, examples, theorem statements, or
  documentation sections.
- Designing practice from public problem sets, labs, sample exams, or exercise
  banks.
- Understanding how a concept is commonly tested.
- Finding beginner-friendly explanations for a learner with prerequisite gaps.
- Comparing levels when the learner needs either intuition or formal treatment.

Do not search just to appear more authoritative. If the tutor can teach a small
concept accurately from foundations and no source is needed, teach directly.

## Resource Types To Search For

- Official documentation.
- Official standards or specifications.
- University course notes.
- Public course materials.
- Open textbooks.
- Lecture notes.
- Problem sets, labs, and assignments.
- Past exams or sample exams from legitimate public sources.
- Exercise banks with clear authorship.
- Reputable educational references.
- Authoritative technical references when relevant.

## Source Priority

1. Official documentation or official standards for programming, tools, APIs,
   systems, or technical specifications.
2. University course materials from reputable institutions.
3. Open textbooks and reputable educational books.
4. Public course lecture notes, assignments, labs, and problem sets.
5. Past exams or sample exams from legitimate public sources.
6. Reputable educational references.
7. General web sources only when higher-quality sources are unavailable.

## Search Workflow

1. Identify the current knowledge point.
2. Decide whether external resources are needed.
3. Search with precise queries: topic, course level, source type, and desired
   role such as "lecture notes," "problem set," "official docs," or "past
   exam."
4. Select the most relevant and trustworthy sources.
5. Prefer exact pages, chapters, lecture numbers, assignment names,
   documentation sections, or problem-set pages.
6. Identify each source's teaching role:
   - definition
   - theorem
   - example
   - intuition
   - proof or derivation
   - implementation detail
   - common exercise type
   - exam pattern
   - misconception
   - practice set
7. Teach in the tutor's own words.
8. Cite or name the source clearly.
9. Give a small check or practice task.
10. Recommend next resources only if helpful.

## Search Query Patterns

- `site:edu linear algebra span basis problem set`
- `matrix multiplication composition linear transformations lecture notes`
- `conditional probability problem set university`
- `Python official documentation list append`
- `recursion base case lecture notes data structures`
- `gradient descent derivatives optimization open textbook`

Use equivalent precise queries for non-STEM subjects: official grammar guides,
primary-source archives, writing center materials, public civics explainers,
or reputable historical references.

## If Source Access Is Unavailable

Say so clearly and continue teaching from internal knowledge:

```text
I can teach this from foundations, but I cannot verify external sources in this
environment. I will avoid naming specific sources I have not checked.
```

Then give source categories the learner can look for later rather than
invented titles or links.

## Source Safety Rules

- Do not fabricate resources, titles, authors, institutions, page numbers,
  links, exams, or citations.
- Do not cite sources not actually used.
- Do not dump links.
- Do not copy substantial source content.
- Avoid pirated PDFs, answer-only sites, SEO farms, low-quality forums, and
  uncited solution dumps.
- If sources disagree or vary in level, choose the one most appropriate for the
  learner's current level and state the limitation.
- Keep resources in a support role; they should improve teaching, not replace
  diagnosis, explanation, checks, or practice.
