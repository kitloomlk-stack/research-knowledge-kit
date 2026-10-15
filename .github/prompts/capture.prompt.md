---
name: "capture"
description: "Save a decision, fact or lesson from this session into the project memory notes."
---

# capture

When invoked, save a durable fact, decision or lesson into the project memory notes. The
argument is the thing to capture; if missing, propose one to three candidates from this
session and ask which to keep.

1. Decide the type: a decision goes in `memory/decisions.md`, a lesson or gotcha in
   `memory/lessons.md`. Create the file with a one-line heading if it does not exist.
2. Read the file first. If a related entry exists, update it or mark it `stale` rather than
   adding a contradiction.
3. Append an entry: date (ISO 8601), a one-line title, the fact in one to three sentences,
   the reason or evidence, and a link to the relevant file or note.
4. Verify the fact against the current code or docs before saving. If you cannot, label it
   `unverified`.
5. Do not include secrets, tokens or personal data. Show the user the entry you added.
