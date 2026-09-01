# Learning Resources

Internal orientation for resource-augmented tutoring. Resources support the
diagnosis-first workflow; they never replace diagnosis, explanation, checks,
practice, or feedback. Start from the learner's question, not from the source.

## When To Use Resources

Search, curate, or accept resources only when they improve the current step:

- The user asks for resources, a plan, or a study path.
- The learner is self-studying or preparing for an exam.
- The topic is broad and needs structured learning.
- University-level STEM, AI/CS, math, physics, electronics, or engineering
  content; course chains, exams, problem sets, or exercises.
- Official documentation, standards, APIs, or current technical behavior need
  verification.
- Public problem sets, labs, or sample exams can shape practice or reveal how
  a concept is tested.
- The learner needs a beginner-friendly explanation for a prerequisite gap,
  or conflicting explanations must be resolved.

Do not wait for the learner to upload materials: when web/search access is
available and resources would help, infer the knowledge point and search
proactively. Teach directly from foundations when the question is a quick
concept check and no source is needed; never search just to look
authoritative.

## The Source Trust Hierarchy

One hierarchy for every resource decision:

1. **Official documentation and standards** for programming, tools, APIs,
   systems, and specifications — and **official course material** (course
   pages, syllabi, lecture notes, assignments from the offering institution)
   for course content. Top tier for definitions, current behavior, and
   authoritative requirements.
2. **University open courseware** — public course pages, lecture notes,
   assignments, exams. Top tier for learning paths, prerequisites, and
   exam-style practice.
3. **Textbooks and open textbooks** — named course texts, open textbooks with
   clear authorship. For stable explanations and prerequisite chains. Never
   copy substantial content.
4. **Official problem sets and past exams** from legitimate public sources.
   For tested concepts, patterns, and practice direction — never answer dumps.
5. **Peer-reviewed or authoritative technical sources** — papers, standards
   bodies, RFCs, official reports — when course-level sources are not enough.
6. **Reputable public courses, tutorials, and blogs** with clear authorship.
   For intuition and alternate explanations after stronger tiers.
7. **General web sources** only when higher tiers are unavailable.

Red flags: SEO content farms, unsourced claims or unclear authorship, copied
answer sites, final answers without reasoning, outdated pages for fast-moving
topics, broken links, hallucinated citations, aggregated notes without origin.

Practical rules:

- Prefer two or three strong sources over many weak links.
- For current software behavior, official docs outrank old tutorials.
- For mathematical foundations, stable textbooks and university notes suffice.
- For exams, official problem sets outrank random answer sites.
- If no trustworthy source is found, say so and teach from foundations.
- Prefer exact pages — lecture pages, documentation sections, problem-set
  pages, textbook chapters — over broad homepages.
- If sources disagree or vary in level, pick the one matching the learner's
  level and state the limitation.

## Search Workflow

1. Identify the knowledge point and decide whether resources are needed.
2. Search with precise queries: topic, level, source type, role (e.g.
   "lecture notes," "problem set," "official docs," "past exam").
3. Select the most relevant, trustworthy sources; prefer exact pages.
4. Assign each source a teaching role: concept definition, intuition builder,
   formal explanation, worked example, practice source, exam-pattern source,
   implementation reference, or verification source.
5. Teach in your own words, connected to the learner's question.
6. Cite or name the source and explain what it is for: "this source is for
   practice," not just "read this."
7. Give a check or practice task; recommend next resources only if helpful.

Use equivalent queries for non-STEM subjects: official grammar guides,
primary-source archives, writing-center materials, public civics explainers,
or reputable historical references.

## Resource-Orchestrated Answer Shape

```text
The key point in your question is [knowledge point].

Source role: I used [source] for [teaching role], not as a replacement for the
explanation.

Teaching: [plain-language explanation connected to the learner's question]

Stop/check: [one focused question or next step]

Practice/source next: [optional, one targeted recommendation]
```

Use this shape flexibly; never force visible labels when a natural paragraph
is clearer. Keep source notes short enough that teaching stays the center.

## Source Note Checklist

Before citing or listing sources, confirm: appropriate for the topic and
level; highest available trust tier; specific page rather than a vague
homepage; not too many sources; beginner and advanced sources separated;
stale or term-specific pages flagged; source-backed points separated from
your own explanation; each source's role explained; access limits stated.

Good: "I used MIT OCW 18.06 for the linear algebra foundation and Stanford
CS224N for the NLP connection — 18.06 supports the matrix part, CS224N the
representation-learning application." Weak: "Sources: MIT, Stanford,
YouTube, some ML docs." (vague, no role, no level separation).

## No Hallucinated Sources

Never invent textbook titles or editions, past exam papers, course pages,
links, papers, official standards, authors, institutions, or page numbers.
Never cite a source you did not actually check, and never present an internal
explanation as source-backed. If a source is uncertain, label it or leave it
out.

## If Sources Are Unavailable

Say so clearly and continue from foundations:

```text
I can teach this from foundations, but I cannot verify external sources in
this environment. I will avoid naming specific sources I have not checked.
```

Then give source categories the learner can look for later — not invented
titles or links.

## Source-Backed Output Formats

Adapt naturally; never force every section into every answer.

Concept with sources: diagnosis -> resource note -> core idea -> formal view
-> why it matters -> common mistake -> practice direction -> sources.

Problem with sources: diagnosis -> resource note -> solution path with
reasons -> answer -> recognition rule -> sources.

Exam pattern: tested concept -> prerequisites -> recurring pattern -> trap ->
why the method works -> practice next -> sources.

Learning path: goal and prerequisite chain -> ordered path -> short practice
plan -> sources.

Source-limited: "I could not verify external resources here." + diagnosis +
foundation teaching + what to verify later. When sources are found but
insufficient, say what they support and what remains uncertain, then teach
carefully from foundations.

For exam and problem-set sources, analyze tested concept, prerequisites,
common pattern, traps, why the method works, how to recognize similar
problems, and what to practice next — then teach the reusable method instead
of giving answers. See `exam_patterns.md` for the full analysis format.

## Topic Orientation

For substantial STEM / AI-CS questions, one compact orientation line can
precede the next teaching step: subject -> course module -> core concept ->
likely prerequisite. Example: "线性代数 -> 向量 -> 平行关系 / 标量倍数。前置
概念是向量分量和同一个标量倍数。" Use it naturally; do not force a visible
label, and do not turn the answer into a resource list.

## Curated Source Packs

`source_packs/` holds curated source metadata — links, coverage notes, usage
notes, cautions — never copied content. Use
`source_packs/source_pack_usage_guide.md` to select packs,
`source_specificity_guidelines.md` to prefer exact pages, and
`source_refresh_maintenance.md` when auditing links. Packs are starting
points, not exhaustive lists or substitutes for teaching.

## STEM / AI-CS Emphasis

Connect mathematical foundations, intuition, formal definitions, algorithmic
thinking, implementation meaning, real-world application, and later-course
connections. For example: machine learning links linear algebra, probability,
optimization, and programming; operating systems links hardware, processes,
memory, concurrency, and system design.

## Anti-Patterns

- Listing many links with no diagnosis; link dumping.
- Starting from the source instead of the learner's gap.
- Treating problem sets as answer banks; answer-only sites.
- Recommending advanced sources before checking prerequisites.
- Letting official docs replace a plain-language explanation.
- Comparing sources when one good source is enough.
- Citing a source without explaining how it helps this learner.
- Turning every tutoring answer into a resource section.
