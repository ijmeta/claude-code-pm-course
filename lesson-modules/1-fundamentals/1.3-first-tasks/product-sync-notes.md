product sync - mon mar 10, 2:30pm

attendees: priya (head of product), david (cto), kai (design), jordan (PM), sam (eng lead), me

=== NOTIFICATIONS DISCUSSION ===

me presenting notification improvements proposal

current state is BAD:
- 143 tickets last quarter about notification issues
- users either get constant alerts or turn everything off
- 6 different notification types but poor targeting
- no distinction between urgent (bank disconnected!) and FYI (weekly summary)
- push delivery sometimes delayed 10-15 min (david flagged this)
- users missing bill due reminders = overdrafts = angry users

my proposal:
3 categories - urgent/important/fyi
- urgent = immediate (bank sync disconnected, bill due in 24hrs, budget 100% hit)
- important = digest eligible (weekly spending summary, budget at 80%, new transaction above $X)
- fyi = opt-in only (AI category suggestion, monthly net worth update, tips)

smarter bank sync alerts
- proactive "your Chase connection expires in 3 days" (not reactive after it breaks)
- reconnect flow directly from notification tap
- no more silent failures

budget overage warnings tiered:
80% → heads up
100% → alert
over budget → urgent (with $ amount over)

bill calendar reminders:
- 7 days out + 1 day out (two taps)
- user configurable window (some people want 3 days, some want 14)
- "bill paid" confirmation tap to dismiss

DAVID'S TECH NOTES:
"push notification delivery is unreliable because we're calling it synchronously"
- move to async queue (we already use redis for sessions)
- notification worker processes queue
- estimated 2-3 weeks to implement

db changes needed:
"notification_prefs table has 6 boolean columns, going to get messy fast"
wants jsonb preference object instead
showed example schema (urgent/important/fyi with delivery channel, quiet hours, digest schedule)

migration = 2 weeks, need gradual rollout
default existing users to "important = on, fyi = off"

"async will also improve API response times - push notifications are slow right now"

CONCERNS from team:

kai: settings UI will get complicated fast
- 3 tiers + channels + quiet hours + digest frequency = lots of options
- needs progressive disclosure (simple defaults + advanced mode)
- "can we hide the power settings behind an 'advanced' toggle?"

priya: how do we communicate the changes to users?
- announcement needed (blog + email + in-app)
- migration guide
- don't want to confuse users who have current prefs set
also timeline concern - 6 weeks min (eng + design + testing)
"this competes with bank sync reliability work in Q1"

jordan: bill reminders need calendar integration eventually
- right now we parse bill data from transactions
- some bills not detected automatically
- "manual bill entry is clunky, needs redesign before we lean into reminders"

sam: what if redis queue backs up?
- delayed notifications could be worse than no notifications
- need dead letter queue + monitoring
david: "will add alerting on queue depth, spec it out"

me: what about users who have push disabled at OS level?
priya: "email fallback + in-app notification center (build that eventually)"

OPEN QUESTIONS:
1. quiet hours - default 10pm-8am? user configurable?
2. bank sync alerts - always urgent or can user downgrade?
3. notification preferences: global only or per-account?
4. digest: daily or weekly? user choice?
5. rollback plan if push queue has issues?

DECISIONS:
✓ moving forward with 3-tier system (unanimous)
✓ async queue (david to spec redis setup + monitoring)
⏸ timeline Q1 or Q2? priya wants detailed plan, decide by eow
⏸ per-account prefs = v2, start with global only
⏸ bill calendar redesign = dependency, jordan to assess scope

ACTION ITEMS:
- me: comprehensive PRD by fri mar 14
- david: tech spec (arch, db schema, migration plan) by fri mar 14
- kai: notification settings UX flows + wireframes by mon mar 17
- jordan: bill detection + manual entry assessment by mon mar 17
- sam: eng estimate breakdown by tue mar 18
- me: competitive analysis (copilot/ynab/mint approach) by tue mar 18
- priya: schedule follow-up meeting wed mar 19 3pm

=== Q1 PRIORITIZATION ===

priya leading this discussion

5 initiatives competing for Q1:
1. bank sync reliability (critical, retention risk)
2. AI categorization accuracy (OKR: 87% → 95%)
3. notification improvements (discussed above)
4. mobile app improvements (high user demand)
5. investment tracking (growth feature, net worth play)

CAPACITY:
10 engineers total
3 on mobile til Q2 launch
7 available for core product
2-week sprints = 6 sprints in Q1

ESTIMATES:
bank sync reliability = 3 sprints (in progress)
AI accuracy = 4 sprints
notifications = 3 sprints
mobile improvements = 2 sprints (parallel with mobile team)
investment tracking = 4-5 sprints

