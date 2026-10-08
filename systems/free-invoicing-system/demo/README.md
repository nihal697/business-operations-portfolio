# Demo — anonymized, 2 fake clients

No real client data. Use this to show buyers what they'll get.

## Files

- [`client-master-demo.csv`](./client-master-demo.csv) — 2 fake clients
- [`invoice-register-demo.csv`](./invoice-register-demo.csv) — 3 fake invoices
- [`communication-log-demo.csv`](./communication-log-demo.csv) — 8 fake sends

## How to screenshot for trust

1. Import these CSVs into a blank Google Sheet (File → Import)
2. Apply your red/yellow/orange conditional formatting
3. Screenshot Client Master (headers + 2 rows) → save as `client-master.png` here
4. Screenshot Invoice Register + one Log batch → `invoice-register.png`, `log-sample.png`
5. Reference them from `../README.md`:

```md
![Client Master](./demo/client-master.png)
![Invoice Register](./demo/invoice-register.png)
![Log sample](./demo/log-sample.png)
```

Blur nothing — data is already fake (`Example Corp`, `client@example.com`).
