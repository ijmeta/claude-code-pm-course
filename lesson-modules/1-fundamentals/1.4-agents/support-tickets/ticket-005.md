# Support Ticket #2045

**Date:** January 18, 2026
**Customer:** James Calloway (Personal, Monthly plan)
**Contact:** James Calloway
**Priority:** High
**Status:** Open

---

## Subject: Budget overage notifications not working — went $400 over on Dining without any alert

## Description

Hi,

I'm pretty frustrated right now. I set a $300/month budget for Dining Out, and I apparently spent $712 this month without receiving a single notification.

I have notifications set up for:
- Alert at 80% of budget ($240)
- Alert when budget is reached ($300)
- Alert at every $50 over budget

I received none of these. I only discovered I was over budget when I manually checked the Budget page today.

My notification settings in the app show all three alert types are toggled ON for the Dining Out category. I have push notifications enabled on my iPhone (iOS 18, iPhone 15 Pro). I also have email notifications enabled as a backup.

I didn't get a push notification OR an email. The budget just silently blew past all my thresholds.

This defeats the entire purpose of using FinTrack. The whole reason I use a budgeting app is to get warned before I overspend, not to discover the damage afterward. If the notifications don't work, I might as well use a spreadsheet.

Can you please fix this? Has anyone else had this problem?

James

---

## Internal Notes

- Significant bug: budget notification pipeline has a defect affecting users whose spending hits multiple thresholds in a short window (e.g., several transactions in quick succession) — only the first threshold notification is queued; subsequent ones are dropped
- Engineering confirmed bug: FT-1978, introduced in the Dec 19 notification system refactor
- Affects users on iOS push AND email — not a device-specific issue
- Fix is in progress, targeted for hotfix release Jan 21
- James's frustration is warranted — proactive apology and acknowledgment of severity appropriate
- Consider offering one month credit given the material impact on his budget tracking

---

## Tags

`budget-notifications` `push-notifications` `ios` `bug` `high-priority` `hotfix-needed`
