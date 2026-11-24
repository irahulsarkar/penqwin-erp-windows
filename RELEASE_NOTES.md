## Penqwin ERP 6.3.1

Pharmacy management software for India. An existing Penqwin ERP or SARK ERP install is upgraded in place and keeps its data.

### Windows

Works on Windows 10 and 11, 64-bit. No administrator rights needed; just run the installer.

| File | Size | SHA-256 |
|---|---|---|
| `Penqwin-ERP-Windows-6.3.1.exe` (the full installer) | 28.3 MB | `01ca493f40e3808d9da966b5bdbfc927d1f7464f2bff5046f0e03be9a960aedb` |
| `PenqwinERPSetup.exe` (a small downloader that fetches the newest version from this page) | 0.1 MB | `133072f5c3e8078678bdbbe0a73beaebb0c6bfedc4c083d004f4fcd640b3edb7` |

Neither installer is code-signed yet, so Windows SmartScreen may ask you to confirm before it runs. This release is for Windows only.

### New in 6.3.1

- **Activate online now works.** The activation screen connects to the Penqwin licence server (console.penqw.in): enter the activation key, the e-mail the licence was bought with and the drug licence number. Offline activation is still available.

Everything in [6.3.0](../../releases/tag/v6.3.0) is included. Every file's checksum is in `release-assets/SHA256SUMS.txt`.

## Penqwin ERP 6.3.0

Pharmacy management software for India. An existing Penqwin ERP or SARK ERP install is upgraded in place and keeps its data.

### Windows

Works on Windows 10 and 11, 64-bit. No administrator rights needed; just run the installer.

| File | Size | SHA-256 |
|---|---|---|
| `Penqwin-ERP-Windows-6.3.0.exe` (the full installer) | 28.3 MB | `f62d2edc84da47b7252df78d96a7a28ba2450cf61d6cb8b0ebe7157073ed7f56` |
| `PenqwinERPSetup.exe` (a small downloader that fetches the newest version from this page) | 0.1 MB | `133072f5c3e8078678bdbbe0a73beaebb0c6bfedc4c083d004f4fcd640b3edb7` |

Either one installs the same program. The full installer needs no internet while it runs. The downloader is tiny, installs without administrator rights, asks before every update, and opens the program in 5 seconds without updating if you do not answer. If Penqwin ERP was installed with the full installer, the downloader removes that older install after the new files are in place; your pharmacy data and licence are not touched.

`Penqwin-ERP-6.3.0-windows-x64.zip` and `latest-windows.json` are what the downloader reads. You do not need them. This release is for Windows only. The macOS and Linux files stay at [6.0.9](../../releases/tag/v6.0.9). Neither installer is code-signed yet, so Windows SmartScreen may ask you to confirm before it runs.

### New in 6.3.0

This release includes everything since 6.0.10. The version numbers in between were not released.

- **Edit a bill after it is posted.** Open a completed sales invoice or a posted purchase bill and choose Edit bill. The corrected bill replaces the old one under the same number, in one step; the old version stays in history and every edit needs a reason. A bill cannot be edited once it has an e-invoice IRN, falls in a closed year or a filed GST period, or has returns against it. A purchase also cannot be edited once its stock has been sold or moved, or if it has payments.
- A new first-run welcome screen, and the installer described above.
- New installs open in the top-bar layout, and the penguin assistant is off until you turn it on in Settings. Voice entry is a separate setting and is not affected. A computer that already chose a layout or turned the assistant on keeps its choice.
- Menus, pickers and pop-ups now stay inside the window instead of being cut off at the edge.
- Pressing Ctrl+Enter in a customer, doctor, supplier or product search that finds nothing opens the form to add a new one.
- A refreshed app icon, and a yellow glass style for notifications.

Every file's checksum is in `release-assets/SHA256SUMS.txt`.

## Penqwin ERP 6.0.10

Pharmacy management software for India. An existing Penqwin ERP or SARK ERP install is upgraded in place and keeps its data.

### Windows

