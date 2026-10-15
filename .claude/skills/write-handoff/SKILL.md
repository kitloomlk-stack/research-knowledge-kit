---
name: write-handoff
description: "Write a compact handoff note so a fresh session can continue the work."
disable-model-invocation: true
---

# handoff

When invoked, write a handoff note so a fresh session or another agent can continue.

1. Review the conversation and the files changed. Do not copy the transcript.
2. Create `handoff/YYYY-MM-DD-topic.md` using today's date and a short kebab-case topic.
3. Include: Goal, Current state, Decisions and why, Tried and failed, Next step (one exact
   action), Files that matter (paths), Commands that matter (exact text), Open questions.
4. State facts only. Mark guesses as guesses. Leave out secrets, tokens, credentials and
   personal data.
5. If a decision or lesson should outlive this task, offer to add it to `memory/` as well
   (see `/capture`).
6. Reply with the path of the note and a two-line summary. Do not start new work.
