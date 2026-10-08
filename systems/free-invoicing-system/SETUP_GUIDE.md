# Setup Guide (15 min, free tier)

1. **Copy the template Sheet** (structure in `SHEET_SCHEMA.md`). Keep tab names exact — script uses them.
2. **Fill Settings:** company name, sender emails, reminder days, business hours, locale. Leave tokens blank for now.
3. **Script Properties:** in Apps Script → Project Settings → Script Properties, add `CLIENT_MASTER_ID`, `WHATSAPP_TOKEN`, `WHATSAPP_PHONE_ID`, `WABA_ID`. Never hardcode.
4. **Paste sanitized `Code.gs`** (see `Code.gs.placeholder` for file list to export).
5. **Triggers:** daily time-driven `runReminders` (e.g. 08:30 Asia/Kolkata) + `onEdit` for ID/folder automation. Respect business-hours check inside code.
6. **Test with 1 demo client** (`client@example.com` + your own WhatsApp): create invoice → mark sent → force reminder → record payment → confirm thank-you + log rows.
7. **Go live:** import real clients only after redacting this repo and rotating any exposed keys (see `SECURITY.md`).

Daily ops: add payments to Payment Register; everything else recalculates. Check Communication Log failures each morning.
