---
name: triage-inbox
description: Process every raw note in inbox/ into tasks, people/account updates and drafts, then archive the originals. Use at the start of any Chief of Staff run or when Lachlan says "process my inbox" / "I dumped some notes".
---

# Triage inbox

For each file in `inbox/` (skip `README.md` and `processed/`):

1. Extract:
   - **Commitments** Lachlan made → task `@me` with a due date (guess sensibly
     if none: "this week" = Friday).
   - **Commitments others made** → **Waiting on others** with a chase date.
   - **People facts** → update or add a block in `context/people.md`.
   - **Account / project facts** → update `context/accounts.md`.
   - **Replies needed** → draft in `drafts/`.
   - **Ideas** → **Someday**.
2. Never invent facts. If something is ambiguous, add it to "Decisions needed"
   in the next brief.
3. Move the file to `inbox/processed/YYYY-MM-DD/`.
