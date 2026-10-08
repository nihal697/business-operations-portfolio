# Reminder Rules (live config, values safe to share)

| Rule | Value |
|------|-------|
| Pre-due Reminder 1 | T-5 days |
| Pre-due Reminder 2 | T-2 days |
| Grace Period | 5 days |
| Overdue Reminder 1 / 2 / 3 | D+2 / D+5 / D+10 |
| Recurring overdue | Every 7 days, starting D+17, unlimited (0 = ∞) |
| Advance invoice month | Current month |
| Postpaid invoice month | Previous month |

**Guardrails:**
- Send only 10:00–19:00 Asia/Kolkata, on checked weekdays
- Skip `Paid`, skip `Inactive` clients, skip if reminders paused
- `Next Reminder Date` computed; yellow highlight = due today
- Late-penalty table is informational (3% / 8% / 10% after 5/15/30d) — applied manually, not auto-charged

**Log proof (anonymized):** `Pre-Due Reminder 1 → Success`, `Overdue Reminder 2 → Success`, `Failed: No email address configured` — batch continues on single failure.
