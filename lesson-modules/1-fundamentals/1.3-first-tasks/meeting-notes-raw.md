MONDAY 3/10 - PACKED DAY

=== Meeting 1: Product sync w/ Maya & Kai (9am) ===

attendees: maya (ceo), kai (design), me
context: weekly product sync

- talked about Q1 priorities
- Maya wants to push bank sync reliability up in priority
  - "users are calling it out in every support ticket"
  - plaid disconnects happening too often (esp chase accounts)
  - might be killing retention?

kai showed initial work on mobile improvements
- looks promising! cleaner transaction list
- uses our existing teal/gold color system
- question: what about accessibility for colorblind users on budget bars?
- kai will investigate

BANK SYNC discussion:
maya: "we need to hit 95% uptime on bank connections by end of Q1"
- current: ~82% (not great, plaid webhooks unreliable)
- reconnect rate: 28% of users have to manually reconnect per month
- competitor copilot: claims 99% uptime

ideas discussed:
- better error handling + auto-retry logic
- proactive reconnect prompts before token expires
- fallback to manual CSV import? (kai says clunky but better than nothing)
- real-time status page for bank connections

ACTION ITEMS:
- me: audit plaid webhook failure logs (last 60 days)
- kai: wireframes for reconnect flow + error states
- maya: loop in David on infra capacity for retry queue

also talked about mobile app progress
- on track for Q2 launch (good news!)
- sam (mobile PM) demoing beta next week

---

=== Meeting 2: Stakeholder check-in w/ David (CTO) (11:30am) ===

david (cto) wants to discuss AI categorization accuracy

CONTEXT:
AI categorization is underperforming
- current accuracy: 87% (need 95%)
- amazon purchases: nightmare (could be anything - groceries, electronics, clothes)
- venmo/paypal: almost always wrong ("friends transfer" vs rent vs reimbursement)
- users manually recategorizing 4-5 transactions/week on avg
- trust in AI is eroding (bad!)

David's perspective:
"our ML model needs retraining but we have a tech debt problem"
- training data labels are inconsistent
- merchant name normalization is a mess
- unclear who owns the model in production

discussed:
1. retraining pipeline
   - david: "we need clean labeled data first"
   - me: use manual corrections as training signal (users are already doing the work!)

2. merchant enrichment
   - normalize merchant names (AMZN MKTP US → Amazon)
   - enrich with category metadata
   - david: "plaid already does some of this, we're duplicating"

3. contextual signals
   - transaction amount + time + merchant = better guess
   - david: "we should weight user history heavily"
   - me: "what about new users? cold start problem"

4. user feedback loop
   - make recategorization super easy (one tap)
   - feed corrections back to model faster
   - david: "right now there's a 2-week lag on retraining"

TECHNICAL CONSIDERATIONS:
- ML pipeline not currently automated (manual retraining)
- need to move to automated weekly retraining
- david estimates 3 sprint effort for pipeline overhaul
- need data team buy-in (they own the labels)

CONCERNS from David:
- team is stretched (bank sync fixes taking bandwidth)
- accuracy improvement might take Q1 + Q2
- suggests phased approach: quick wins first, then model overhaul

my take: need both tracks - fix obvious errors fast, long-term model work in parallel
priya might have thoughts on how to sequence - need to discuss priorities

ACTION:
- me: pull data on most miscategorized merchants (top 20)
- me: draft spec for user feedback loop improvements
- me: talk to CS - how many tickets are recategorization complaints?
- david: technical spec for automated retraining pipeline

random note: david mentioned eng team satisfaction survey results
- tooling satisfaction: 6.9/10 (down from 7.4 last quarter)
- "too many manual processes" came up 5 times in comments
- performance on transaction loading mentioned by 3 people

---

=== Meeting 3: Planning session - Investment Tracking (2pm) ===

brainstorming session for investment tracking feature
attendees: me, kai (design), riley (PM), sam (eng lead)

BACKGROUND:
users asking for investment account support for months
current state:
1. user connects bank accounts
2. sees checking/savings/credit
3. ... but where's my 401k? brokerage? crypto?
4. manually adds net worth estimate (annoying!)
5. net worth number is incomplete/wrong
6. loses trust in product

GOAL: complete financial picture in one place

INVESTMENT TRACKING CONCEPT:
connect brokerage + investment accounts
- plaid supports: fidelity, schwab, vanguard, robinhood, coinbase (beta)
- show: holdings, value, allocation, gain/loss
- roll up into net worth tracker (big feature!)
- portfolio view: asset allocation chart, performance over time

