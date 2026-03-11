# Support Ticket #2043

**Date:** January 16, 2026
**Customer:** Derek Okonkwo (Personal, Annual plan)
**Contact:** Derek Okonkwo
**Priority:** Medium
**Status:** Open

---

## Subject: Transactions from the last 3 days are missing — Plaid sync delay?

## Description

Hi there,

I noticed this morning that my FinTrack transaction feed hasn't updated since January 13th. I can see the transactions in my actual bank app (Wells Fargo and a Capital One credit card), but they're not showing up in FinTrack.

Specifically missing:
- A $134 grocery run at Whole Foods on Jan 14
- A $22 Uber on Jan 14
- Multiple small transactions on Jan 15 (coffee, lunch, gas)
- A $289 credit card payment on Jan 15

My accounts show "Last synced: Jan 13, 2:14 PM" in FinTrack, which is about 3 days ago. I've tried hitting the manual refresh button and it just says "Syncing..." for a minute and then nothing changes.

Is there a Plaid outage? Or is something wrong specifically with my account connections? I have a monthly budget review I do every Sunday and missing 3 days of transactions makes it pretty useless.

Any help would be appreciated.

Derek

---

## Internal Notes

- Plaid is reporting elevated latency on Wells Fargo and Capital One connections since Jan 13 — webhook delivery delays of 24-72 hours affecting a subset of users
- Not a FinTrack bug per se, but we should communicate proactively rather than waiting for users to file tickets
- Manual "force sync" feature would help here — adding to backlog (FT-2011)
- Transactions will auto-populate once Plaid resolves the delay; estimated resolution Jan 17
- Recommend flagging on status page and sending proactive email to affected users

---

## Tags

`bank-sync` `plaid` `missing-transactions` `wells-fargo` `capital-one` `sync-delay`
