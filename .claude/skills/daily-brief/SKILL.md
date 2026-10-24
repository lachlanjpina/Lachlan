---
name: daily-brief
description: Produce today's morning brief — top priority, schedule, tasks due, follow-ups, decisions needed — and save it to briefs/YYYY-MM-DD.md. Use for the scheduled weekday run or when Lachlan asks for "my brief" / "what's on today".
---

# Daily brief

1. Follow "Every run, in this order" in `CLAUDE.md` (read context, triage inbox,
   pull live data if connectors exist).
2. Update `tasks.md`: move items due today into **Today**, flag overdue with ⚠️,
   add a chase date to any **Waiting on others** item older than 3 days.
3. For every follow-up due today, write a ready-to-send draft in
   `drafts/YYYY-MM-DD-<slug>.md` (To / Subject / Body).
4. For every meeting today with an external person, add 3 prep bullets (who,
   what they want, what we want) — use `context/people.md` and `accounts.md`.
5. Write `briefs/YYYY-MM-DD.md` using exactly this template, omitting empty
   sections:

```markdown
# Brief — <Weekday> <YYYY-MM-DD>

**The one thing:** <single highest-leverage action today, and why>

## Decisions needed
- <yes/no or A/B question>

## Schedule
- 09:30 — <meeting> — <one-line prep / link to prep>

## Due today
- [ ] ...

## Overdue ⚠️
- [ ] ...

## Follow-ups drafted (in drafts/)
- <who> — <what> → `drafts/<file>`

## Watch list
- <risks, slipping deals, people you haven't spoken to in a while>

_Data sources: <repo only | Gmail, Calendar, …>_
```

6. Log, commit (`cos: daily brief YYYY-MM-DD`), push.
