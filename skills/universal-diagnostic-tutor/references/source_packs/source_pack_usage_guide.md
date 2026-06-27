# Source Pack Usage Guide

Source packs are curated starting points for resource-augmented tutoring. They
help the tutor choose better first sources for STEM, AI, and CS learning
questions, while the skill remains universal across all subjects.

## How To Use Source Packs

1. Diagnose the learner's subject, topic, goal, and likely prerequisite gap.
2. Choose the smallest relevant source pack, then one to three source entries.
3. Verify source access when web access is available.
4. Prefer specific course, lecture, assignment, documentation, or textbook
   section pages over generic homepages.
5. Explain why each source fits the learner's current gap.
6. Turn sources into a learning path: foundation, concept, worked reasoning,
   practice, and next step.
7. List sources used or recommended with clear labels.

## Core Packs And Specialty Addendums

Start with the core packs for broad learning questions. Use specialty addendums
when the learner's topic is clearly narrower or when the core packs are too
general.

- Use core packs for first-pass routing and prerequisite diagnosis.
- Use specialty addendums for theory/formal methods, cryptography/security,
  numerical/HPC/control, networks from zero, and VR/multimedia.
- Choose one to three sources for most answers. More links usually make the
  answer harder to use.
- Separate beginner sources from advanced sources. A beginner path should not
  start with standards, RFCs, or graduate notes unless the user asks for exact
  technical detail.
- Escalate from beginner-friendly sources to advanced courses, standards, or
  specifications only after the learner has the prerequisites.

## Routing By Topic

- Calculus, linear algebra, discrete math, probability, statistics,
  optimization: use `math_foundations.md`.
- Programming fundamentals, OOP, data structures, algorithms, software
  construction: use `programming_and_cs_foundations.md`.
- Computer organization, architecture, operating systems, networks,
  databases, security: use `systems_networks_security.md`.
- AI, ML, neural networks, data mining, search engines, embeddings,
  information retrieval: use `ai_ml_data.md`.
- Physics, electronics, digital logic, signals, DSP, systems, controls:
  use `physics_electronics_signals.md`.
- Graphics, image processing, multimedia, HCI, accessibility, software
  engineering practice: use `graphics_multimedia_hci_software.md`.
- Exam prep, practice planning, problem-set patterns, official assignments:
  use `exam_problem_set_sources.md`.
- Formal languages, automata, computability, complexity, proof-heavy theory:
  use `theory_formal_methods.md`.
- Cryptography, number theory in crypto, network security, web security:
  use `crypto_security_addendum.md`.
- Numerical analysis, scientific computing, HPC, parallel computing, control:
  use `numerical_hpc_control.md`.
- Beginner computer networks, TCP/IP, DNS, HTTP, Wireshark labs:
  use `networks_from_zero.md`.
- VR, WebXR, multimedia, image/audio/video processing:
  use `vr_multimedia_addendum.md`.
- Link refresh and source-pack maintenance:
  use `source_refresh_maintenance.md`.
- Exact page citation and avoiding broad homepage citations:
  use `source_specificity_guidelines.md`.

## Source Pack Rules

- Treat source packs as preferred starting points, not exhaustive coverage.
- Still search or verify when the user asks for current, specific, or obscure
  resources.
- Do not cite a source unless it was available from the pack and reasonably
  verified in the current environment, or clearly label it as not verified.
- Do not invent sources to fill gaps.
- Do not use answer-only sites when teaching reasoning matters.
- Do not copy large source content into answers or into the repository.
- Do not let STEM / AI-CS source packs narrow the skill's universal identity.

## When A Source Pack Is Insufficient

If the pack does not contain a good source for the learner's exact topic:

- Say that the pack has only partial coverage.
- Use the closest reliable source only for the part it supports.
- Search for better official, university, open textbook, or authoritative
  sources if web access is available.
- If search is unavailable, answer from foundations and give the learner
  source categories to verify later.

## Good Source-Backed Teaching Pattern

```text
Diagnosis: You are asking about [topic]. The gap is likely [prerequisite].

Source selection: I would start with [source] for [reason], and [source] for
practice or implementation.

Teaching path: First learn [foundation], then [core idea], then [practice
pattern].

How to use the sources: Read/watch [specific part if verified], then try
[practice type], then explain the idea back in your own words.

Sources: [labels and links]
```

## Poor Source-Pack Use

- Listing ten links without diagnosing the learner's gap.
- Citing a generic homepage when a specific lecture or assignment page is
  available.
- Treating a tutorial as more authoritative than official documentation.
- Giving final answers from a problem set without teaching the reusable method.
- Recommending advanced sources before checking prerequisites.
- Citing a broad course homepage when an exact lecture, assignment,
  documentation, standard, or chapter page is available.
