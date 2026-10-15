---
description: "Research a question from primary sources and write a cited findings note."
---

# research

When invoked, research the question the user gives (the argument; ask for it if missing).

1. Restate the question and its scope in one or two sentences. If it is ambiguous, ask one
   clarifying question before continuing.
2. Find primary sources: official docs, the paper, the specification, or the code. List each
   with title, publisher or author, date and URL. Fetch only what the question needs.
3. For long documents, delegate reading to the `source-reader` sub-agent and use its cited
   summary.
4. Create `research/<topic>.md` (kebab-case) with frontmatter (title, date, status draft,
   sources, tags) and these sections: Question, Short answer, Findings (each claim cited),
   Disagreements or gaps, Open questions, Next steps.
5. Mark any claim you could not verify as `unverified`. Never invent citations.
6. Reply with the short answer, the confidence level, and the path of the note.
