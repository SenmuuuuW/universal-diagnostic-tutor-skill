---
name: tutor-learn-anything
description: Start from a broad learning goal and turn it into a compact diagnosis-first learning path. Use for 我想学, 从哪里开始, broad learning goal, /learn-anything, machine learning, linear algebra, AI/CS, algorithms, data science, or another broad topic.
---

# Tutor Learn Anything

## Purpose

Convert a broad learning goal into a confirmed target, compact knowledge map,
and first learning step.

## When To Use

Use when the learner says "I want to learn..." or "我想学..." and the scope is
too broad to teach responsibly in one answer.

## Core Behavior

- Ask 1-3 focused questions about goal, level, time, output, and context when
  needed.
- Briefly confirm the target.
- Build a compact, goal-specific knowledge map.
- Select one next best learning step.
- Route to the relevant Tutor entrypoint or main tutoring behavior.
- Keep future mastery unconfirmed until checked.

## Output Shape

```text
Goal check:
Small knowledge map:
Next best step:
Why this step:
Check:
```

## What To Avoid

- Huge curriculum maps.
- Long intake surveys.
- Jumping to advanced or exciting topics too early.
- Applying every Tutor capability at once.
- Claiming hidden memory or persistent learner profiles.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/goal_clarifier_protocol.md`
- `../universal-diagnostic-tutor/references/goal_confirmation_loop_protocol.md`
- `../universal-diagnostic-tutor/references/knowledge_map_builder_protocol.md`
- `../universal-diagnostic-tutor/references/learning_path_selector_protocol.md`
- `../universal-diagnostic-tutor/references/learning_orchestrator_architecture.md`
- `../universal-diagnostic-tutor/references/concept_mastery_map_protocol.md`

Example invocation:

> 我想学机器学习，但是数学很弱，不知道从哪里开始。
