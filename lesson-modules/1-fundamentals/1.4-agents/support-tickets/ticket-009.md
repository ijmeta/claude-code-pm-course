# Support Ticket #2049

**Date:** January 22, 2026
**Customer:** Liam Fitzgerald (Personal, Monthly plan)
**Contact:** Liam Fitzgerald
**Priority:** Medium
**Status:** Open

---

## Subject: Duplicate transaction — same charge showing twice after I added it manually

## Description

Hello,

I have a duplicate transaction issue. I have a charge from "Green Leaf Market" for $67.43 appearing twice in my transaction list.

Here's what happened: The transaction didn't show up in my feed for a couple of days (I think there was a sync delay), so I added it manually on January 19th. Then on January 21st, the transaction came through automatically via the bank sync — and now I have two entries for the same $67.43 purchase.

Both appear in my Groceries category and they're being counted toward my monthly budget. So my Groceries budget now thinks I've spent $134.86 instead of $67.43. My budget numbers are totally off as a result.

I deleted the manual entry, but the auto-synced one is still there and I'm not 100% sure which one is the "real" one from the bank. I don't want to accidentally delete the bank-synced record and have the transaction disappear from my history entirely.

How do I safely clean this up? And is there a way to prevent this from happening again if I add transactions manually in the future?

---

## Internal Notes

- Classic manual-add + delayed sync duplicate scenario — very common UX problem
- We currently have no duplicate detection logic when a manual transaction and a synced transaction match on amount + merchant + approximate date — this is a known gap (FT-1755)
- Safe resolution: the bank-synced transaction (showing bank account source) is the canonical record; the manual entry should be deleted
- Can help user identify which is which: bank-synced transactions show the linked account name (e.g., "Chase Checking") in transaction details; manual entries show "Manual Entry"
- Duplicate detection feature is on Q2 2026 roadmap — would auto-match and merge likely duplicates
- Consider adding a warning banner when manually adding a transaction: "We'll check for duplicates when your bank syncs"

---

## Tags

`duplicate-transaction` `manual-entry` `bank-sync` `budget-accuracy` `ux-gap` `deduplication`
