# universal-diagnostic-tutor-skill

A reusable Codex Agent Skill for diagnosis-first tutoring across subjects.

This project contains the first version of `universal-diagnostic-tutor`, a
universal teaching skill for Codex and ChatGPT-style assistants. It is designed
for learning-related questions in math, science, humanities, social sciences,
law, economics, history, geography, literature, language learning, writing,
coding, AI, exam prep, and general concept learning.

## Not Answer-First, Diagnosis-First

Many tutoring interactions jump straight to the final answer. That can be fast,
but it often hides the real problem: the learner may be missing a prerequisite,
misreading the task, using the wrong mental model, or not seeing why a step
makes sense.

This skill asks the assistant to diagnose first:

1. What subject is this?
2. What topic or skill is being tested?
3. What prerequisite ideas matter?
4. What knowledge gaps are likely?
5. Where should the explanation begin?

Only after that diagnosis should the assistant teach, solve, summarize, and
offer practice.

## Why This Skill Exists

The goal is mastery, not just completion. A strong tutor does more than produce
answers. It finds the right starting point, builds the missing foundation,
explains the reasoning, names common mistakes, and helps the learner transfer
the method to the next problem.

This skill is intentionally universal. It must not become SAT-only, math-only,
coding-only, or limited to any single school subject.

## How It Works

When a learning-related request triggers the skill, the assistant follows this
core pattern:

1. Identify the subject domain.
2. Identify the specific topic or skill.
3. Identify prerequisite knowledge.
4. Diagnose likely knowledge gaps.
5. Decide where the explanation should begin.
6. Teach necessary foundations first.
7. Explain step by step.
8. Explain why each step makes sense.
9. Give the final answer or conclusion.
10. Summarize how to solve similar problems.
11. Point out common mistakes.
12. Connect to real-world applications when useful.
13. Give a short practice or understanding-check question.

The skill also defines teaching depth levels, subject-specific teaching modes,
and reusable answer formats.

## Repository Structure

```text
universal-diagnostic-tutor-skill/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── AGENTS.md
└── skills/
    └── universal-diagnostic-tutor/
        ├── SKILL.md
        ├── references/
        │   ├── subject_routing.md
        │   ├── teaching_depth_levels.md
        │   ├── subject_teaching_modes.md
        │   ├── output_formats.md
        │   ├── evaluation_checklist.md
        │   ├── manual_test_matrix.md
        │   ├── response_length_calibration.md
        │   ├── resource_integration_protocol.md
        │   ├── resource_augmented_output.md
        │   ├── source_trust_hierarchy.md
        │   ├── stem_ai_cs_scope.md
        │   ├── source_note_checklist.md
        │   ├── source_packs/
        │   │   ├── ai_ml_data.md
        │   │   ├── crypto_security_addendum.md
        │   │   ├── exam_problem_set_sources.md
        │   │   ├── graphics_multimedia_hci_software.md
        │   │   ├── math_foundations.md
        │   │   ├── networks_from_zero.md
        │   │   ├── numerical_hpc_control.md
        │   │   ├── physics_electronics_signals.md
        │   │   ├── programming_and_cs_foundations.md
        │   │   ├── source_refresh_maintenance.md
        │   │   ├── source_pack_usage_guide.md
        │   │   ├── source_specificity_guidelines.md
        │   │   ├── systems_networks_security.md
        │   │   ├── theory_formal_methods.md
        │   │   └── vr_multimedia_addendum.md
        │   └── maintenance_notes.md
        └── examples/
            ├── ai_concept_example.md
            ├── bad_vs_good_example.md
            ├── economics_business_example.md
            ├── finance_boundary_example.md
            ├── health_boundary_example.md
            ├── humanities_evidence_example.md
            ├── math_example.md
            ├── science_example.md
            ├── humanities_example.md
            ├── coding_example.md
            ├── cryptography_foundation_example.md
            ├── formal_languages_example.md
            ├── law_civics_example.md
            ├── language_literature_example.md
            ├── mixed_subject_example.md
            ├── natural_style_example.md
            ├── networks_from_zero_source_example.md
            ├── numerical_analysis_example.md
            ├── resource_augmented_ai_example.md
            ├── resource_augmented_cs_example.md
            ├── resource_augmented_exam_pattern_example.md
            ├── resource_augmented_math_example.md
            ├── source_pack_usage_example.md
            ├── source_limited_answer_example.md
            ├── writing_revision_example.md
            └── exam_prep_example.md
```

## V0.2 Improvements

V0.2 improves real-world reliability without changing the skill's identity. It
adds a manual evaluation checklist, fuller diagnosis-first examples, compact
short-answer guidance, bad-vs-good contrast, mixed-subject routing guidance, and
stronger educational boundaries for high-stakes domains such as law and
finance.

