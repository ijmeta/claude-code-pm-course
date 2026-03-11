DESIGN REVIEW - NEW BUDGET OVERVIEW DASHBOARD
Date: January 9, 2026
Attendees: Kai Nguyen (Design Lead), Priya Sharma (Head of Product), Jordan Lee (PM, Core Experience), Riley Park (PM, Mobile), Frontend Lead (Arjun Mehta)

DISCUSSION:
Kai presented three mockup directions for a redesigned Budget Overview dashboard — the most-used screen in FinTrack. Current design dates from 2023 and has accumulated visual debt: inconsistent spacing, a progress bar system that doesn't scale well past 8 categories, and no at-a-glance indication of overall budget health.

Direction A: "At a Glance" — large summary card at top showing total budgeted vs. spent, with a circular progress ring. Category cards below in a scrollable grid. Clean and simple.

Direction B: "Category Deep Dive" — emphasizes individual category bars with projected month-end spend based on current pace. More analytical, shows velocity not just current state.

Direction C: "Hybrid" — keeps the summary ring from Direction A but adds a "Needs Attention" section that surfaces only the categories that are at risk (>80% spent with >10 days left in month). Other categories collapsed.

Team discussion heavily favored Direction C. Jordan noted that most users have 10-15 budget categories but only 2-3 are usually "interesting" at any given time — surfacing those automatically reduces cognitive load. Kai agreed this matches findings from last quarter's user research (users said they wanted to "know where to focus, not review everything").

Arjun raised an implementation concern: the "projected month-end spend" calculation in Direction B requires additional data processing and could add latency to the dashboard load time. If we include it in Direction C's "Needs Attention" cards, we should make it async/lazy-load.

Riley pushed for mobile-first layout — the current design was clearly designed desktop-first. Kai confirmed the new mockups were built mobile-first with a responsive desktop adaptation, which the team appreciated.

ACTION ITEMS:
- Kai to finalize Direction C mockups incorporating feedback by Jan 14
- Kai to produce mobile and desktop variants of the new layout
- Arjun to prototype the "Needs Attention" component and test performance impact
- Jordan to write acceptance criteria for budget dashboard redesign by Jan 13
- Priya to schedule user testing session for final mockups (target: week of Jan 19)

DECISION: Proceed with Direction C ("Hybrid") for budget dashboard redesign. Mobile-first layout required. Ship target: end of February.
