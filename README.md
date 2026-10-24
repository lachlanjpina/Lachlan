# Lachlan's Chief of Staff

A Claude-powered Chief of Staff that runs on a schedule, keeps your tasks and
relationships straight, drafts your follow-ups and preps your meetings. You
dump notes in; it hands you briefs and ready-to-send drafts.

## How it works

```
 you ──► inbox/  (notes, pasted emails, "remind me to…")
            │
   scheduled run (weekday mornings + Friday afternoon)
            │
            ▼
   tasks.md · context/people.md · context/accounts.md   (kept up to date)
   briefs/YYYY-MM-DD.md                                 (read in 2 minutes)
   drafts/                                              (you approve & send)
```

The operating rules are in [`CLAUDE.md`](CLAUDE.md). The routines are skills in
`.claude/skills/`:

| Skill | When | Output |
|---|---|---|
| `daily-brief` | Weekdays, morning | `briefs/YYYY-MM-DD.md` |
| `weekly-review` | Fridays, afternoon | `reviews/YYYY-Www.md` |
| `triage-inbox` | Every run | updates tasks/people/accounts |
| `meeting-prep` | "prep me for …" | `drafts/prep-…md` |
| `capture` | "remind me to …" | filed in the right place |

## Setup (10 minutes)

1. **Fill in** `context/about-me.md` and `context/priorities.md`. Rough is fine.
2. **Connect your tools** at claude.ai → Settings → Connectors (Gmail / Outlook,
   Google Calendar, Slack, Salesforce…). Without them it still works from the
   repo; with them it reads your calendar and email automatically.
3. **Schedule it** — in a Claude Code session on this repo, ask:
   _"Schedule the daily brief for weekdays at 7:30am and the weekly review
   Fridays at 3pm, my timezone is Australia/Sydney."_
4. **Use it day to day:**
   - Drop notes into `inbox/` (GitHub mobile app works well).
   - Open a session and say "remind me to…", "prep me for my 2pm", or
     "what's on today?".
   - Read `briefs/` each morning; send what's in `drafts/`.

## Ground rules

- It never sends emails or messages on your behalf — it drafts, you send.
- Everything it does is a git commit, so you can see and undo any change.
