# Support Ticket #2042

**Date:** January 15, 2026
**Customer:** Priya Nambiar (Personal, Monthly plan)
**Contact:** Priya Nambiar
**Priority:** Medium
**Status:** Open

---

## Subject: Amazon purchases keep getting categorized as "Business Expenses" — should be "Shopping"

## Description

Hello,

I'm having an ongoing issue with how FinTrack categorizes my Amazon transactions. For the past month, virtually every Amazon purchase I make gets automatically labeled as "Business Expenses" instead of "Shopping."

I don't run a business. These are regular personal purchases — household items, books, clothing, etc. I've manually corrected the category five or six times now, but it just reverts back to "Business Expenses" the next time an Amazon charge comes through.

I tried using the "Always categorize this merchant as..." option after one correction, but it doesn't seem to be sticking. Last week I bought a lamp from Amazon for $47.99 — definitely not a business expense — and it was auto-categorized as "Business" again within an hour of syncing.

This matters because my "Shopping" budget is completely off. FinTrack thinks I'm way under budget on Shopping when actually I've gone over. And my "Business Expenses" category looks artificially inflated.

How do I permanently fix this? Why does the AI keep overriding my manual corrections?

Thanks,
Priya

---

## Internal Notes

- Known issue: AI categorization model was retrained in December and over-indexed on Amazon transactions being business-related, possibly due to training data skew
- User-defined merchant rules should override AI — investigating bug where rule is not persisting correctly for Amazon (large merchant with many sub-categories)
- Engineering ticket open: FT-1892 (merchant rule persistence bug)
- Workaround: Have user create a manual rule via Settings > Categorization Rules for "Amazon" → "Shopping"; this path appears to persist correctly unlike the in-transaction flow
- Estimated fix: Sprint ending Jan 23

---

## Tags

`ai-categorization` `amazon` `merchant-rules` `bug` `budget-accuracy`
