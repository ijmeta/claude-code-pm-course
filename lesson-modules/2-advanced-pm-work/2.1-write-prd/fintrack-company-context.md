# FinTrack Company Context

## Company Overview

**FinTrack** is a fast-growing personal finance SaaS that gives individuals and households a complete, real-time view of their financial life. Think Monarch Money meets YNAB, but built for the era of AI-powered insights and automatic bank sync.

**Tagline:** "See your full financial picture, finally."

**Founded:** 2020
**Headquarters:** Austin, TX
**Employees:** 45 people (12 product/eng, 8 sales/marketing, 25 customer success/ops)
**Subscribers:** ~180,000 active paying subscribers
**Funding:** Series B ($18M raised)
**Pricing:** $9.99/month or $79/year

## Product

FinTrack is a personal finance and budgeting platform with seven core features:

1. **Bank Sync (Plaid)** — Automatically connect checking, savings, credit cards, loans, and investment accounts. Transactions import daily with no manual entry required.
2. **AI Spending Categorization** — Machine learning categorizes every transaction automatically (currently 88% accurate, target 95%+). Users can correct mistakes and the model learns.
3. **Budget Goals** — Set monthly spending targets by category (groceries, dining, entertainment, etc.) and get real-time progress tracking throughout the month.
4. **Net Worth Tracker** — Assets minus liabilities, updated daily as accounts sync. Users see their full financial picture at a glance.
5. **Bill Calendar** — Upcoming recurring bills and subscriptions surfaced in a calendar view so nothing is missed or forgotten.
6. **Credit Score Monitoring** — Free credit score updates with alerts when the score changes and explanations of what drove the change.
7. **Savings Rate Dashboard** — Shows what percentage of income is being saved each month, with historical trends and comparisons to personal goals.

**In active development:** Investment Tracking — portfolio value, allocation, and performance across brokerage and retirement accounts.

**Key differentiator:** FinTrack is the only app that combines bank sync, AI categorization, net worth, credit monitoring, and savings rate in a single clean interface — without the ad-driven data monetization model that killed Mint's trust with users.

## Target Customers

**Primary:** Individuals aged 25–45 who earn enough to save but feel like they have no real visibility into where their money goes. They are motivated to improve their finances but frustrated by manual tracking tools.

**Secondary:** Couples and households managing shared finances. They want one view of joint and individual accounts without the awkward "who has access to what" problem.

## Personas

**Jordan — Young Professional Saving for a Home**
- 29, software engineer, renting in Austin
- Income: $115k/year, but only saving ~8% without knowing it
- Cares about: Understanding spending patterns, maximizing savings rate, building a down payment fund
- Pain points: Transactions miscategorized everywhere, no idea where "the rest" of the money goes, scared to look at credit score
- Quote: "I make decent money but I have no idea why I'm not saving more."
- FinTrack value: Sees complete picture for first time, AI categorization works without manual effort, savings rate dashboard motivates behavior change

**The Hendersons — Family Budgeting Together**
- Married couple, two kids, one full-time earner ($140k) plus one part-time ($38k)
- Cares about: Shared budget visibility, grocery and childcare spending, saving for college, avoiding bill surprises
- Pain points: Each spouse tracks spending separately, no joint view, one partner doesn't know the budget limits until they overspend
- Quote: "We need one place that shows both of us what we're spending."
- FinTrack value: Shared Household Budgets feature (in development), joint account sync, bill calendar prevents missed payments

**Alex — Debt Payoff Mode**
- 34, marketing manager, $22k in combined credit card and student loan debt
- Cares about: Seeing total debt clearly, tracking payoff progress, staying on budget to accelerate payoff
- Pain points: Debt spread across four accounts and two apps, interest calculations unclear, doesn't know when they will actually be debt-free
- Quote: "I know I have debt but I don't know when I'll actually be free."
- FinTrack value: Net worth tracker shows full debt picture, bank sync keeps all accounts current, budget goals enforce the discipline needed to pay down debt faster

## Market Position

**Competitors:**
- **YNAB (You Need a Budget)** — Strongest budgeting methodology, loyal fan base, but expensive ($99/yr), requires manual transaction entry, steep learning curve. No investment tracking or credit monitoring.
- **Monarch Money** — Closest direct competitor. Clean UI, growing fast after Mint shut down. Strong on budgeting, weaker on investment tracking. Slightly higher price ($99/yr). FinTrack's UX and AI categorization are advantages.
- **Copilot** — Apple-only, premium feel, strong investment tracking. Disadvantage: iOS/Mac only, no Android or web, $13/mo price point higher than FinTrack.
- **Credit Karma** — Free, but ad-driven, primarily a credit product. No real budgeting. Users see it as a credit score app, not a budgeting tool.
- **Empower (formerly Personal Capital)** — Strongest investment tracking in the space, free. Disadvantage: sales-driven (pushes wealth management services), budgeting features are weak.

**FinTrack's edge:** The only tool that combines serious budgeting (YNAB-like goals), modern UX (Monarch-like design), AI automation (no manual categorization), credit monitoring, and investment tracking in one platform — at the most competitive price in the category.

**Market opportunity:** Mint shut down in January 2024, displacing an estimated 3.6 million users overnight. Many are still searching for a replacement. Monarch has captured a large share, but FinTrack is positioned to win users who want more AI automation and a lower price point.

