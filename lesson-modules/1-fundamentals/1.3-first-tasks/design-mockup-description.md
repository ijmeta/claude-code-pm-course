DESIGN MOCKUP: FINTRACK DASHBOARD REDESIGN
Designer: Kai Chen
Version: v2 (For product review)
Date: March 12, 2025
Figma Link: [figma.com/fintrack-dashboard-redesign-v2]

═══════════════════════════════════════════════════════════════════

OVERVIEW:

Kai presented the dashboard redesign mockups for FinTrack. This is version 2 after incorporating feedback from user research and the product team. The redesign covers the main dashboard, budget section, and the addition of a dark mode toggle. The goal is to surface the most important financial data at a glance while making the app feel more premium and trustworthy.

═══════════════════════════════════════════════════════════════════

COLOR SYSTEM:

Primary Colors:
- Deep teal: #0D6B6B (primary brand, buttons, active states)
- Teal light: #1A9B9B (hover states, secondary actions)
- Gold accent: #F5A623 (highlights, budget warnings, call-to-action)

Background Colors (Light Mode):
- Primary background: #FAFAF9 (warm off-white, not stark white)
- Card background: #FFFFFF (pure white cards on warm background)
- Subtle surface: #F2F0ED (for secondary panels and sidebars)

Background Colors (Dark Mode - new this version):
- Primary background: #0F1A1A (very dark teal-black, not pure black)
- Card background: #1A2828 (slightly lighter for cards/panels)
- Elevated surface: #223333 (for hover and active states)

Text Colors:
- Primary text (light): #1A1A1A
- Primary text (dark mode): #EFF6F6 (off-white, reduces eye strain)
- Secondary text: #6B7B7B (for labels, metadata)
- Disabled: #A8B8B8

Status Colors:
- On track (green): #22C55E
- Warning (amber): #F59E0B (budget approaching limit)
- Over budget (red): #EF4444
- Positive trend: #10B981 (net worth up)

Borders:
- Subtle: #E8E4DF (light mode card separators)
- Dark mode subtle: #2A3D3D

═══════════════════════════════════════════════════════════════════

KEY SCREENS SHOWN:

1. MAIN DASHBOARD:

Spending Overview Card (top left, full width on mobile):
- "March Spending" header with current month-to-date total
- Large dollar amount in primary text (e.g., $2,847)
- vs. monthly budget below in secondary text (Budget: $3,200)
- Horizontal progress bar (teal fill, 89% full = amber warning state)
- "11% left" label on right of bar
- Sparkline showing daily spend this month (subtle, not noisy)

Net Worth Trend Chart (top right):
- Line chart, 6-month view (default)
- Y-axis: dollar values
- X-axis: month labels (Sep → Mar)
- Teal line for total net worth
- Dashed line showing 12-month projection
- Toggle buttons: 3M / 6M / 1Y / All
- Current value prominently shown: "$47,230" in large type
- Month-over-month delta: "+$1,840 (4.1%)" in green

Upcoming Bills Widget (below spending card):
- Section header: "Due in the next 7 days"
- List of upcoming bills (max 4 shown, "View all" link)
- Each row: merchant icon | bill name | amount | due date
  - Example: [Spotify icon] Spotify Premium · $9.99 · Due Mar 14
  - Example: [Rent icon] Rent · $1,850.00 · Due Mar 15 (bold, large amount)
  - Example: [Electric icon] ConEd · $87.42 · Due Mar 17
- Overdue bills shown in red with "OVERDUE" badge
- "All caught up!" empty state with checkmark illustration

Recent Transactions Feed (bottom, full width):
- Section header: "Recent Transactions"
- Each row: merchant logo | merchant name | AI category badge | amount | date
  - Example: [Whole Foods logo] Whole Foods Market [Food & Drink] -$67.43 Mar 10
  - Example: [Amazon logo] Amazon [Shopping] -$34.99 Mar 9
  - Example: [Payroll icon] Direct Deposit [Income] +$3,200.00 Mar 8
- AI category badges: pill-shaped, color-coded by category
  - Food & Drink: teal
  - Shopping: purple
  - Transportation: blue
  - Income: green
  - Utilities: gray
- Tap on transaction to expand: show full merchant name, map link, recategorize option
- "Possibly wrong category?" link under AI badges (feeds ML corrections)

2. BUDGET SECTION:

Budget Overview Header:
- Month selector (← March 2025 →)
- Total spent vs total budgeted (large, prominent)
- "3 categories over budget" warning if applicable

Category Progress Bars:
- Each category row: icon | category name | spent/budgeted | progress bar
- Food & Drink: $312 / $400 — bar at 78% (teal, healthy)
- Transportation: $89 / $200 — bar at 45% (teal, good)
- Shopping: $482 / $400 — bar at 120% OVER BUDGET (red bar, extends past 100% marker)
  - "Over by $82" label in red below
- Entertainment: $45 / $150 — bar at 30% (teal)
- Subscriptions: $67 / $80 — bar at 84% (amber, approaching limit)
- "Add Category" button at bottom

