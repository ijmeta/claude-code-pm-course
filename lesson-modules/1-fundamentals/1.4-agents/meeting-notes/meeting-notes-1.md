PRODUCT SYNC - BANK SYNC RELIABILITY IMPROVEMENTS
Date: January 6, 2026
Attendees: Priya Sharma (Head of Product), Jordan Lee (PM, Core Experience), David Chen (CTO), Sam Okafor (PM, Integrations), Kai Nguyen (Design Lead)

DISCUSSION:
Bank sync reliability is our most common support ticket category — roughly 34% of all tickets in Q4 2025. Priya opened with the data: we're seeing a 6.2% weekly disconnection rate across linked accounts, with Chase, Wells Fargo, and Bank of America accounting for 73% of reported issues. David noted that Plaid's OAuth upgrade path is the root cause for most Chase disconnections specifically — Plaid deprecated a legacy token flow in December and our migration was only partially complete when the cutover happened.

Sam walked through the three main failure categories: (1) OAuth token expiration without automatic refresh, (2) institutions that require periodic re-authentication and don't notify us, and (3) Plaid webhook delivery failures that cause stale data without surfacing an error state to users. All three are fixable but require different approaches.

Jordan raised the UX side: even when sync fails, users often don't know until they manually check. The current "last synced" timestamp is small and easy to miss. Kai showed quick mockups of a more prominent sync status indicator — a colored badge on each account card (green = healthy, yellow = delayed, red = disconnected). Team responded positively to the concept.

David estimated 2-3 sprints to complete the Plaid OAuth migration and implement retry logic for webhook failures. The UX improvements are lighter lift and could ship sooner.

ACTION ITEMS:
- David to scope full Plaid OAuth migration and provide engineering estimate by Jan 9
- Sam to audit all 47 supported institutions for re-auth notification support by Jan 13
- Kai to finalize sync status indicator designs by Jan 12
- Jordan to draft user-facing copy for sync error states (clear, non-technical language)
- Priya to update roadmap with bank sync reliability as Q1 2026 priority

DECISION: Elevate bank sync reliability to P0 for Q1 2026. Plaid OAuth migration and sync status UX improvements to ship together in February release.
