# Message Templates (inventory — bodies live in Settings sheet)

Tone: friendly, professional, never threatening. Each has Email + WhatsApp variant.

| # | Type | Email subject (pattern) | From |
|---|------|--------------------------|------|
| 1 | Welcome | `Welcome to <Company>!` | personal |
| 2 | Invoice | `Invoice for {{InvoiceMonthYear}} – <Company>` | default |
| 3 | Pre-Due 1 | `Friendly Reminder – Payment Due on {{DueDate}}` | default |
| 4 | Pre-Due 2 | `A Friendly Follow-up Before {{InvoiceMonth}} Says Hello` | default |
| 5 | Overdue 1 | `A Gentle Follow-up Regarding Your {{InvoiceMonth}} Invoice` | financial |
| 6 | Overdue 2 | same as above (escalated body) | financial |
| 7 | Overdue 3 | Final friendly reminder + expected-date ask | financial |
| 8 | Recurring | `Payment Reminder – {{InvoiceMonth}} Invoice` | financial |
| 9 | Payment Confirmation | `Payment Received – Thank You` | financial |

WhatsApp variants are 2–4 lines: greeting + amount + due date + invoice link + opt-out-if-paid line.

Shared components: branded HTML wrapper (`{{BodyContent}}` + `{{SignatureContent}}`), signature card (Call/WhatsApp/Email pills + website), Drive CTA button (`ACCESS INVOICE FILE →` → `{{DriveLink}}`).

Full copy stays in your private Settings sheet — don't commit client-branded copy verbatim. Summarize here; share full text only with prospects under NDA if needed.
