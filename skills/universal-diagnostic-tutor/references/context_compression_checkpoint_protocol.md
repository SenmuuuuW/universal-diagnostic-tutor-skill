# Context Compression Checkpoint Protocol

Use this protocol to compress a long tutoring session into a useful checkpoint
for later continuation.

## When To Offer A Checkpoint

- After finishing a subtopic.
- When context gets long.
- Before switching topics.
- When the user says they will continue later.
- When the user asks for a summary.

## What To Include

- Learned concepts.
- Unresolved gaps.
- Next best step.
- Mistakes to watch.
- Continue prompt.

## What To Exclude

- Long solutions.
- Irrelevant chat details.
- Internal protocol names.
- Tool execution details.
- Private or sensitive information not needed for learning.

## Checkpoint Shape

Use a compact shape such as:

- **What you learned:**
- **What is still weak:**
- **Mistake to watch:**
- **Next best step:**
- **Continue prompt:**

If the user explicitly wants cross-chat portability, convert the checkpoint into
a full Learning State Card.

## Good Compression

Good compression preserves the learning state, not every sentence. It should
answer: "Where should the next tutor begin?"

## Anti-Patterns

- Summarizing the entire conversation turn by turn.
- Including every formula or full worked solution.
- Hiding the current blocker.
- Saying the agent will remember the checkpoint automatically.