Bar states:
- < 70% = teal (#0D6B6B)
- 70-90% = amber (#F5A623) — "heads up" zone
- > 90% = amber with pulse animation
- > 100% = red (#EF4444), bar shown with overflow indicator

3. QUICK ACTIONS BAR:

Fixed strip at bottom of dashboard (mobile-first design):
- [+ Add Transaction] — opens quick-add modal, pre-fills today's date
- [Connect Account] — deep links to Plaid connection flow
- [View Insights] — navigates to AI spending insights page

Desktop: Quick Actions shown as button row below spending overview card
Mobile: Fixed bottom tab bar (persists across app navigation)

4. DARK MODE TOGGLE:

Located in top-right header, sun/moon icon
Three states: Light / Dark / Auto (follows system)
Kai suggests defaulting to Auto (respect OS setting)

Settings page toggle: more prominent, shows preview thumbnails of light/dark
Preference stored in user account (syncs across devices)
localStorage cache for instant load (no flash on page refresh)

5. TOP NAVIGATION:

- FinTrack wordmark + teal logo (left)
- Search bar (center desktop, icon-only mobile)
- Dark mode toggle, notifications bell, user avatar (right)
- Notifications badge: gold dot if unread (not a number — less anxiety-inducing)
- Mobile: hamburger menu collapses to bottom nav tabs

═══════════════════════════════════════════════════════════════════

KEY DESIGN DECISIONS:

Dark Mode Approach:
Kai chose a dark teal-black (#0F1A1A) rather than pure black to maintain brand identity. "Pure black loses our teal brand feel. This dark background is distinctly FinTrack, not generic."

Category Color Coding:
Budget bars use traffic light logic (teal → amber → red) rather than arbitrary category colors. "Users need to see health at a glance, not memorize what colors mean."

AI Badge Design:
Category badges are intentionally low-key (small pill, muted color). "We want users to trust AI categorization, not be constantly reminded they're talking to a machine. If it's wrong, the 'fix' link is right there."

Net Worth as Hero Metric:
Kai moved net worth to top-right prominence. "This is the number users care about most in the long run. Spending is daily, net worth is the journey. Both should be visible immediately."

Warm Neutrals vs Cold Gray:
Background uses warm off-white (#FAFAF9) instead of cool gray. "Finance apps feel cold and institutional. We want FinTrack to feel approachable, like good advice from a friend."

Transaction Feed vs Accounts View:
Homepage shows transactions not accounts. "Users check FinTrack to see 'what did I spend.' Account balances are secondary. We can show balances in a drill-down."

═══════════════════════════════════════════════════════════════════

COMPONENT DETAILS:

Spending Overview Card:
- Size: Full width (desktop: 60% of main area)
- Corner radius: 16px
- Shadow: 0 2px 12px rgba(0,0,0,0.06)
- Progress bar height: 10px, rounded ends
- Transition: bar fill animates on page load (0.6s ease-out)

Net Worth Chart:
- Library: Recharts (already in use)
- Dark mode: chart background inherits, line color stays teal
- Tooltip: white card with shadow, shows date + value
- Empty state (no accounts connected): illustrated placeholder + "Connect an account"

Budget Progress Bars:
- Height: 8px
- Over-budget visual: bar fills to 100% then shows red overflow arrow
- Animation: bars fill on page load (staggered, 0.1s delay each)
- Mobile: same design, slightly thinner (6px)

AI Category Badges:
- Font size: 11px, semibold
- Padding: 2px 8px
- Border radius: 100px (pill shape)
- Confidence threshold: badges only shown when AI confidence > 75%, otherwise "Uncategorized"

Quick Add Transaction Modal:
- Half-sheet on mobile (slides up from bottom)
- Fields: Amount, Merchant, Date (today default), Category
- Category picker: grid of icons, AI suggestion pre-selected
- Submit: "Add Transaction" teal button

═══════════════════════════════════════════════════════════════════

ACCESSIBILITY CONSIDERATIONS:

Contrast Ratios:
Kai verified all text meets WCAG AA standards. Primary text on light background: 14.2:1. Teal buttons with white text: 4.8:1 (passes AA). Gold on white: needs checking — Kai flagged this as borderline.

Color-Blind Considerations:
Budget bars don't rely on color alone. Each bar state also uses a text label ("On track" / "Approaching" / "Over"). For users with red-green color blindness, the over-budget bar uses a pattern fill in addition to red color.

Screen Reader Support:
Budget bars need aria-label="Food & Drink budget: 78% used, $312 of $400"
Transaction list needs semantic list markup
Chart needs text summary for screen readers ("Net worth increased from $45,390 in September to $47,230 in March")

Tap Target Sizes:
All interactive elements minimum 44x44px (Apple HIG / Google Material guidelines)
Quick action buttons: 48px height on mobile
Category rows in budget: 56px height (easy to tap)

Focus States:
- Keyboard outline: 2px solid #0D6B6B, 3px offset
- Visible on both light and dark mode

Dark Mode Eye Strain:
Off-white text (#EFF6F6) on dark teal background instead of pure white. "Pure white on very dark backgrounds causes halation for some users. Slightly warm white is easier on the eyes."

═══════════════════════════════════════════════════════════════════

RESPONSIVE BREAKPOINTS:

Mobile (< 768px):
- Single column layout
- Spending card full width
- Net worth chart collapses to summary card (no chart, just number + delta)
- Budget bars full width
- Quick actions as bottom tab bar (fixed)
- Transaction feed shows 5 rows, "Load more" button

Tablet (768px - 1024px):
- Two column layout: spending + net worth side by side
- Budget section below, 2 columns
- Quick actions as floating action button (bottom right)

Desktop (> 1024px):
- Three column layout: left sidebar nav | main content | right panel
- Right panel: upcoming bills + quick actions
- Full net worth chart with 6-month default view
- Budget section: 3-column grid of category bars

═══════════════════════════════════════════════════════════════════

CONCERNS / OPEN QUESTIONS FROM REVIEW:

1. CHART LIBRARY DARK MODE:
Issue: Recharts default tooltip and axis colors don't adapt to dark mode automatically
Kai's solution: Override chart theme with CSS variables
ACTION: Sam needs to test Recharts dark mode support - may need custom tooltip component

2. TRANSACTION LOGO FETCHING:
Issue: Merchant logos sourced from Clearbit — not all merchants have logos, some are low quality
Jordan: "Blank logo placeholder looks worse than just initials"
Suggestion: Fallback to merchant initial + generated color (like Notion avatars)
DECISION NEEDED: Kai to design fallback state

3. OVER-BUDGET ANIMATION:
Issue: Pulsing red bar might be anxiety-inducing for users already stressed about money
Kai: "Maybe just static red, no pulse?"
Me: "Or pulse only when > 150% over?"
DECISION NEEDED: Product and design to align on tone

4. MOBILE NET WORTH CHART:
Issue: Chart is collapsed to just a number on mobile — loses the "trend" story
Alternative: Show a small sparkline (7-day or 30-day) instead of full chart
Kai: "Sparkline works, I have a version of this in Figma"
DECISION NEEDED: Product to decide how important trend is on mobile

5. DARK MODE DEFAULT:
Options:
  a) Default to light mode (safe, familiar)
  b) Default to system setting (Auto — Kai recommends this)
  c) Default to dark mode
Kai suggests option B — most modern apps do this now
DECISION NEEDED: Product to confirm

6. AI BADGE CONFIDENCE THRESHOLD:
Currently hiding badge if AI confidence < 75%
Threshold may need tuning once we have real categorization data
Should "Uncategorized" show as a badge or just blank?
DECISION NEEDED: Product + data team input needed

═══════════════════════════════════════════════════════════════════

TECHNICAL IMPLEMENTATION NOTES:

Kai worked with Sam on implementation approach:

CSS Variables for theming:
Use CSS custom properties for all colors:
--color-background: #FAFAF9;
--color-surface: #FFFFFF;
--color-brand: #0D6B6B;
etc.
Dark mode switches root variables. Same approach as light mode, just different values.

Persistence:
User theme preference stored in user_settings table
Also cached in localStorage to prevent flash on page load

Animations:
Budget bars and net worth chart animate on mount (0.6s ease-out)
Dark mode toggle: 0.2s transition on all color properties
Kai: "No jarring flashes between modes"

System Preference Detection:
Use prefers-color-scheme media query for Auto mode
Respects OS-level dark mode and updates if user changes OS setting while app is open

Chart Theming:
Recharts will need theme-aware config object passed as prop
Sam to create useChartTheme hook that returns correct colors based on current mode

═══════════════════════════════════════════════════════════════════

ROLLOUT STRATEGY:

Kai suggests:
1. Internal dogfood: team tests for 1 week (catch obvious bugs)
2. Beta opt-in: 200 users from "power user" segment (people checking app daily)
3. Collect feedback via in-app survey (3 questions max, appears after 3 sessions)
4. Fix issues, iterate
5. Full release with in-app announcement banner

Marketing opportunity:
- Blog post: "Meet the new FinTrack dashboard"
- Screenshot for app store screenshots update
- Email to all users: "Your finances, redesigned"
- Social: before/after comparison image

═══════════════════════════════════════════════════════════════════

NEXT STEPS:

[ ] Product (me): Decisions on over-budget animation, mobile net worth, dark mode default
[ ] Engineering (Sam): Investigate Recharts dark mode support, chart theming approach
[ ] Design (Kai): Design merchant logo fallback state, sparkline option for mobile
[ ] Engineering (Sam): Estimate for dashboard redesign implementation
[ ] Product (me): Align with David on CSS variable approach vs. current theming

═══════════════════════════════════════════════════════════════════

PERSONAL NOTES:

This is a significant improvement over the current dashboard. Kai has clearly thought about the emotional side of personal finance — making the UI feel warm and supportive rather than cold and judgmental (which is a real risk with finance apps).

The budget progress bars are the standout feature. The traffic-light system plus "over budget" overflow visual is immediately understandable without any explanation.

Biggest open questions are around the chart on mobile (trend matters for net worth) and the over-budget animation tone. These are worth a quick user test before committing.

Overall: Strong yes to move forward. This will meaningfully improve daily engagement and user trust in the data.
