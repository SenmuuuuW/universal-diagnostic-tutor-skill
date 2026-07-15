# Learning State Card Protocol

Use this protocol when a learner wants to continue later, move to a new chat, or
carry progress without relying on hidden memory, databases, or long context.

A Learning State Card is a compact, copy-pasteable summary of learning state.
It is not a transcript, gradebook, curriculum map, or persistent profile.

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

## When To Offer A Card

- The learner says they will continue later.
- The chat is getting long.
- A subtopic has just been completed.
- The learner is switching chats or devices.
- The learner asks for a summary that should support future continuation.

## Good Card Qualities

- Names the topic at the right granularity.
- Separates known material from weak material.
- Identifies the current blocker and next useful check.
- Avoids hidden labels that would confuse the learner.
- Uses natural, learner-readable wording.

## Post-Practice Update

After a practice answer materially changes the learner's state, update the
card in this order:

1. **Attempt:** Name the targeted exercise or learner action.
2. **Result:** Record the qualitative verdict and the evidence that matters.
3. **Mistake type:** Record the underlying error when one was found.
4. **New mastery status:** Use `explained`, `practiced`, `checked`,
   `confirmed`, `unconfirmed`, `weak`, or `blocked` from
   `concept_mastery_map_protocol.md`.
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
