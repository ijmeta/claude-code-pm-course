SPRINT RETROSPECTIVE - Q4 2025 SPRINT 6 (DEC 16 - DEC 30)
Date: January 5, 2026
Attendees: David Chen (CTO), Priya Sharma (Head of Product), Riley Park (PM, Mobile), Jordan Lee (PM, Core Experience), Sam Okafor (PM, Integrations), Engineering team (6 engineers), Kai Nguyen (Design Lead)

SPRINT SUMMARY:
Goal was to ship the notification system refactor, investment tracking beta, and iOS performance improvements. Shipped 2 of 3 — the notification system refactor and iOS performance improvements went out. Investment tracking beta was partially shipped (account balance sync only, holdings detail deferred).

WHAT WENT WELL:

1. iOS performance improvements shipped on time and are working well. Dashboard load times improved 38% on average. Users have noticed — app store reviews mentioning speed increased significantly.

2. Cross-team communication between design and engineering improved this sprint. Kai's practice of posting daily design update screenshots in Slack meant engineers always had current specs — no "wrong version" confusion like in Sprint 4.

3. The QA process for the Plaid SDK integration held up. Tomas caught three edge cases during testing that would have caused silent data corruption in production. Investment in test coverage is paying off.

4. Sprint planning estimates were more accurate this sprint — we committed to 68 points and shipped 64. Previously we were committing to 80+ and consistently missing.

WHAT DIDN'T GO WELL:

1. The notification system refactor introduced a critical bug (budget notification pipeline failure, ticket #2045 and others). We shipped a refactor without sufficient regression testing on notification delivery paths. This has become our most urgent production issue heading into Q1 and has impacted real users. We need a better "pre-ship checklist" for changes to core notification infrastructure.

2. Investment tracking beta was partially shipped but the communication of "what's actually in the beta" was confusing internally and externally. Users expected holdings detail based on the announcement language; we only shipped balance sync. Priya took responsibility for this — the announcement copy wasn't reviewed against the actual shipped scope.

3. Holiday sprint capacity was overestimated. We planned for 75% capacity during the Dec 16-30 window but actual availability was closer to 55% due to informal holiday time and reduced energy. This is predictable — we should plan for 50% capacity in future holiday sprints.

4. Three engineering decisions were made without PM awareness during the sprint (two API design choices and one database schema change). These didn't cause immediate problems but could constrain future feature work. Need a clearer norm around when engineering decisions require PM/design input.

IMPROVEMENTS FOR NEXT SPRINT:

1. Add "notification regression checklist" to the definition of done for any changes touching the notification system.
2. All external communications about shipped features must be reviewed by PM against actual ship scope before publishing.
3. Holiday sprints: plan for 50% capacity, commit to 40% of normal story points.
4. Weekly "decision log" — engineering posts any architectural decisions in a shared doc so PM and design stay aware.

ACTION ITEMS:
- David to create notification regression checklist by Jan 7
- Priya to draft "announcement review" process for shipped features by Jan 9
- Scrum master (Riley) to update sprint planning template with holiday capacity adjustments
- David to set up weekly decision log Slack channel and document the norm by Jan 7

OVERALL: A mixed sprint. Strong technical execution in some areas, a significant quality miss in others. The notification bug is our top priority for Q1 Sprint 1 and must be resolved before anything else ships.