math: can do ~2 major projects with 7 engineers given bank sync is already running

priya's criteria:
1. retention impact (churn risk vs growth)
2. user trust (accuracy + reliability = trust)
3. competitive pressure
4. OKR alignment
5. technical dependencies

DISCUSSION:

bank sync reliability:
david: "this is not optional, users leaving over this"
jordan: "28% monthly reconnect rate is embarrassing"
sam: "already started, would be bad to pause mid-sprint"
priya: "Q1, non-negotiable"

AI categorization:
me: "87% sounds ok but 1 in 8 transactions is wrong, users notice"
priya: "is this blocking revenue or just annoying?"
me: "both - power users who care about accuracy churning to Monarch"
david: "also tech debt - manual retraining is a mess"
priya: "if not Q1 for model overhaul, definitely Q1 for quick wins"

notifications:
me: "143 tickets, and silent bank sync failures are the worst UX"
priya: "agreed on urgency but the scope might be too big for Q1"
david: "can we split it? async infrastructure Q1, UX redesign Q2?"
priya: "yes - infra now, settings redesign later"

mobile improvements:
jordan: "users on mobile are frustrated, clunky transaction entry"
priya: "mobile team is doing this in parallel, it's funded separately"
sam: "just need design direction from kai"

investment tracking:
me: "net worth tracker is incomplete without investments, top feature request"
priya: "growth feature vs reliability - reliability wins in Q1"
david: "too much scope risk to add in Q1 while fixing bank sync"
priya: "Q2 - but build foundation (data model) in Q1 if we have bandwidth"

PRIYA'S STRAWMAN:
Q1: bank sync reliability + AI quick wins + notification infra + mobile improvements
Q2: investment tracking + notification UX redesign + AI model overhaul

rationale: fix the foundation (sync + accuracy + notifications) before adding features

PUSHBACK:

david: "AI quick wins and full pipeline overhaul are different scopes"
"can we commit to top 20 merchant fixes in Q1 even if full retraining is Q2?"
priya: "yes, merchant normalization list = Q1, automated pipeline = Q2"

sam: "investment tracking data model takes 1 sprint, worth doing in Q1?"
jordan: "agree - build foundation now, UI in Q2, avoids re-architecture later"
priya: "ok, 1 sprint for data model only, no UI"

REVISED PLAN:
Q1:
- bank sync reliability (3 sprints, 3 eng)
- AI merchant fixes + feedback loop (2 sprints, 2 eng)
- notification async infra (1 sprint, 2 eng)
- mobile improvements (2 sprints, mobile team)
- investment data model (1 sprint, 1 eng)

Q2:
- AI model overhaul + retraining pipeline (3 sprints)
- notification UX redesign (2 sprints)
- investment tracking UI (3 sprints)
- shared household budgets (4 sprints)

consensus: feels right, priya will finalize in roadmap doc

=== ENTERPRISE/POWER USER FEEDBACK ===

priya summarizing recent sales calls + user interviews

common power user requests:
- full transaction data export (CSV, Sheets-compatible)
- API access for personal automation (Zapier/n8n integrations)
- family sharing / household accounts (couples budgeting together)
- custom categories + sub-categories
- dedicated financial advisor integration

deal blockers for premium tier upsell:
- no family plan (couples are a huge segment)
- no data export (power users want their data)
- no custom categories (YNAB refugees want flexibility)

pipeline / opportunity:
- 8 enterprise / family deals in discussion (avg $24/mo family vs $12/mo individual)
- 4 blocked by no family sharing feature
- 2 blocked by no data export

priya: "family plan = Q2/Q3 investment but need scoping now so eng can plan"

=== SPRINT 18 PREVIEW ===

sam presenting

sprint starts mon mar 17

planned:
- bank sync: plaid webhook reliability fixes (priority!)
- AI: top 20 merchant normalization list (quick win)
- notification: redis queue setup (infrastructure only)
- mobile: transaction entry redesign (kai's new flow)
- bug fixes: 6 P1s in backlog (including duplicate transaction detection)

team availability:
sam out mar 24-28 (vacation)
mobile team at full capacity
core eng has 2.5 sprint capacity this sprint

goal: "ship the reliability fixes, prep foundation for Q1 roadmap"

=== PARKING LOT ===

- family/household account scoping (priya to schedule discovery)
- marketing wants "tax season" campaign for april (hold for priya approval)
- venmo/paypal sync escalated by 3 enterprise users (jordan investigating plaid support)
- competitor "Monarch Money" launched portfolio view last week (need to check out)

=== NEXT MEETINGS ===

wed mar 12: design review (dashboard redesign mockups)
thu mar 13: sprint 18 planning
wed mar 19: notification go/no-go
fri mar 21: Q1 roadmap finalization + OKR review

meeting done 3:41pm
