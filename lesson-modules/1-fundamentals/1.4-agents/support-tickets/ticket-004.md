# Support Ticket #2044

**Date:** January 17, 2026
**Customer:** Tamara Reyes (Personal, Annual plan)
**Contact:** Tamara Reyes
**Priority:** Medium
**Status:** Open

---

## Subject: Can't add Fidelity or Vanguard investment accounts

## Description

Hi FinTrack,

I've been trying to add my investment accounts to FinTrack so I can use the net worth tracker properly, but I'm running into issues with both Fidelity and Vanguard.

With Fidelity: When I search for "Fidelity" in the Add Account flow, I see it listed and click it, go through the Plaid login, enter my Fidelity credentials — but after it says "Connecting..." it comes back with "Fidelity Investments is not currently supported for automatic sync." But I've seen screenshots online showing it working for other people?

With Vanguard: Same issue. It gets further in the process (it shows my account list), I select my accounts, and then I get an error: "Unable to retrieve account data. This institution may not support balance/investment syncing."

I have a 401(k) at Fidelity and index funds at Vanguard. These are my biggest assets. Without them in FinTrack, the net worth tracker is basically useless — it only shows my checking/savings which is a fraction of my actual net worth.

Is investment account syncing actually supported? If so, what am I doing wrong?

Thanks,
Tamara

---

## Internal Notes

- Fidelity and Vanguard are partially supported via Plaid — Fidelity supports balance sync but NOT brokerage holdings detail; Vanguard OAuth updated in Q4 2025 and some account types (specifically individual brokerage) are temporarily broken
- This is a known gap in our investment tracking feature — we currently only pull balances, not individual holdings/positions
- Engineering tracking Vanguard OAuth fix: FT-2034, expected Jan 24
- Fidelity holdings detail is on the roadmap (Q2 2026) but not yet available
- Should update help docs to clarify what "investment account sync" actually includes — currently misleading
- Consider manual account entry as a workaround for now

---

## Tags

`investment-accounts` `fidelity` `vanguard` `net-worth` `plaid` `feature-gap` `documentation`
