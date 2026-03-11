SPRINT PLANNING - Q1 2026, SPRINT 1 (JAN 5 - JAN 16)
Date: January 5, 2026
Attendees: Priya Sharma (Head of Product), David Chen (CTO), Riley Park (PM, Mobile), Sam Okafor (PM, Integrations), Engineering team (6 engineers)

SPRINT GOAL: Begin investment tracking MVP and ship iOS stability fixes from Q4 backlog.

CAPACITY REVIEW:
Team has 72 story points available. One engineer returning from holiday PTO Jan 8 (partial capacity first week). Two planned company meetings consuming ~4 hours each. Effective focus time: 68% accounting for meetings and code reviews.

BACKLOG REVIEW:
- Investment account sync (Fidelity/Vanguard holdings): 28 points
- Investment dashboard UI (portfolio overview, allocation chart): 22 points
- iOS Net Worth crash fix (iOS 17 compatibility): 8 points
- Budget notification pipeline bug fix: 6 points
- Manual account entry improvements (better for 401k, real estate): 9 points
- Tech debt: Plaid SDK upgrade to v14: 12 points

Committed to sprint: 63 points. Team comfortable; leaves buffer for bug escalations.

NOTABLE DECISIONS:
- Investment tracking MVP scoped to: account balance sync + basic allocation chart. Holdings-level detail (individual stocks/funds) deferred to Sprint 3.
- iOS crash fix elevated to top of sprint given active customer impact (ticket #2046 and similar).
- Plaid SDK upgrade included now to unblock OAuth migration work planned for Sprint 2.
- Deferred: savings rate dashboard improvements (Q1 Sprint 3), credit score UI refresh (Q1 Sprint 4).

RISKS:
- Fidelity API documentation is incomplete for holdings endpoint — Sam to clarify with Plaid integration support before engineering starts implementation.
- Riley flagged that iOS 17 crash fix may reveal additional Metal rendering issues — timebox investigation to 1 day before escalating.

ACTION ITEMS:
- Engineers to break down investment tracking stories and self-assign by EOD Jan 5
- Riley to file Fidelity API documentation gap with Plaid support today
- David to review iOS crash root cause analysis before Jan 7
- Priya to confirm investment tracking MVP scope with Maya (CEO) before Jan 8

Sprint demo scheduled for January 16 at 2pm PT.
