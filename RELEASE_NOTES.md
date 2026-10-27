## Penqwin ERP 6.0.0

Pharmacy management software for India, for Windows 10 and 11 (64-bit). An existing installation is upgraded in place and keeps its data.

| File | SHA-256 |
|---|---|
| `Penqwin-ERP-Setup-6.0.0.exe` | `898E05BE4B27FEA93B7AB1F7FEA88F378179F606AD9E0956881AD3F73A00B4B0` |

### Highlights

**Profit and margin**
- Each invoice shows its profit and margin, with the figures line by line on request.
- Each customer shows spend, profit and margin over all time, a financial year or any date range, in the customer list and on the customer page.
- These figures appear on screen only. They are never printed on a bill.

**Dashboard and navigation**
- Quick actions with live figures, and compact lists on wide screens.
- Redesigned sidebar and menu icons; the top bar keeps its labels on narrower windows.

**Counter and billing**
- Product search shows where stock is held (store or godown).
- Settling a bill no longer stops on stock that is held in a godown.
- Patient details for scheduled drugs are asked once per bill.
- Optional PTR column on invoices, off by default.

**Everyday use**
- Customer, supplier, doctor and bank account forms use the full window width.
- Suggestion lists close when you move to another field.
- The customer list opens faster on shops with long sales history.

### About Penqwin ERP

Point of sale, quotations, delivery challans and invoices; purchase orders, goods receipt and supplier payments; batch and expiry control; GST filing, GSTR-2B reconciliation and e-invoice; bank reconciliation, vouchers and financial reports; Schedule H1 and X registers. Records are stored on your own computer, with optional backup to Google Drive. The full list is in `docs/FEATURES.md` in this repository.

### Installing

Run `Penqwin-ERP-Setup-6.0.0.exe`; no administrator rights are needed. Verify the download with `certutil -hashfile Penqwin-ERP-Setup-6.0.0.exe SHA256`. A licence is per computer: see [penqw.in](https://penqw.in) or write to hello@penqw.in.
