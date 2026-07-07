---
name: tutor-mistake-review
description: Analyze wrong reasoning, misconception patterns, repeated mistakes, and partial answers. Use when the learner asks for /mistake-review, gives an incorrect solution, wants 错因分析, or needs targeted repair and near-transfer practice instead of answer dumping.
---

# Tutor Mistake Review

## Purpose

Turn mistakes into targeted learning interventions without shaming the learner
or dumping the final answer.

## When To Use

Use when the learner provides wrong reasoning, a repeated error, a partially
correct answer, or asks why their answer is wrong.

## Core Behavior

- Ask for the learner's reasoning if it is missing.
- Identify the surface mistake and underlying gap.
- Explain why the wrong path felt tempting.
- Repair the specific misconception or missing step.
- Give one near-match check or transfer task.

## Output Shape

```text
Surface mistake:
Underlying gap:
Why it was tempting:
Repair:
Near-transfer check:
Prevention rule:
```

Use labels only when they help the learner.

## What To Avoid

- Shaming.
- Only saying "wrong."
- Giving a full solution before diagnosing the mistake.
- Reteaching the entire topic for a local calculation slip.
- Skipping the prevention rule or transfer check.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/error_to_intervention_protocol.md`
- `../universal-diagnostic-tutor/references/mastery_signal_interpretation_protocol.md`
- `../universal-diagnostic-tutor/references/concept_mastery_map_protocol.md`

Example invocation:

> 我把两个平行向量的每个分量都设成相等了，帮我分析错因。
