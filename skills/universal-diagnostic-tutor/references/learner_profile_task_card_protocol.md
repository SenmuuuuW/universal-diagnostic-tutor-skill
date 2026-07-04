# Learner Profile And Learning Task Card Protocol

Use this protocol to improve continuity without databases, hidden memory, user
accounts, or persistent learner profiles.

All cards are user-visible and copy-pasteable. The learner controls what is
included and where it is pasted.

## Card Types

### Learner Profile Card

Use for relatively stable preferences the learner explicitly wants to preserve.

```text
Learner Profile Card:
- Preferred language:
- Current subjects:
- Learning level:
- Common weak areas:
- Preferred teaching pace:
- Exam goal, if any:
- Platform used:
- Notes to preserve:
```

### Learning Task Card

Use for a current task, exam target, or active study item.

```text
Learning Task Card:
- Task:
- Topic:
- Target outcome:
- Current blocker:
- Next action:
- Due date / exam date, if provided:
- Practice needed:
- Checkpoint:
```

## When To Offer Cards

Offer a card when:

- the session is long
- the user is preparing for an exam
- the user has multiple tasks
- the user wants to continue later
- the user switches platforms
- the learner asks for `/state-card`

Use a Learning State Card for the current concept checkpoint. Use a Learner
Profile Card for stable preferences. Use a Learning Task Card for a concrete
near-term goal.

## Rules

- Keep cards short.
- Do not include private or sensitive data unless the user explicitly provides
  it and wants it included.
- Do not claim the tutor will remember the card automatically.
- Do not include full transcripts.
- Do not turn cards into gradebooks, curriculum maps, or permanent labels.
- When a card is pasted into a new chat, continue from it rather than
  restarting from zero.
- If a card conflicts with new learner evidence, trust the current evidence and
  update the card only if the user wants.

## Natural Wording

When offering a card:

```text
如果你想下次接着学，我可以给你一张短卡片。你复制到新 chat 里，它就能从当前卡点继续，不需要假装有隐藏记忆。
```

When continuing from a card:

```text
好，我们按这张卡继续，不从头讲。你当前卡点是 [blocker]，下一步先做 [next action]。
```
