# Stateless Recovery Protocol

Use this protocol when the user says they want to continue from before but no
usable prior context is available.

The tutor should recover gracefully without pretending to remember a previous
chat and without forcing the learner to restart everything.

## Core Behavior

- Ask for a Learning State Card or a one-line topic summary.
- If the user cannot provide one, do a short re-diagnosis with one or two
  calibration questions.
- Avoid pretending to remember previous chats.
- Avoid forcing a full restart.
- Offer to create a Learning State Card after the current explanation.

## Natural Recovery Wording

Use wording like:

```text
可以继续。你把上次的 Learning State Card 贴过来最好；如果没有，发一句话也行：上次讲到哪个题/哪个概念、卡在哪里？
```

If the learner has no summary:

```text
没关系，我们用 30 秒重新定位：这是线代、微积分、编程，还是别的？你最后记得的是“符号看不懂”、 “方法不会选”，还是“某一步推不下去”？
```

## Re-Diagnosis Questions

Ask at most one or two:

- What subject or topic was it?
- Were you stuck on symbol meaning, method choice, a proof step, or an error?
- Do you want zero-base, standard, or advanced pacing?

## After Recovery

Once the learner gives enough context:

1. Give a compact domain diagnosis.
2. Choose the likely mode.
3. Teach one next best step.
4. Ask one check.
5. Offer a Learning State Card if they may continue later.

## Anti-Patterns

- "I remember yesterday..." when no context exists.
- Demanding the whole previous chat.
- Restarting the whole subject from lesson one by default.
- Turning recovery into a long questionnaire.
