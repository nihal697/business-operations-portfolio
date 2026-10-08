# Do not commit secrets. Ever.

This repo is a public showcase. It must never contain:

- Passwords, app passwords, API keys (Google Picker, WhatsApp tokens, etc.)
- Workbook / Drive / WABA / phone-number IDs from live systems
- Client PII: real names, phones, emails, fees, invoice amounts
- Private Apps Script project URLs with edit access

## Rules

1. All examples use **anonymized demo data** (`Example Corp`, `client@example.com`, `₹10,000`).
2. Real screenshots must be blurred/redacted before adding to `docs/`.
3. `Code.gs` is added as `Code.gs.placeholder` until you paste a **sanitized** copy with:
   - `SpreadsheetApp.openById("PASTE_ID_HERE")` instead of real IDs
   - No hardcoded passwords/tokens — use `PropertiesService.getScriptProperties()`
4. If you accidentally pasted a secret (it happened in chat — password + Picker key + client PII):
   - Rotate it immediately in Google Cloud / WhatsApp / Gmail
   - Remove the message/file, never commit it
   - Check `git log` — secrets in history need `git filter-repo` + rotation, not just delete

## Safe pattern for Apps Script config

```gs
// NEVER hardcode:
// const TOKEN = "EAAxxxx..."

// DO THIS:
const TOKEN = PropertiesService.getScriptProperties().getProperty("WHATSAPP_TOKEN");
const SHEET_ID = PropertiesService.getScriptProperties().getProperty("CLIENT_MASTER_ID");
```
