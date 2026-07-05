---
name: tutor-study-plan
description: Create a brief diagnosis-first study plan from a learner's goal, current level, time constraints, and blockers. Use for STEM, AI-CS, university STEM, exam review, or self-study planning when the learner asks for /study-plan, a learning route, review order, or what to study first.
---

# Tutor Study Plan

## Purpose

Create short, diagnosis-first study plans that help the learner start now.

## When To Use

Use when the learner asks for a study plan, review order, self-study path,
exam-prep plan, or what to study first.

## Core Behavior

- Clarify a broad goal with 1-3 focused questions only when needed.
- Briefly confirm the current level, target, time constraint, and main blocker.
- Identify top gaps and choose a realistic order.
- For broad STEM / AI-CS goals, use discipline-first planning: required
  disciplines -> subtopics -> minimum mastery -> skip-for-now -> first step.
- For ML / AI-CS plans, name the needed parts of programming, linear algebra,
  calculus/optimization, probability/statistics, and ML core before any
  timeline.
- Include today's first concrete step and one check question.
- Keep the plan short enough to act on.

## Output Shape

```text
Goal confirmation:
Discipline map:
Required subtopics:
Minimum mastery standard:
Suggested order:
Today's first step:
Check question:
Optional trusted resources:
```

Use natural wording when labels would feel stiff.

## What To Avoid

- Giant curriculum maps.
- Score guarantees or fake deadlines.
- Resource dumping.
- Starting advanced topics before prerequisites are named.
- Vague stages such as "learn vectors, functions, probability" without naming
  the discipline and exact subtopics.
- Jumping to scikit-learn, PyTorch, deep learning, or research papers before
  the prerequisite map is clear.
- Treating the plan as a rigid course builder.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/brief_study_plan_protocol.md`
- `../universal-diagnostic-tutor/references/goal_clarifier_protocol.md`
- `../universal-diagnostic-tutor/references/goal_confirmation_loop_protocol.md`
- `../universal-diagnostic-tutor/references/learning_path_selector_protocol.md`
- `../universal-diagnostic-tutor/references/learning_state_card_protocol.md`

Example invocation:

> 我想学机器学习，但是数学很弱。帮我做一个短学习计划。
