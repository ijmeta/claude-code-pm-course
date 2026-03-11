# Customer Feedback Session - Tuesday Mar 11, 3pm

attendees: me (PM), jordan (PM), customer success team (2 people), 5 FinTrack users on video call

## Session Context

Recruited 5 users via in-app survey ("would you join a 60-min feedback call?"). Mix of personas across different usage patterns. Ran as a facilitated group session — users heard each other's pain points which surfaced a lot of "YES, that too!" moments.

---

## User Profiles

**User 1: Marcus T., 29, Software Engineer, San Francisco**
- Single, early career, 2 years on FinTrack
- Use case: tracking spending, saving for house down payment
- Connected accounts: 2 checking, 1 savings, 1 credit card

**User 2: Diane & Chris P., 41/43, Marketing Manager + Teacher, Chicago**
- Married couple (Diane uses FinTrack, Chris does not — pain point!)
- Use case: household budgeting, saving for kids' college
- Connected accounts: 3 checking, 2 credit cards, 1 mortgage

**User 3: Keisha R., 34, Nurse, Atlanta**
- Single, actively paying off $22k student debt
- Use case: debt payoff tracker, strict budget adherence
- Connected accounts: 1 checking, 1 savings, 3 credit cards

**User 4: Tom W., 52, Small Business Owner, Denver**
- Separated personal and business finances (mostly)
- Use case: personal budgeting, net worth tracking
- Connected accounts: 4 accounts, manually added investment balances

**User 5: Preethi S., 27, Graduate Student, Boston**
- Low income, very budget-conscious, switched from Mint after it shut down
- Use case: making $1,800/month stretch, no overdrafts
- Connected accounts: 1 checking, 1 credit card

---

## Discussion Sections

### What's Working Well

Before going into pain points, asked what they love (important to hear this!):

**Budget progress bars:**
Marcus: "The bars are the first thing I look at every morning. I know instantly if I'm on track."
Keisha: "I literally changed my spending behavior because of those bars. I see Shopping at 70% and I stop."
Preethi: "Best feature in the app. Simple and scary at the same time." (laughter)
→ Unanimous love for budget progress bars. Do not change this.

**Spending summaries:**
Tom: "Monthly summary emails are actually useful. I read them. Can't say that about many emails."
Keisha: "The AI categories are mostly right — I appreciate that it even tries."

**Simplicity vs Mint:**
Preethi: "Mint was overwhelming. Too many things happening. FinTrack feels calmer."
Marcus: "Agreed. I didn't need most of Mint's features. FinTrack feels focused."

---

### Pain Point 1: Bank Sync Disconnecting

Every single user mentioned this unprompted. Loudest pain point of the session.

Marcus: "Chase disconnects constantly. Maybe once every 2-3 weeks. I have to reconnect and I always worry I missed transactions."
Keisha: "I have 3 credit cards and at least one is broken at any given time. It's exhausting."
Preethi: "I have my checking account synced. It disconnected last week and I didn't notice for 5 days. I almost overdrafted because I thought I had more money."

→ Preethi's story got a lot of nods. Silent disconnect = dangerous for users on tight budgets.

Diane: "I've just stopped relying on it being accurate. I manually check my bank app and FinTrack. Kind of defeats the purpose."