discussion:

riley: "we should nail brokerage first, skip crypto for now"
- crypto = regulatory gray area
- brokerage = cleaner data, better plaid support
- "get the foundation right"

me: "how does this fit net worth tracker?"
- kai: "user has this big beautiful net worth number at top of dashboard"
- investments would finally make that number accurate
- "right now net worth is mostly debt - looks terrible for users"

sam: "portfolio view tech?"
- plaid investment endpoints are newer, less stable
- need to handle rate limits (plaid charges per call)
- real-time prices vs daily snapshot? (real-time = expensive)

kai: "UI considerations"
- pie chart for allocation (ETF vs stocks vs bonds vs cash)
- performance chart (1M / 3M / 1Y / All)
- individual holdings table with gain/loss coloring (green/red)
- mobile: condensed card view, expand for details

CONCERNS:
sam: "investment data is complex"
- lots of edge cases (options, fractional shares, dividend reinvestment)
- reconciling across multiple brokerages
- tax implications info? (probably v2)

me: "data freshness?"
- users expect investment values to update daily
- real-time too expensive + plaid doesn't guarantee it
- daily refresh at market close = reasonable starting point

COMPETITIVE RESEARCH NOTES:
- Personal Capital (now Empower) has investment tracking (it's their core!)
  - very detailed, maybe too complex
  - portfolio analyzer is powerful
- Mint had investments (RIP mint)
- YNAB: no investments (feature gap, good for us!)
- Copilot: recently added investments (competitor threat - timeline?)

OPEN QUESTIONS:
1. manual investment entry for accounts plaid can't reach (401k with obscure provider)?
2. do we show individual stock picks or just totals?
3. performance benchmarking (vs S&P 500)?
4. tax lot tracking - phase 1 or skip?

sam's technical estimate: 4-5 sprints
- plaid investment endpoint integration
- data model for holdings/accounts
- portfolio view UI (web + mobile)
- net worth integration
- daily refresh job

riley: "can we do a lightweight v1? just account balances, no holdings detail?"
- faster to ship (2 sprints)
- validates demand before full build
- me: "might feel underwhelming... but ships sooner"

DECISION: need to prioritize with Priya
- is investment tracking Q2 or Q3?
- ties into net worth tracker OKR
- but bank sync reliability might need resources first

ACTION ITEMS:
- me: write one-pager on investment tracking (scope, phasing, risks)
- me: pull data on how many users have manually added investment accounts
- kai: quick mockup of portfolio overview + net worth integration
- sam: more detailed estimate for v1 (balance only) vs v2 (full holdings)
- riley: check plaid investment API coverage (which brokerages supported?)

---

RANDOM NOTES / PARKING LOT:

- priya wants to discuss shared household budgets next week (big feature req)
- CS escalated power user asking for full data export to CSV/Sheets
  (we have basic export but they want raw transaction data + categories)
- david mentioned performance issue on transaction search > 90 days (looking into it)
- marketing wants to do a "new year new budget" campaign (timing???)
- someone on slack mentioned competitor "Monarch Money" growing fast - need to check out

personal reminder: need to review sam's mobile PRD by wednesday

UPCOMING THIS WEEK:
- tuesday: customer interview (debt payoff user, referred by CS)
- wednesday: design review (dashboard redesign mockups)
- thursday: sprint planning
- friday: all-hands (maya presenting Q1 OKRs)

data to pull:
- bank sync failure breakdown by institution (which banks are worst?)
- AI miscategorization rate by merchant type
- feature request frequency (investment tracking vs shared budgets vs mobile)
- NPS breakdown by cohort (new vs 6mo+ users)

---

PRIORITIES EMERGING:
1. bank sync reliability (committed, user retention risk)
2. AI categorization accuracy (OKR-critical, trust issue)
3. mobile app (Q2 launch, high demand)
   - better UX, faster load times
4. investment tracking (high request volume, but complex)
5. shared household budgets (couples/families = big market segment)

need to get clarity from priya on what's actually Q1 vs Q2 vs Q3

---

FOLLOW-UPS NEEDED:
✓ plaid webhook failure audit (me)
- spec for AI feedback loop improvements (me)
- one-pager on investment tracking (me)
- talk to CS re: miscategorization & bank sync tickets (me)
- review mobile PRD (me)
- reconnect flow wireframes (kai)
- dashboard redesign mockups (kai)
- retraining pipeline spec (david)
- investment tracking estimate (sam)

busy week ahead!
