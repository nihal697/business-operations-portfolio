# Sheet Schema (sanitized demo)

All column names from your live system. Formulas simplified. Example values are fake.

## 1. Client Master

| Column | Source | Purpose |
|--------|--------|---------|
| Client ID | Manual (`CL00001`) | Stable key for lookups |
| Client Name | Manual, unique | Renaming auto-renames Drive folder |
| Contact Person | Manual | `{{ContactPerson}}` in mails |
| Phone / Email | Manual | WhatsApp + email destinations |
| Active Services | Manual (`SEO, SMM`) | Scope reference |
| Monthly Fee (₹) | Manual | e.g. `₹11,000` (demo) |
| Billing Type | Manual (`Advance`/`Postpaid`) | Drives invoice-month logic |
| Due Date | Manual (day of month) | e.g. `1`, `5`, `10` |
| Client Status | Manual (`Active`) | Inactive clients skipped |
| Account Manager | Manual | Owner |
| Client Since / Notes / Drive Folder ID | Manual / Script | Folder auto-created per client |

## 2. Invoice Register (Dashboard)

| Column | Source | Logic |
|--------|--------|-------|
| Invoice ID | Script (`INV00001`) | Unique, red if duplicate |
| Client / Client ID | Manual + `XLOOKUP(Client Master)` | Red if bad Client ID |
| Due Date | Script | Yellow if within 3 days |
| Invoice Amount | Manual | Billed |
| Invoice Link | Manual (Drive) | Red if missing |
| Received Amount | Formula `SUMIF(Payment Register)` | Red if > invoice |
| Balance Due | Formula `Invoice − Received` | — |
| Payment Status | Formula | `Pending / Partially Paid / Paid` — do not edit |
| Collection Status | Formula | `Paid / Overdue / Upcoming` from `TODAY() > Due` |
| Payment Count | Formula `COUNTIF` | — |
| Invoice Sent Date / Last Reminder / Reminder Count / Next Reminder | Script | Orange if unsent; yellow if reminder due today |
| All / Email / WhatsApp Reminders | Script+Manual | `Enabled` toggles |
| Email Thread ID / Notes / Version | Script / Manual | Threading + revisions |

## 3. Payment Register

`Payment ID (PAY...)` / `Invoice ID` / `Client ID (=XLOOKUP)` / `Client Name` / `Payment Date` / `Received Amount` / `Payment Method (UPI/Bank/Cash)` / `Reference Number` / `Notes`. Auto-stub created on invoice creation.

## 4. Communication Log

`Log ID (LOG...)` / `Timestamp` / `Invoice ID` / `Client ID` / `Client Name` / `Activity (Welcome / Invoice / Pre-Due 1-2 / Overdue 1-3 / Recurring / Payment Confirmation)` / `Channel (Email/WhatsApp)` / `Status (Success/Failed)` / `Description (subject + recipient or error)`.

## 5. Settings

Reminder cadence, business hours, penalties, signature HTML, Drive CTA, locale (`Asia/Kolkata`, `en-IN`, `₹`), ID counters, workbook IDs (never commit real ones), confirmation dialogs.

## 6. Templates

10 types × 2 channels. See `TEMPLATES.md`. Placeholders: `{{ContactPerson}} {{InvoiceMonth}} {{InvoiceMonthYear}} {{DueDate}} {{InvoiceAmount}} {{InvoiceLink}} {{SenderName}} {{DriveLink}} {{BodyContent}} {{SignatureContent}}`.
