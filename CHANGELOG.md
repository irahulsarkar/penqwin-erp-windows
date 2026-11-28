# Changelog

All notable changes to Penqwin ERP for Windows are listed here, newest first.

## 6.5.1

### Changed
- When Penqwin opens and a newer version is out, the update installs by itself after a 5-second countdown, then opens the new version. Not now still skips it.

### Fixed
- The update window on an existing install never changed: it stayed the one first installed. Penqwin now replaces it with the newest one shortly after it starts.

## 6.5.0

### Added

- **WhatsApp inside Penqwin.** WhatsApp Web slides up from the foot of the window. After settling a bill for a customer with a mobile number, send it as a PDF or PNG: the file waits in a small tray and can be dragged into the chat, or put there automatically if you choose that. Refill reminders, dues, wishes, order updates and other messages open in the same place. You always press Send yourself. WhatsApp does not permit other software to control WhatsApp Web, so automatic attaching is off until you turn it on.
- **Barcode on the PDF invoice.** The invoice number is printed as a barcode at the top right.
- **Supplier payment due dates.** Enter a due date on a goods receipt and be reminded before it; the reminder days are set in Settings.
- **Widgets button** in the navigation, for the calculator, notepad and other tools.
- **New lock screen and welcome screen**, a cleaner window frame, and new update and installer screens.
- Reports show dates as dd/mm/yyyy, and expiry dates as mm/yyyy.

### Changed

- The top bar layout and the switch to it are removed.
- AI Medicine Search is removed. The Medicine Directory stays.

### Fixed

- A bill settled for a customer now shows the customer in the "Invoice saved" window.

## 6.4.0

### Added
- An Update button beside the search box when a newer version is out.
- A redesigned dashboard and billing screen.
- New report designs: Register, Statement, Ledger, Compact and Classic.
- A button on goods receipts to open bills that are awaiting entry.

### Fixed
- Typing in a goods receipt no longer loses the cursor when it saves itself.
- The pharmacist's name prints on the barcode bill, a customer added with Ctrl+Enter shows on the bill, and the medication sheet opens in front of the print preview.

## 6.3.3

### Fixed
- 6.3.2 was built without the illustrations, so the shutter-opening welcome animation, the page illustrations and the setup picture were missing. They are back.

## 6.3.2

### Added
- Three new black-and-white invoice designs: Clean Business, Clean Executive and Clean Studio. No filled areas and no lines between items; choose them in the print window or in Settings, Print Templates.

### Changed
- The demo copy now opens on a realistic pharmacy (Shree Sai Medicals & General Stores) with six months of busy sales, purchases and stock.

## 6.3.1

### Changed
- "Activate online" now connects to the Penqwin licence server at console.penqw.in. Type the activation key, the e-mail the licence was bought with and the drug licence number; the licence is bound to the computer and saved. The offline method stays as a fallback.

## 6.3.0

This includes everything since 6.0.10; the version numbers in between were not released.

### Added
- Editing a posted sales invoice or purchase bill: the corrected bill replaces the old one under the same number, the old version stays in history, and a reason is required. Refused when the bill has an e-invoice IRN, is in a closed year or filed GST period, or has returns; a purchase is also refused when its stock has been sold or moved, or it has payments.
- `PenqwinERPSetup.exe`, a small installer that fetches the newest version from the GitHub releases, installs without administrator rights, and asks before every update.
- A new first-run welcome screen.

### Changed
- New installs open in the top-bar layout and start with the penguin assistant off; an existing choice is kept.
- Menus, pickers and pop-ups stay inside the window.
- Ctrl+Enter in a search that finds nothing opens the form to add a customer, doctor, supplier or product.
- A refreshed app icon and a yellow glass style for notifications.

## 6.0.10

### Added
- Silent, all-users install for managed and Microsoft Store installs: `/VERYSILENT /SUPPRESSMSGBOXES /NORESTART /SP- /ALLUSERS`.
- New invoice designs, dispatch and LR details, a declaration and jurisdiction line, and image, Excel and CSV export of a bill.
- A print preview for every report, with column choice, paper and orientation, and PDF, Excel and CSV output.
- Purchase orders and a stronger invoice import.

### Changed
- WhatsApp Business shows "Coming soon" until Meta's approval is complete; the WhatsApp buttons open WhatsApp with the message written.
- The Windows program is built on the Wails 3 window shell for this release.

## 6.0.9

