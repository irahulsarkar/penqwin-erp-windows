## Penqwin ERP 6.0.3

Pharmacy management software for India, now for Windows and Linux. An existing Windows installation is upgraded in place and keeps its data.

| File | What it is | Size | SHA-256 |
|---|---|---|---|
| `Penqwin-ERP-Windows-6.0.3.exe` | Windows 10 and 11 (64-bit): the installer to use | 27.9 MB | `8CF5B06EE52C83519FFFEF2B6C7DBBF978DB39069544256918BAA1604874CA9B` |
| `Penqwin-ERP-Demo-Windows-6.0.3.exe` | Windows: a trial copy with sample data, ready to try with no licence; it keeps its own data and does not touch a real installation | 33.7 MB | `D539BD8CBFA9D7BFB18774C3F38C95F38BACB3DCBFACECDCE3A37027E5C7C7CB` |
| `Penqwin-ERP-Linux-6.0.3.deb` | Linux, 64-bit Intel/AMD: a package for Ubuntu 24.04 and newer, Debian 13 and the distributions of that age | 26.7 MB | `9BC496464CF7E50F8AE1B218C914FD3B2CDBBDA81E423A5732C7508E8B2BD93E` |
| `Penqwin-ERP-Linux-6.0.3.tar.gz` | Linux, 64-bit Intel/AMD: the same program as a plain archive, for any distribution with GTK 4 and WebKitGTK 6 | 29.1 MB | `F99E59429F6193FF2CA17CEBE06B4DB78D0EE0AC75670D882531CBC01D859AA3` |

Pick the file for your system. The Demo file is a trial copy with sample data. macOS is not in this release.

### What is new since 6.0.0

**A window of its own (Windows and Linux)**
- The program draws its own title bar in its own colours, with a search box in the middle: type a page, a product or an invoice number and open it from there. A product shows how many can be sold and where the stock and the rack are.
- Back and forward buttons, an online / offline indicator, and a display menu (text size, higher contrast, reduce motion).
- Runs on Linux as well as Windows, with a tray icon, one copy at a time and desktop alerts.

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

**Windows:** run `Penqwin-ERP-Windows-6.0.3.exe`; no administrator rights are needed. Verify the download with `certutil -hashfile Penqwin-ERP-Windows-6.0.3.exe SHA256`.
**Linux:** `sudo apt install ./Penqwin-ERP-Linux-6.0.3.deb`. Verify with `sha256sum Penqwin-ERP-Linux-6.0.3.deb`. More in `docs/INSTALL.md`.

A licence is per computer: see [penqw.in](https://penqw.in) or write to hello@penqw.in.
