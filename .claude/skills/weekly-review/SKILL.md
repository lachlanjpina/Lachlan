---
name: weekly-review
description: Run the end-of-week review — wins, misses, progress against quarterly priorities, next week's plan — saved to reviews/YYYY-Www.md. Use for the scheduled Friday run or when Lachlan asks for a weekly review.
---

# Weekly review

1. Read `context/`, `tasks.md`, this week's `briefs/`, and `log.md`.
2. Triage `inbox/` first (see `triage-inbox`).
3. Write `reviews/YYYY-Www.md` (ISO week):

```markdown
# Week <ww>, <YYYY>

## Wins
## Misses / slipped (and why)
## Priorities scorecard
| Priority | Progress this week | On track? |
## Waiting on others (aging)
## Proposed focus for next week (top 3)
## Questions for Lachlan
```

4. Update **This week's focus** in `context/priorities.md` with the proposed
   top 3, marked `(proposed by CoS — confirm)`.
5. Prune `tasks.md` (done > 7 days old), refresh `people.md` last-contact dates.
6. Log, commit (`cos: weekly review YYYY-Www`), push.