Works on Windows 10 and 11, 64-bit. No administrator rights needed; just run the installer.

- `Penqwin-ERP-Windows-6.0.10.exe` (29.4 MB)
- SHA-256: `478c2ef0b96b7848d179bc007cd9a77c2fc79224581256b9be47f1532b257ae5`

This release is for Windows only. The macOS and Linux files stay at [6.0.9](../../releases/tag/v6.0.9). The Windows program in this release is built on the newer Wails 3 window shell: if printing to a receipt or label printer misbehaves, please tell hello@penqw.in.

### New in 6.0.10

- Penqwin ERP can now be installed silently for all users: `Penqwin-ERP-Windows-6.0.10.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART /SP- /ALLUSERS` (Program Files, listed in Windows' Installed apps for every account). Without `/ALLUSERS` it installs for the current user only, as before.
- The WhatsApp Business connection is shown as "Coming soon" until Meta's approval is complete. The WhatsApp buttons keep working as before: they open WhatsApp with the message written for you to send.
- New invoice designs, dispatch and LR details, a declaration and jurisdiction line, and image, Excel and CSV export of a bill.
- A print preview for every report: choose columns, paper and orientation, then print or save as PDF, Excel or CSV.
- Purchase orders, a stronger invoice import, and fewer buttons on busy screens.
- The dashboard sales chart has a legend and a 3-day average line.

Every file's checksum is in `release-assets/SHA256SUMS.txt`.

### New in 6.0.9

- Fixed a real, previously hard-to-notice bug: the "Sales, last 30 days" chart on the dashboard could draw its curve, its markers and its "today" dot at the wrong position the first time the program opened each day, correcting itself only once the screen was refreshed. The chart now waits for a real measurement of its own box before drawing anything in it.

### New in 6.0.8 (6.0.6 and 6.0.7 were not released on their own)

**The gateway, now the app's main screen**
- Opening the program (and finishing setup) now lands on the gateway: every module and screen reachable by a letter or two, no sidebar or menu bar in the way.
- A still-unactivated install is asked, before a single pharmacy-profile field, whether it already has a license key: activate first, or carry on free and activate later from Settings.
- The gateway shows the pharmacy's figures for the day, what needs attention, screens opened recently, and now the running program's own version number.

**Reports, tax and planning**
- A catalogue of around 55 reports, GST statements, a TDS/TCS register, and targets, budgets and assets.
- A medication sheet (dosage schedule) that can be handed to a patient or printed.

**Printing and the keyboard**
- One shared print engine behind every report and document: pages fill and continue properly, a report's own page setup (paper, margin, orientation) is remembered, and Alt+P prints whatever screen is open.
- Every screen can be worked without a mouse; a save always refreshes what is on screen.
- The first field of a screen is focused the moment it opens.

**Online UPI and WhatsApp**
- Collect UPI payments with a QR code on the bill through Razorpay or PhonePe, using your own gateway account.
- Send WhatsApp Business messages from the desktop program.

**Safer and clearer**
- No internal codes, ids or system keys are ever shown on a screen or a printout.
- A free, permanent plan (3 sales invoices, 3 purchase entries and 5 products a day) with no trial countdown; a one-time guided tour the first time the program is used.
- A number of real, previously hard-to-notice bugs fixed: warning and error banners that were rendering as invisible text in several places, a page-setup menu that could open off the bottom of a dialog, and a chart line that could vanish over a stretch of zero-sales days.

### New in 6.0.5

**Miscellaneous billing**
- Carry bags, delivery and other small charges come from a new master (Masters, Miscellaneous billing), each with its usual price and the income ledger its money is booked to.
- At the counter, add them in the calculation line (click Misc, or Alt+M): type, arrow to one, Enter. Change the quantity or the price for that bill. An item that is not in the master yet is created on the spot.
- They are added after tax and discount, carry no tax, and show on the bill, every printout and the PDF. A cancelled bill reverses them.

**A faster counter**
- Ctrl+A opens the settle window from anywhere on the counter, and Ctrl+A again settles the bill. Enter on an empty item line moves to the calculation line.
- A wider settle window with the mode on one key (C, U, D, K), a Cash received box that shows the change to return, and Enter to settle.
- A tabbed customer card (dues, credit, points, history, profile), the selected item and the substitute finder at the left of the calculation line, a closable shortcuts panel, and the arrow keys show the item name in the search box.
- After a sale you can save a copy of the bill as a PDF, a CSV or an Excel sheet.
- Long text that is cut off slides into view when you hover it.

**Import and suppliers**
- A much stronger import engine: any file, printed-bill CSVs, medicines created on the spot with the usual product form, and an import history that opens on request.
- Pay suppliers from the Suppliers page and the supplier profile, with the invoice numbers a payment settled, a payment summary to print and a supplier acknowledgement stamp.

### Also new since 6.0.0 (6.0.3 was not released on its own)

**Free trial, and activation**
- A copy with no licence runs free for 24 hours, with 5 sales and 5 purchase entries; the AI features are locked. Installing again does not give another trial. When it ends the program says so and shows how to reach us for an activation key; after activating you carry on where you left off, with your pharmacy details kept.
- Activation is by request file and licence file (online activation is switched off for now).

**Safer**
- A web page can no longer reach the program through the browser, updates are installed only if we signed them, the online UPI gateway secrets are stored sealed, and known weaknesses in the Go runtime and two libraries are fixed.

**Money in and out**
- A Transactions screen lists every movement of money (cash, bank, UPI and card) with who it was with, the bill, the bank account and the payment gateway. It can be printed.
- Interest on dues: a yearly rate and grace period for the shop, or a rate of its own (or none) for each customer. It is worked out on each unpaid bill and shown on statements, the ageing list and printouts. It is shown only; nothing is posted to your books.
- Outstanding bills can be printed for each customer and each supplier, and every screen with a table has a Print button.
- Collect UPI payments with a QR on the bill through Razorpay or PhonePe (with your own gateway account); each gateway can be linked to a bank account that the counter picks for you. Send messages with WhatsApp Business.

**Purchasing**
- Type a medicine on a purchase entry and pick it from the medicine directory to add it as a new product.
- A supplier bill number that is already entered offers to continue that bill. Items can be added to a bill that is already posted; the items already on it stay locked.
- Sales made before the supplier's bill is matched no longer distort margin until the bill is matched.

**Reports and accounts**
- A catalogue of reports, GST statements, a TDS and TCS register, targets, budgets and assets.
- A new page engine for printing: pages fill before they continue, and report page setup is remembered.

**Working faster**
- Every screen can be used from the keyboard. Rows and column headings can be reached with Tab, the arrow keys move between rows and between fields, F6 moves between the menu and the screen, typing a letter in a choice jumps to it, and lists scroll as you arrow through them.
- Alt shortcuts work while the cursor is in a field. Choosing from a dropdown moves on to the next field.
- A redesigned product form, with racks and shelves added right there. Windows no longer close when you click outside them.
- Whatever you save shows on screen at once: counts, lists, totals and recently added items.
- Screens fit smaller laptop windows better. Internal numbers and codes are no longer shown on screens or printouts.

### About Penqwin ERP

Point of sale, quotations, delivery challans and invoices; purchase orders, goods receipt and supplier payments; batch and expiry control; GST filing, GSTR-2B reconciliation and e-invoice; bank reconciliation, vouchers and financial reports; Schedule H1 and X registers. Records are stored on your own computer, with optional backup to Google Drive. The full list is in `docs/FEATURES.md` in this repository.

### Installing

Run `Penqwin-ERP-Windows-6.0.5.exe`; no administrator rights are needed. Verify the download with `certutil -hashfile Penqwin-ERP-Windows-6.0.5.exe SHA256`. More in `docs/INSTALL.md`.

The installer is not code-signed yet, so Windows SmartScreen may warn: choose More info, then Run anyway.

A licence is per computer: see [penqw.in](https://penqw.in) or write to hello@penqw.in.