To manually test the skill, use prompts from several subject areas and score the
answers with
`skills/universal-diagnostic-tutor/references/evaluation_checklist.md`. A good
answer should diagnose the learning task, teach from the right starting point,
adapt to the subject, avoid over-explaining simple questions, and stay
educational in high-stakes contexts.

## V0.3 Improvements

V0.3 adds a lightweight Markdown-only manual test system. The manual test
matrix in `skills/universal-diagnostic-tutor/references/manual_test_matrix.md`
covers 12 subject and boundary scenarios, while
`skills/universal-diagnostic-tutor/references/response_length_calibration.md`
shows how to tune ultra-short, short, standard, and deep answers without losing
diagnosis-first reasoning.

V0.3 also adds health and finance educational boundary examples, a humanities
evidence example for interpretive uncertainty, and a natural style example that
shows how to avoid robotic template language.

## V0.4 Improvements

V0.4 adds a resource-augmented learning protocol for university-level STEM,
AI, and computer science study while preserving the universal tutor identity.
For STEM / AI-CS questions, the tutor should use reliable learning resources
when web access is available, explain what sources were used, and turn those
sources into a teaching path rather than a source dump.

The new source trust hierarchy prioritizes official documentation, official
course materials, university open courseware, textbooks and open textbooks,
official problem sets, authoritative technical sources, and reputable tutorials.
When external resources are used, answers should cite or list sources. When
internet access is unavailable, the tutor should say that sources could not be
verified instead of inventing links, textbooks, exams, or papers.

V0.4 does not add API dependencies, scripts, websites, copied textbooks, or
scraped course materials. This remains a universal diagnosis-first tutor skill,
not a CS-only skill.

## V0.5 Improvements

V0.5 adds curated, lightweight source packs for university-level STEM, AI, and
computer science learning. These packs give the tutor better starting points
for resource-augmented teaching in math foundations, programming and CS,
systems, networks, security, AI/ML/data, physics/electronics/signals,
graphics/HCI/software, and exam or problem-set practice.

Source packs are for source selection, study-path design, and citation
discipline. They are not copied textbooks, downloaded course archives, answer
banks, or a substitute for teaching. No API dependency, search integration,
website, package setup, PDFs, or copyrighted source material is included.

When sources are used, the tutor should still verify links when possible, cite
specific useful pages, and explain how each source supports the learner's next
step. STEM / AI-CS is the primary current use case, but the skill remains a
universal diagnosis-first tutor across all subjects.

## V0.6 Improvements

V0.6 strengthens the source-pack system with specialty addendums for
theory/formal methods, cryptography/security, numerical analysis, HPC, control,
beginner computer networks, VR, and multimedia. It also adds source specificity
guidance so the tutor prefers exact lecture, assignment, documentation,
standard, or textbook pages over broad homepages when possible.

The networks-from-zero pack gives beginners a gentler path before advanced
networking courses or RFCs. Source refresh maintenance guidance explains how to
mark stale, unverified, or term-specific links without turning source packs into
large dumps. This remains a universal diagnosis-first tutor skill; STEM / AI-CS
coverage is strengthened without making the skill STEM-only.

## Use With Codex

To use the skill locally, copy the skill folder into your Codex skills
directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/universal-diagnostic-tutor ~/.codex/skills/
```

Then start a new Codex session and ask a learning-related question, such as:

```text
Use the universal diagnostic tutor to help me understand why supply curves slope
upward.
```

Codex should load the skill when the request is about learning, teaching,
explaining, studying, practicing, debugging for understanding, exam prep, or
concept mastery.

## Maintain And Update

When updating the skill:

- Keep it universal across subjects.
- Preserve the diagnosis-first teaching philosophy.
- Keep `SKILL.md` concise and move detailed guidance into `references/`.
- Update examples when behavior changes.
- Update `CHANGELOG.md` for user-visible changes.
- Avoid scripts or infrastructure unless the skill truly needs them.

## Roadmap

- V0.1: Core universal tutor skill.
- V0.2: Stronger examples, subject routing, and manual evaluation checklist.
- V0.3: Manual test matrix and response length calibration.
- V0.4: STEM / AI-CS resource integration reference pack.
- V0.5: Curated STEM / AI-CS source packs for resource-augmented tutoring.
- V0.6: Specialty source addendums and source maintenance guidance.
- V1.0: Stable reusable tutor skill.

## 中文简介

这个项目是一个通用的 Codex 教学 Skill。它不是先给答案的
"答案机器人", 而是先判断学科、主题、前置知识和可能的知识漏洞,
再像老师一样从合适的位置开始讲解。

它适用于数学、科学、人文社科、语言文学、写作、编程、法律、经济、
考试备考等多种学习场景。核心目标是帮助学习者真正理解, 而不是只把
题目做完。
