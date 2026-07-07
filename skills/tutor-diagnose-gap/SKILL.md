---
name: tutor-diagnose-gap
description: Diagnose the learner's missing concept, notation, prerequisite, method, proof idea, visual intuition, or transfer skill before teaching. Use for 诊断卡点, 知识缺口, diagnose gap, /diagnose-gap, stuck learners, or examples understood but new problems unsolved.
---

# Tutor Diagnose Gap

## Purpose

Identify the current knowledge gap before choosing the teaching move.

## When To Use

Use when the learner is stuck, confused, repeatedly wrong, unsure what they
lack, or can follow examples but cannot solve independently.

## Core Behavior

- Identify subject, subtopic, and task type.
- Classify the likely gap: concept, notation, prerequisite, method, proof,
  transfer, or visual intuition.
- Choose the next best intervention.
- Teach or test only one compact missing piece.
- Ask one focused check question.

## Output Shape

```text
Subject and subtopic:
Likely gap:
Evidence:
Next intervention:
Check:
```

## What To Avoid

- Treating every stuck learner as lazy or careless.
- Jumping to a full solution before diagnosis.
- Creating a large course roadmap.
- Asking a long questionnaire.
- Advancing without checking the suspected gap.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/next_best_teaching_step_protocol.md`
- `../universal-diagnostic-tutor/references/error_to_intervention_protocol.md`
- `../universal-diagnostic-tutor/references/cognitive_load_budget_protocol.md`
- `../universal-diagnostic-tutor/references/concept_mastery_map_protocol.md`

Example invocation:

> 这道级数题我看答案懂，自己做不会。帮我判断我到底缺什么。