## Current Priorities

**Q1 2025 Goals:**
1. **Grow to 250,000 active subscribers** (from ~180k, targeting Mint refugees and Monarch switchers)
2. **Launch investment tracking in public beta** (currently in alpha with 500 users)
3. **Improve bank sync reliability from 97.8% to 99.5%** (top churn driver is broken sync connections)
4. **Reduce monthly churn from 4.2% to 3.5%** (retention improvement has higher ROI than acquisition at current scale)

**Strategic Initiatives:**
- **Bank Sync Reliability** — Every dropped Plaid connection is a churn risk. Plaid re-auth redesign is in progress.
- **AI Categorization Accuracy** — At 88%, wrong categories erode trust. Target 95%+ through improved ML model and user correction feedback loops.
- **Mobile Experience** — 68% of sessions happen on mobile. App lags web by one release cycle. Closing the gap is a top retention lever.
- **Shared Household Budgets** — Top feature request. Couples represent 35% of the user base and churn 20% less when both partners are active. Building Q1.

## Team and Culture

**Leadership:**
- **Maya Rodriguez** — CEO (former fintech growth operator, built FinTrack from founding)
- **David Park** — CTO (ex-Stripe engineer, deep infrastructure expertise)
- **Priya Patel** — Head of Product (previously at Intuit on the Mint team — knows this space deeply, and knows what Mint got wrong)

**Product Team:**
- 3 Product Managers (you are the PM for core budgeting and activation)
- 6 Engineers (split into two squads: Core Platform + Growth/Onboarding)
- 2 Designers
- 1 Data Analyst

**Culture:**
- Remote-first with quarterly Austin offsites
- Ship small, ship often (2-week sprints)
- Data-informed: every decision needs a metric and a hypothesis
- Customer-obsessed: PMs do 4 hours/week of customer calls minimum
- Financial privacy is core to the brand — we do not sell user data, ever

## Customer Insights

**What customers love:**
- "Finally, one place where I can see everything."
- "The AI categorization is shockingly good — I barely have to touch anything."
- "I didn't know my net worth until FinTrack. That number motivated me more than anything."

**What customers want:**
- Better investment tracking (top request, in development)
- Shared household budgets for couples (second most requested)
- More reliable bank sync (broken connections are the top frustration)
- Android app improvements (feels behind iOS)

**Why users churn:**
- 41% cite bank sync breaking and not reconnecting easily
- 22% say they "just stopped using it" (engagement problem, not product problem)
- 18% say they switched to a competitor for investment tracking
- 12% say price was a factor (usually comparing to free Credit Karma or Empower)

**Recent feedback:**
- NPS: 51 (strong for fintech; Mint was at ~30 before shutdown)
- App Store rating: 4.6 stars (iOS), 4.3 stars (Android)
- Top support ticket category: "My bank disconnected and I can't reconnect it" — 38% of all tickets

## Business Context

**Revenue Model:**
- **Monthly:** $9.99/month (no free tier, 7-day trial)
- **Annual:** $79/year ($6.58/month effective, 34% discount — our best margin)
- ~60% of subscribers are on annual plans

**Key Metrics:**
- CAC: ~$38 (primarily paid social and SEO)
- LTV: ~$190 (avg 19-month subscriber lifetime × $9.99/mo)
- LTV:CAC ratio: 5:1
- Monthly churn: 4.2% (target: 3.5%)
- Annual plan subscribers churn at 1.8%/year vs. 4.2%/month for monthly — annual plan conversion is a key lever

**Competitive Pressure:**
- Monarch Money growing aggressively post-Mint shutdown (well-funded, strong brand)
- Copilot expanding to web (was iOS-only advantage for FinTrack)
- YNAB holding price at $99/yr (pricing advantage for FinTrack)
- Free tools (Credit Karma, Empower) attract price-sensitive users we need to convert with value demonstration

## Why This Matters

You are working at a **critical inflection point**:

- **Mint's shutdown created a once-in-a-decade market opportunity.** Millions of users need a new home. The window to capture them is 12–18 months before they settle elsewhere.
- **Reliability is the moat.** In personal finance, trust is everything. A broken bank sync does not just annoy users — it makes them question whether FinTrack can be trusted with their financial life.
- **Retention is the business.** At 4.2% monthly churn, the average subscriber stays 19 months. Dropping to 3.5% extends that to 24 months — a 26% LTV increase with zero additional CAC.
- **Every feature needs to drive retention or acquisition.** We cannot afford to build things that do not move the core metrics.

Your PRDs need to balance:

- Customer needs (what they are asking for and what they actually need)
- Business goals (what drives revenue, retention, and competitive position)
- Technical feasibility (bank sync and Plaid complexity constrain some approaches)
- Strategic positioning (what keeps FinTrack differentiated from Monarch and YNAB)

---

**Remember:** You are not building features in a vacuum. Priya and Maya both came from companies where losing customer trust — even once — set the product back years. Every decision you make affects whether FinTrack becomes the default personal finance app for the next decade. Your PRDs need to tell the story of why THIS feature, why NOW, and why it matters to FinTrack's mission of helping people finally understand their financial lives.
