# Support Ticket #2041

**Date:** January 14, 2026
**Customer:** Marcus Webb (Personal, Annual plan)
**Contact:** Marcus Webb
**Priority:** High
**Status:** Open

---

## Subject: Chase bank sync disconnected — can't get it to reconnect

## Description

Hi FinTrack team,

My Chase checking and savings accounts have been disconnected for the past two days. I noticed when I saw my dashboard showing no new transactions since January 12th.

I've tried reconnecting through the "Fix Connection" button in the Accounts tab but it just spins for a while and then shows a generic error: "Unable to connect to Chase at this time. Please try again later."

I've tried:
1. Logging out of FinTrack and back in
2. Disconnecting and re-adding the Chase connection from scratch
3. Using both the mobile app and web browser
4. Waiting overnight and trying again this morning

Every time I re-add Chase, it takes me through the Plaid login flow, I enter my Chase credentials, it says "Connection successful!" — and then a few minutes later the account shows as disconnected again.

I rely on FinTrack daily to track my spending against my monthly budget. Without the Chase sync working, I have no visibility into my largest account. This is really frustrating given I'm paying for the annual plan.

Is there a known issue with Chase connections right now? Any ETA on a fix?

Thanks,
Marcus

---

## Internal Notes

- Plaid status page shows intermittent issues with Chase OAuth connections as of Jan 13 — likely related
- User has been on annual plan for 11 months, renewal coming up in February
- Chase recently updated their OAuth flow; Plaid compatibility patch expected Jan 16
- Recommend acknowledging the known issue and providing ETA rather than generic troubleshooting steps
- Consider proactive outreach to all affected Chase users

---

## Tags

`bank-sync` `plaid` `chase` `reconnection` `high-priority` `known-issue`
