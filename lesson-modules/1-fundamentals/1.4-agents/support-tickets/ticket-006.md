# Support Ticket #2046

**Date:** January 19, 2026
**Customer:** Sophie Harrington (Personal, Annual plan)
**Contact:** Sophie Harrington
**Priority:** High
**Status:** Open

---

## Subject: App crashes every time I open the Net Worth screen on iOS 17

## Description

Hello,

The FinTrack app crashes instantly whenever I try to open the Net Worth screen. Every single time — no freeze, no loading, just immediate crash back to the home screen.

My setup:
- iPhone 12 Pro
- iOS 17.7.2 (I haven't updated to iOS 18 yet)
- FinTrack app version 3.4.1

The crash happens the moment I tap the "Net Worth" tab in the bottom navigation. All other sections of the app work fine — I can see transactions, budgets, the bill calendar, everything else. Just Net Worth causes the crash.

I've tried:
- Force-closing the app and reopening
- Uninstalling and reinstalling the app
- Restarting my phone

None of these fixed it. The crash has been happening since I updated to FinTrack 3.4.1 last Tuesday. It worked fine in the previous version.

I really need access to the net worth screen — it's actually the main reason I pay for FinTrack. I track my assets and liabilities every month. Is there a way to roll back to the previous version, or is a fix coming soon?

Sophie

---

## Internal Notes

- Confirmed iOS 17 crash bug introduced in version 3.4.1 — the new chart rendering library (upgraded for iOS 18 performance improvements) is incompatible with iOS 17's Metal rendering stack
- Affects iPhone models running iOS 17.x — NOT affecting iOS 18.x users
- Engineering has a fix in test, hotfix release 3.4.2 targeting Jan 22
- Cannot roll back App Store versions for users, but can advise them to update to iOS 18 as an alternative workaround
- Approximately 18% of our iOS user base is still on iOS 17 — this is a significant impact
- Should post to status page and consider in-app banner for affected users

---

## Tags

`mobile` `ios` `crash` `net-worth` `ios-17` `bug` `hotfix-needed` `high-priority`
