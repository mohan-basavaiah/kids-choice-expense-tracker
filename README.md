# Kids Choice Expense Tracker

A local-first, mobile-friendly PWA starter for tracking shop money in and money out.

## Included
- Cash and UPI balances calculated separately from all recorded transactions.
- Sales and other income entries.
- Inventory purchases, rent, electricity, store expenses, transport, packaging, marketing, and other expenses.
- Edit/delete, date/type/payment/search filters.
- Monthly reports and category/payment breakdowns.
- JSON backup/restore and CSV export.
- IndexedDB local storage; no account or server-side transaction database.
- PWA manifest and service worker for install/offline shell caching.

## Run locally
For basic testing, open `index.html` in a modern browser. For PWA installation/offline caching, serve over HTTPS or localhost. Example, from this folder:
`python3 -m http.server 8000`
Then visit `http://localhost:8000`.

## Move to another device
On the old device, use Settings → Export full backup (JSON). Transfer that file securely to the new device, open the same app there, and use Restore backup. Restore replaces transactions on that device after confirmation. Keep independent backups in a safe place.

## Important accounting note
Cash and UPI balances represent the net of all logged transactions assigned to those payment methods since the tracker was first used. If starting with cash or UPI already on hand, record an Opening balance transaction using the corresponding payment method. This is a simple cash-flow tracker, not inventory valuation or profit accounting.

## Deployment
Deploy the folder contents to any static HTTPS host. Do not publish a personal backup JSON file to a public website. The provided service worker caches the app shell; transaction data remains in browser IndexedDB.
