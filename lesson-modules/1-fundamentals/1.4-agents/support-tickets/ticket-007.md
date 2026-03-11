# Support Ticket #2047

**Date:** January 20, 2026
**Customer:** Roberto Espinoza (Personal, Annual plan)
**Contact:** Roberto Espinoza
**Priority:** Medium
**Status:** Open

---

## Subject: Credit score hasn't updated in 6 weeks — still showing November value

## Description

Hi FinTrack support,

My credit score in the FinTrack dashboard has been stuck at 724 since early December. It's now been about 6 weeks and I know the score has changed because I checked it directly on Experian's website and it shows 741.

My FinTrack dashboard says "Last updated: December 8, 2025" under the credit score widget. The score should be refreshing monthly, but it's just... not.

A few things I've ruled out:
- This is definitely the right credit bureau — I see "Experian" listed in the app
- I haven't changed any account settings
- I re-authenticated the credit monitoring connection last week and it still didn't trigger an update

The 17-point difference matters to me. I've been working hard to improve my score and it's demotivating to not see that reflected in the app I use every day. I also rely on the score history chart to track my progress.

Is this a known issue? How can I force a refresh?

Roberto

---

## Internal Notes

- Experian API integration has had intermittent failures since a credential rotation issue on Dec 10 — automated monthly pull is silently failing for a subset of users without surfacing an error state in the UI
- UI shows "Last updated" date but does not show an error when the pull fails — this is a UX gap we need to fix (should show "Update failed" state)
- Engineering fix for Experian credential rotation: FT-2058, expected Jan 24
- Manual force-refresh workaround: have user disconnect and reconnect credit monitoring from Settings > Credit Score > Reconnect
- Should surface error states in credit score widget — adding to design backlog

---

## Tags

`credit-score` `experian` `data-sync` `bug` `silent-failure` `ux-gap`
