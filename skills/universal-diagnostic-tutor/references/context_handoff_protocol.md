# Context Handoff Protocol

Use this protocol when the user provides a Learning State Card or compact
learning summary from another chat.

## Core Behavior

- Do not restart from zero.
- Briefly confirm the topic and the next best step.
- Trust "Already understood" provisionally.
- Focus on "Still weak" and "Current blocker."
- If evidence shows an already-understood item is weak, repair it briefly.
- Ask one check before advancing.
- Do not mention that memory is unavailable; just use the card.

## Handoff Sequence

1. Read the card for subject, topic, mode, and blocker.
2. Start from the next best step rather than the beginning.
3. Compress known material into at most one reminder if needed.
4. Teach or repair one compact unit.
5. Ask one diagnostic check.
6. Update the learning state only from the learner's new response.

## Natural Opening Examples

- "好，我们不从头讲。你现在卡在同一个标量必须同时适配每个分量。"
- "继续这个点：你已经知道 \(K_n\) 是完全图，现在重点是奇偶性为什么影响边染色。"
- "The card says recursion base cases are clear, but smaller same-shaped calls
  are still weak. Let's focus there."

## If The Card Is Incomplete

Ask one short question that fills the missing piece most needed for the next
step. Do not require a full history.

Example:

```text
你还记得上次最后卡在“符号含义”还是“方法选择”吗？选一个就行。
```

## Anti-Patterns

- Restarting every prerequisite despite a usable card.
- Claiming direct memory of the previous chat.
- Ignoring the listed blocker and teaching a different topic.
- Advancing without one check when the card says the learner is still weak.
