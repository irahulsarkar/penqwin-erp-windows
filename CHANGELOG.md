# Changelog

All notable changes to Penqwin ERP for Windows are listed here, newest first.

## 6.0.3

### Added
- Penqwin ERP also runs on Linux.
- A window of its own on Windows and Linux: a title bar with a search box (pages, products with their stock and rack, invoices), back and forward buttons, an online / offline indicator and a display menu for text size, contrast and motion.
- Transactions: every movement of money (cash, bank, UPI, card) on one screen, printable.
- Interest on dues, by a shop rate or a rate of its own per customer, shown on statements, the ageing list and printouts (never posted to the books).
- Printable outstanding for each customer and supplier, and a Print button on every screen with a table.
- UPI collection through Razorpay and PhonePe, each linked to a bank account the counter picks automatically; WhatsApp Business messages.
- A catalogue of reports, GST statements, a TDS and TCS register, targets, budgets and assets.
- On a purchase entry: pick a medicine from the medicine directory to add it as a new product; continue a supplier bill that is already entered; add items to a posted bill.
- Full keyboard use: Tab to rows and headings, arrows between rows and fields, F6 between menu and screen, letter jumps in choices, lists that scroll with the arrows.
- Racks and shelves can be added from inside the product form.

### Changed
- A redesigned product form; windows no longer close when clicking outside them.
- Saved changes show on screen at once, with no refresh.
- Alt shortcuts work inside a field; choosing from a dropdown moves on to the next field.
- A new page engine for printing and report page setup.
- Screens fit smaller laptop windows; tables keep whole words together; header buttons wrap.
- Internal numbers and codes are no longer shown.

### Fixed
- Sales made before a supplier's bill is matched no longer distort margin until the bill is matched.
- The browser no longer offers saved addresses on number fields.

## 6.0.0

### Added
- Profit and margin on each invoice, with a line-by-line view on request. Shown on screen only; never printed.
- Spend, profit and margin per customer, filterable by all time, a financial year or a date range, in the customer list and on the customer page.
- Quick actions on the dashboard with live figures; compact two- and three-column lists on wide screens.
- Product search shows where stock is held (store or godown).
- Optional PTR column on invoices, off by default, on every print template.
- Short maker name on one line on the wholesaler bill.
- Redesigned sidebar and menu icons, and a welcome screen when the app opens.

### Changed
- Customer, supplier, doctor and bank account forms use the full window width.
- The top bar keeps its labels on narrower windows.
- The Y and N keys for on/off switches are hinted only inside forms.
- Suggestion lists close when focus moves to another field.

### Fixed
- Settling a bill no longer stops on stock held in a godown.
- Patient details for scheduled drugs are asked once per bill, not for each scheduled item.
- The customer list opens faster on shops with a long sales history.