Tom: "Is it a Plaid issue or a FinTrack issue? I never know who to blame."
(good question — CS confirmed this is partly Plaid but also FinTrack's handling of webhook failures)

**What they want:**
- A clear notification when an account disconnects (not just a red icon they have to notice)
- "Reconnect" should take them directly into the fix, not make them hunt through settings
- Some kind of status indicator: "All accounts synced ✓" vs "1 account needs attention"

---

### Pain Point 2: AI Miscategorizing Transactions

This came up right after bank sync. Keisha had particularly strong feelings.

Keisha: "Amazon. Oh my god. Amazon gets miscategorized every single time. I buy groceries on Amazon Fresh, household supplies, electronics — it just says 'Shopping' for everything."
Marcus: "Same. Amazon Prime order could be anything. The AI doesn't know."
Tom: "Venmo is the worst for me. I pay my dog walker through Venmo. FinTrack thinks I'm going out to eat."

Preethi: "I've given up fixing them. It takes too long. But then my budget numbers are wrong and I don't trust them."

→ This is a trust erosion issue. If users stop fixing, the data degrades and the product becomes less useful over time.

**What they want:**
- One-tap recategorization (current flow has too many steps)
- "Remember this for future transactions from [merchant]" option — persistent rule
- Learn from corrections faster (Marcus noticed it doesn't seem to learn)
- Better Amazon handling: ask "was this grocery, household, or electronics?" on first Amazon purchase

Diane: "Can it ask me once when a new merchant appears? A quick pop-up: 'What is [new merchant]?' — I'd do that."

---

### Pain Point 3: No Investment Account Support

Tom and Marcus both brought this up. Others nodded.

Tom: "My net worth number is wrong. I have a Fidelity account with $180k in it. FinTrack has no idea. It thinks my net worth is negative because it only sees my mortgage."
Marcus: "I have a 401k and a Roth IRA. I manually added rough estimates but they're stale. I'd love it to sync."

Jordan (PM, our team): "Which platforms are most important to you?"
Tom: "Fidelity and Schwab. Probably covers 80% of people."
Marcus: "Fidelity, Vanguard. Robinhood would be nice."
Keisha: "I have a small Robinhood account. Nothing big but I want to see it."
Preethi: "I have almost nothing invested yet but I'd use this when I start."

→ Clear demand. Investment tracking would complete the financial picture, especially for net worth accuracy.

---

### Feature Requests (Unprompted)

Asked "if you could add one feature, what would it be?" — went around the room:

Marcus: "Venmo and PayPal sync. I use Venmo constantly and none of those transactions show up."
Diane: "Shared budget with my husband. He needs to see the same view I do. Right now I show him screenshots. It's ridiculous."
Keisha: "A debt payoff calculator. Show me: if I pay an extra $200/month, I'll be debt-free in X months. I'd look at that every day."
Tom: "CSV export. I want to pull my data into a spreadsheet. Power user thing but I really want it."
Preethi: "Bill negotiation tool. Like, 'your internet bill is $89, average in Boston is $65, want help negotiating?' That would be wild."

(Bill negotiation tool got a big reaction from everyone — lots of "ooh that's smart" comments)

Diane (follow-up): "Also, custom categories. I want a 'Childcare' category. Right now I put it in 'Other.'"
Keisha: "Custom categories +1. I want 'Student Loans' as its own category, not buried in debt payments."

---

### Competitor Context

Asked: "What did you use before FinTrack? Why did you switch?"

Marcus: "Mint. RIP. Had to find something new. Tried YNAB, too complex. Tried Copilot, too expensive. FinTrack felt right."
Preethi: "Mint. I miss nothing about it except it was free. FinTrack's $8/month is worth it."
Keisha: "YNAB for a year. I wanted to love it. The envelope system was too much overhead. I spend 2 minutes in FinTrack vs 20 in YNAB."
Tom: "Personal Capital (now Empower). It kept trying to sell me wealth management services. The ads felt gross. FinTrack feels cleaner."
Diane: "Nothing before. Spreadsheet for 10 years. My sister convinced me to try FinTrack."

**What FinTrack does better:**
- Simpler than YNAB
- Less predatory than Personal Capital/Empower
- Cheaper than Copilot
- Survived Mint's death (still here, still improving)

**Where competitors are better:**
- Personal Capital has investment tracking (Tom misses this)
- YNAB has more budgeting control / zero-based method (Keisha misses the philosophy even if not the complexity)
- Copilot has better mobile app (Marcus uses both right now)

---

### NPS Discussion

Ran a quick NPS at end of session. Asked: "How likely are you to recommend FinTrack to a friend? (0-10)"

Marcus: 8 ("would go to 9 if bank sync was reliable and investments synced")
Diane: 6 ("I'd recommend it if it had family sharing — hard to recommend something my husband can't use")
Keisha: 9 ("genuinely changed my financial habits, just needs the AI fix")
Tom: 7 ("good but incomplete without investments")
Preethi: 8 ("love it, just wish bank sync was more reliable")

In-session NPS average: 7.6 (extrapolated score ~38)
→ Our current app NPS is 38, industry average 35-45. Right in the middle.
→ Diane's 6 is the drag — family features could be a real NPS lever.

What would move each person to a 10:
- Marcus: investment sync + reliable bank connections
- Diane: shared household accounts
- Keisha: one-tap AI recategorization + learning
- Tom: investment tracking + data export
- Preethi: reliable bank sync + maybe mobile app

---

## Key Themes Summary

### Critical (mentioned by 4-5 users):
1. **Bank sync reliability** — all 5 users, silent disconnects are dangerous, erodes trust
2. **AI miscategorization** — 4/5 users, Amazon and Venmo worst offenders, trust erosion if not fixed
3. **Investment account support** — 3/5 users, net worth is "wrong" without it

### High Priority (2-3 users):
4. **Shared household budgets / family sharing** — Diane most vocal, but others see it for couples
5. **Mobile app improvements** — Marcus using Copilot in parallel because mobile UX is better
6. **One-tap recategorization** — Keisha and Marcus want frictionless correction flow

### Nice to Have:
7. Venmo/PayPal sync (Marcus)
8. Debt payoff calculator (Keisha)
9. Custom categories (Diane, Keisha)
10. Data export CSV (Tom)
11. Bill negotiation tool (Preethi — but this got the biggest group reaction, worth noting)

---

## Customer Success Team Input

After users left, CS reps shared:

- "Bank sync is our #1 support ticket category by volume. Roughly 35% of all tickets."
- "The Amazon miscategorization issue — we get this 3-4 times per week. Users are frustrated that it keeps happening."
- "We've seen 4 churns this quarter where the user mentioned 'my partner doesn't use it.' Family sharing would have kept those."
- "The Mint refugees are our most engaged users — they're motivated, they want to make it work. Don't lose them."

---

## Action Items

- me: share feedback summary with Priya + David (tag bank sync + AI accuracy as P1)
- me: add "bill negotiation tool" concept to innovation backlog (surprising amount of interest)
- jordan: create family/household feature brief (demand is clearly there, needs scoping)
- CS team: start tagging support tickets by feature area — need better data on bank sync vs AI vs other
- me: check Plaid's Venmo/PayPal support status (has it improved?)
- me: pull NPS data segmented by "has investment accounts manually added" vs not
- CS team: follow up with Diane P. specifically re: family sharing beta interest

---

## My Takeaways

The bank sync issue is worse than I thought. Preethi's near-overdraft story should be in the next product review. When a finance app makes someone less financially safe, that's a serious trust problem.

The AI categorization feedback confirms what we discussed in Monday's product sync. Users aren't giving up on the AI — they want it to be better and they'll help train it (Diane's "ask me once" suggestion is exactly the feedback loop David wants to build).

Investment tracking is a clear gap, especially for users with significant assets. Tom is right that the net worth number is incomplete without it. That's a feature that could move our NPS from 38 to 45+ for the right segment.

Bill negotiation tool is a sleeper idea. Preethi mentioned it casually but the room lit up. Worth a quick market research pass — companies like Rocket Money do this. Is it in our lane?

Bottom line: fix the foundation (sync, accuracy) before adding features. These users are forgiving because they like the core product. But "forgiving" has a shelf life.
