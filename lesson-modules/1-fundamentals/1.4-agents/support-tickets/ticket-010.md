# Support Ticket #2050

**Date:** January 23, 2026
**Customer:** Nadia Thornton (Personal, Annual plan)
**Contact:** Nadia Thornton
**Priority:** Low
**Status:** Open

---

## Subject: Need to export all my transactions to CSV for taxes — can't find the option

## Description

Hi FinTrack,

Tax season is coming up and I need to export all of my 2025 transactions to a CSV file so I can give them to my accountant. I've looked everywhere in the app and I cannot find an export option.

I've checked:
- Account settings
- Each individual account page
- The Transactions tab (no export button visible)
- The Help Center (searched "export" — found nothing useful)

I have about 3,000 transactions from 2025 across four linked accounts. My accountant needs a spreadsheet with date, merchant, amount, and category columns to reconcile everything and flag potential deductions.

Is data export a feature that exists? If so, where is it hiding? If not — this seems like something a lot of people would need around tax time. I'm happy to pay for it as an add-on if needed, but honestly it feels like something that should just be available.

Thanks,
Nadia

---

## Internal Notes

- Data export IS available but very poorly discoverable — it's buried at Settings > Data & Privacy > Export My Data, not in the Transactions view where users logically look for it
- Current export includes: date, merchant, amount, category, account, notes — exactly what she needs
- Export is limited to date ranges up to 12 months at a time; for full year 2025 she'll need one export (Jan 1 – Dec 31, 2025)
- This is a significant UX discoverability issue — "Export Transactions" button should be on the Transactions page itself, not buried in Settings
- Creating UX improvement ticket: FT-2071 — add export button to Transactions view
- High seasonal volume expected for this ticket type in Jan-April (tax season); consider adding a Help Center article and in-app banner pointing to export feature

---

## Tags

`data-export` `csv` `tax-season` `discoverability` `ux-gap` `settings` `transactions`
