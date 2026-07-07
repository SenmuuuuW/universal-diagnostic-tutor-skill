---
name: tutor-state-card
description: Generate or continue from visible Learning State Cards, Learner Profile Cards, and Learning Task Cards. Use for 学习状态卡, 继续学习, state card, /state-card, cross-chat continuation, pasted cards, or compact checkpoints without hidden memory.
---

# Tutor State Card

## Purpose

Create or use compact, copy-pasteable learning cards for continuity without
claiming hidden memory.

## When To Use

Use when the learner wants to continue later, move to a new chat, preserve
preferences, track a current learning task, or resume from a pasted card.

## Core Behavior

- Generate a Learning State Card, Learner Profile Card, or Learning Task Card
  depending on the request.
- Keep cards visible, short, and user-controlled.
- Continue from a pasted card without restarting from zero.
- If no usable context is provided, ask for a card or one-line topic summary.
- Update cards only when useful or requested.

## Output Shape

```text
Learning State Card:
- Subject:
- Topic:
- Already understood:
- Still weak:
- Current blocker:
- Next best step:
- Suggested continue prompt:
```

Use the fuller card format only when needed.

## What To Avoid

- Hidden-memory claims.
- Full transcript dumps.
- Sensitive details without permission.
- Rigid grades or persistent learner labels.
- Restarting from zero when a useful card is provided.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/learning_state_card_protocol.md`
- `../universal-diagnostic-tutor/references/learner_profile_task_card_protocol.md`
- `../universal-diagnostic-tutor/references/context_handoff_protocol.md`
- `../universal-diagnostic-tutor/references/stateless_recovery_protocol.md`

Example invocation:

> 帮我生成下次继续用的学习状态卡。
