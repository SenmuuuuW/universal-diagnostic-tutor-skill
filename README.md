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
        │   └── maintenance_notes.md
        └── examples/
            ├── math_example.md
            ├── science_example.md
            ├── humanities_example.md
            ├── coding_example.md
            ├── language_literature_example.md
            └── exam_prep_example.md
```

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
- V0.2: Stronger examples and subject routing.
- V0.3: Testing and evaluation checklist.
- V0.4: Optional subject-specific reference packs.
- V1.0: Stable reusable tutor skill.

## 中文简介

这个项目是一个通用的 Codex 教学 Skill。它不是先给答案的
"答案机器人", 而是先判断学科、主题、前置知识和可能的知识漏洞,
再像老师一样从合适的位置开始讲解。

它适用于数学、科学、人文社科、语言文学、写作、编程、法律、经济、
考试备考等多种学习场景。核心目标是帮助学习者真正理解, 而不是只把
题目做完。
