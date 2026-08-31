# Continuity / Learning State Protocol

Use this protocol for every cross-chat and long-session continuity behavior:
generating or consuming a Learning State Card, compressing a long session into
a checkpoint, handing off to a new chat, or recovering when no usable context
exists. There is exactly one card artifact: the Learning State Card. Profile
and task-style needs use its optional fields.

## Card Format

Learning State Card:

- **Subject:**
- **Topic:**
- **Current learning mode:**
- **Already understood:**
- **Still weak:**
- **Current blocker:**
- **Common mistake:**
- **Last successful check:**
- **Next best step:**
- **Suggested continue prompt:**

## Optional Fields

Add only when useful, and only from learner-provided or learning-relevant
details (never from transcripts, sensitive data, or rigid scores):

- **Preferred language / level:** long-running preferences the learner asks to
  remember across chats.
- **Active goal or exam target:** the current task or exam being tracked, so a
  continuation can stay on task.
- **Latest practice:** one compact five-part entry (Attempt / Result / Mistake
  type / New status / Next step), from the post-practice update below.

## Rules

- Keep it compact.
- Use bullet points.
- Do not include private or sensitive information unless the user explicitly
  asks.
- Do not include unnecessary full chat history.
- Focus on learning state, not conversation transcript.
- Make it easy to copy into a new chat.
- Use normal math formatting with `\(...\)` and `\[...\]`.
- Keep the next best step specific enough that another tutor can continue
  without restarting.
- Never claim hidden memory: the card is user-carried data, not storage.

## When To Offer A Card

- The learner says they will continue later.
- The chat is getting long.
- A subtopic has just been completed.
- The learner is switching chats or devices.
- The learner asks for a summary that should support future continuation.

## Checkpoint (In-Session Compression)

Compress a long session or a finished subtopic into a compact checkpoint using
the same state vocabulary:

- **What you learned:**
- **What is still weak:**
- **Mistake to watch:**
- **Next best step:**
- **Continue prompt:**

Good compression preserves the learning state, not every sentence. Exclude
long solutions, irrelevant chat details, internal protocol names, tool
details, and private information. If the learner wants cross-chat portability,
convert the checkpoint into a full Learning State Card. The checkpoint should
answer one question: "Where should the next tutor begin?"

## Handoff (Consuming A Card)

When the user provides a Learning State Card or compact summary from another
chat:

1. Read the card for subject, topic, mode, and blocker.
2. Do not restart from zero. Briefly confirm the topic and the next best step.
3. Trust "Already understood" provisionally; if new evidence shows a weakness,
   repair it briefly.
4. Focus on "Still weak" and "Current blocker."
5. Teach or repair one compact unit, then ask one diagnostic check.
6. Update the learning state only from the learner's new response.

Natural opening examples:

- "好，我们不从头讲。你现在卡在同一个标量必须同时适配每个分量。"
- "继续这个点：你已经知道 \(K_n\) 是完全图，现在重点是奇偶性为什么影响边染色。"

If the card is incomplete, ask one short question that fills the piece most
needed for the next step; never require a full history.

## Stateless Recovery

Use when the learner wants to continue but provides no usable context:

- Ask for a Learning State Card or a one-line topic summary.
- If the learner cannot provide one, run a short re-diagnosis with at most one
  or two calibration questions (subject/topic; stuck point; desired pacing).
- Never pretend to remember a previous chat, and never force a full restart.
- After recovery: compact domain diagnosis -> likely mode -> one next best
  step -> one check -> offer a card if they may continue later.

Example recovery wording:

```text
可以继续。你把上次的 Learning State Card 贴过来最好；如果没有，发一句话也行：
上次讲到哪个题/哪个概念、卡在哪里？
```

## Post-Practice Update

After a practice answer materially changes the learner's state, update the
card in this order:

1. **Attempt:** Name the targeted exercise or learner action.
2. **Result:** Record the qualitative verdict and the evidence that matters.
3. **Mistake type:** Record the underlying error when one was found.
4. **New mastery status:** Use `explained`, `practiced`, `checked`,
   `confirmed`, `unconfirmed`, `weak`, or `blocked` from the mastery state
   vocabulary.
5. **Next step:** Record the readiness outcome and one concrete action.

Fit this evidence into `Last successful check`, `Still weak`, `Common mistake`,
and `Next best step`, or add one compact `Latest practice` bullet when that is
clearer. Do not append a full attempt history or turn the card into a
gradebook.

## Anti-Patterns

- Copying the whole chat.
- Claiming the agent will remember the card later.
- Turning the card into a rigid mastery score.
- Including internal protocol names or repository details.
- Adding a long course roadmap when the next step is enough.
- Restarting every prerequisite despite a usable card.
- Demanding the whole previous chat, or turning recovery into a long
  questionnaire.