### Fixed
- The dashboard's "Sales, last 30 days" chart could draw its curve, its markers and its "today" dot at the wrong position on the program's first open each day, only correcting itself on a refresh. It now waits for a real measurement of its own plotting area before drawing anything data-dependent in it.

## 6.0.8

This includes everything listed under 6.0.6 and 6.0.7 below (neither was released on its own).

### Added
- The gateway (every module and screen reachable by a letter or two) is now where the program opens and where setup finishes, instead of the dashboard.
- Before a single pharmacy-profile field, a still-unactivated install is asked whether it already has a license key, with a choice to activate first or continue free.
- A report catalogue of around 55 reports, GST statements, a TDS/TCS register, targets, budgets and assets.
- A medication sheet that can be printed or handed to a patient.
- One shared print engine across every report and document, with a remembered per-report page setup and Alt+P printing whatever screen is open.
- A keyboard-first interface throughout, with the first field of every screen focused on open.
- Online UPI collection on the bill through Razorpay or PhonePe, and WhatsApp Business messaging from the desktop program.
- A permanent free plan with a one-time guided tour, and no internal codes or ids shown anywhere in the UI.
- The running program's own version number, shown on the gateway.

### Fixed
- Several warning and error banners that rendered as unreadable, near-invisible text because of undefined color tokens.
- A page-setup menu that could open off the bottom edge of a dialog.
- A sales chart line that could vanish over a stretch of zero-sales days.
- A pharmacy name field on the offline activation form that was pre-filling from a not-yet-real placeholder.

## 6.0.5

This includes everything listed under 6.0.3 below (that version was not released on its own).

### Added
- Miscellaneous billing: a master of small charges (carry bag, delivery), added in the POS calculation line with Alt+M, booked to their own income ledger, shown on the bill, every printout and the PDF, reversed when a bill is cancelled. No tax is charged on them.
- Ctrl+A opens the settle window from anywhere on the counter and settles it the second time; Enter on an empty item line goes to the calculation line.
- A wide settle window: the payment mode on one key, a Cash received box with the change to return, Enter to settle.
- A tabbed customer card on the counter (dues, credit, points, history, profile); the selected item and the substitute finder in the left corner of the calculation line; a closable shortcuts panel; the arrow keys fill the item name into the search box.
- After a sale: save a copy of the bill as a PDF, a CSV or an Excel sheet.
- Text that is cut off slides into view on hover.
- A much stronger import engine (any file, printed-bill CSVs, packs against units, medicines created on the spot, import history on request) and an Import / Export menu.
- Supplier payments from the Suppliers page and the supplier profile, with the invoice numbers settled, a printable payment summary and an acknowledgement stamp.

### Changed
- The Settle Bill button is shown only on a phone-width window; on a computer the bill is settled from the keyboard.
- Notifications and menus sit above the page content, and the menu bar fits smaller windows.

## 6.0.3

### Added
- Penqwin ERP also runs on Linux.
- A free trial for a copy with no licence: 24 hours, 5 sales and 5 purchase entries, AI locked. It cannot be restarted by installing again, and an activation afterwards continues where the pharmacy left off. The activation screen opens on "Your free trial has ended" with the support phone, WhatsApp and e-mail.
- Pincode comes first in every address (pharmacy, customer, supplier); typing it fills the state and the city.
- Transactions: every movement of money (cash, bank, UPI, card) on one screen, printable.
- Interest on dues, by a shop rate or a rate of its own per customer, shown on statements, the ageing list and printouts (never posted to the books).
- Printable outstanding for each customer and supplier, and a Print button on every screen with a table.
- UPI collection through Razorpay and PhonePe, each linked to a bank account the counter picks automatically; WhatsApp Business messages.
- A catalogue of reports, GST statements, a TDS and TCS register, targets, budgets and assets.
- On a purchase entry: pick a medicine from the medicine directory to add it as a new product; continue a supplier bill that is already entered; add items to a posted bill.
- Full keyboard use: Tab to rows and headings, arrows between rows and fields, F6 between menu and screen, letter jumps in choices, lists that scroll with the arrows.
- Racks and shelves can be added from inside the product form.

### Security
- A web page can no longer read or change anything through the browser ("DNS rebinding"): the server answers only to addresses of this computer.
- Updates are installed only when signed by us; the update address is now penqw.in.
- The online UPI gateway secrets are sealed in the database, so a backup never carries them.
- Go 1.26.10 and newer libraries: 14 known vulnerabilities fixed.
- Online activation is switched off for now; activation is by request file and licence file.

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
