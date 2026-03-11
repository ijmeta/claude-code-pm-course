# 4.2 Plan

Before we build, we need to get clear on what we're building.

This is called "requirements" - basically a description of how your budget tracker should work and look.

STOP: Have you ever given someone vague instructions and gotten something totally different than you expected?

USER: Yes / Definitely

---

That's what happens when you skip requirements. The more detail we figure out now, the better I can build what you actually want.

I'm going to interview you about your budget tracker. We'll figure out the features, the categories, the style. Then I'll save it all to a file so we have a clear spec to build from.

STOP: Think of this like briefing a contractor before they start work. The clearer the brief, the better the result. Ready to start?

USER: Yes

---

I'm going to use a tool called AskUserQuestion - it gives you nice buttons to pick from instead of typing. You can ask me to use this anytime you want a cleaner way to make decisions. Just say "ask me" or "give me options."

Let's try it now.

ACTION: Use AskUserQuestion with two questions:
- Q1 Header: "Core features" / Question: "Which features do you want in your budget tracker?" / Options: "Just expenses (simple and focused)", "Income + expenses (Recommended)", "Income + expenses + savings goals", "Full suite: income, expenses, savings goals, and notes"
- Q2 Header: "Categories" / Question: "How many spending categories do you want?" / Options: "5 - Keep it simple (groceries, rent, transport, entertainment, other)", "8 - Good variety (Recommended)", "10+ - Full breakdown", "I'll define my own categories"

USER: [Selects options]

Great choices! Now let's pick your spending categories.

---

Remember: the tracker groups transactions by CATEGORY so you can see where your money goes. So we need to decide which categories make sense for you.

Here are some category ideas. Pick the ones you want based on your earlier choice. Just type the numbers, like "1, 4, 7":

1. **Groceries** - Food and household essentials
2. **Rent / Mortgage** - Housing costs
3. **Transport** - Gas, public transit, rideshare
4. **Entertainment** - Streaming, dining out, events
5. **Utilities** - Electricity, water, internet, phone
6. **Healthcare** - Medical, pharmacy, insurance
7. **Shopping** - Clothing, electronics, general retail
8. **Education** - Courses, books, subscriptions
9. **Travel** - Flights, hotels, holidays
10. **Savings** - Transfers to savings accounts
11. **Income** - Salary, freelance, other income
12. **Other** - Anything that doesn't fit

STOP: Type the numbers you want (e.g., "1, 2, 3, 4, 5")

USER: [Types numbers]

ACTION: Note their selections for use in REQUIREMENTS.md

---

Perfect! Now we need to figure out the "logic."

Logic is the behind-the-scenes rules for how something works. If users do X, what happens? If they click this, what do they see? It's the "if this, then that" of your product.

Every app, website, or tool has logic. When you're planning something, you always need to think through how it should actually behave. I can help you brainstorm options.

Here's how this budget tracker will work: you add transactions with an amount, category, and date. The app tallies up spending by category and shows you a monthly summary.

The question is: how do we show the summary? Two options:

**Option A: Monthly total + category list** - "November: $2,340 spent. Groceries: $420, Rent: $1,200, Entertainment: $180..."

**Option B: Monthly total + category chart** - Same numbers, but also a simple bar chart or pie chart so you can see it visually.

STOP: Which do you prefer - text list (A) or include a chart (B)?

USER: [Responds A or B]

ACTION: Note their choice for REQUIREMENTS.md

Great choice! So if someone adds a $50 grocery trip and a $120 electricity bill in November:

[If they chose A]: They see "November: $170 spent. Groceries: $50, Utilities: $120."

[If they chose B]: They see the same summary plus a chart showing the proportional breakdown by category.

The app always shows the current month by default, but lets you browse to past months too.

STOP: Make sense?

USER: Yes

---

Now for the fun part - how should it LOOK?

I'm going to generate a few different visual styles as preview pages and open them in your browser.

STOP: Ready to see some style options?

USER: Yes

ACTION: Generate 3-4 HTML style preview files with different aesthetics:
- Style 1: Clean/modern (white background, green accents, card-based layout)
- Style 2: Minimal/dark (dark background, high contrast numbers, sleek typography)
- Style 3: Friendly/colorful (soft colors, rounded cards, approachable feel)
- Style 4: Dashboard/professional (structured grid, data-forward, business-like)

Each preview should show a sample transaction list and a monthly summary card. Save them to the budget-tracker-app folder as style-preview-1.html, style-preview-2.html, etc.

ACTION: Open all preview files in the browser using bash open commands

Take a look at those previews in your browser. Each tab is a different style.

STOP: Which style do you like best? You can pick one, or tell me what to mix - like "I like the colors from #2 but the layout from #3"

USER: [Responds with preference]

ACTION: Note their style preference. If they want to mix elements, clarify what specifically they want combined.

---

One more visual question: do you want icons next to each category?

Like a little cart icon for Groceries, a house for Rent, a car for Transport.

Icons make the tracker feel more polished and visual, but we can also keep it text-only if you prefer a cleaner look.

STOP: Icons or no icons?

USER: [Responds]

ACTION: Note their choice for REQUIREMENTS.md

---

Last part - how do you want to add transactions?

There are two approaches:

**Option A: Simple form** - A form at the top of the page: Amount, Category (dropdown), Date, optional Note. Fill it in and click Add.

**Option B: Quick-add row** - A compact inline row at the top of the transaction list. Faster to use but less obvious.

STOP: Which feels better to you - full form (A) or quick-add inline (B)?

USER: [Responds]

ACTION: Note their choice for REQUIREMENTS.md. If they want both or aren't sure, go with Option A as the safer default.

---

Perfect! We've got everything we need. Let me save all of this to a requirements file.

ACTION: Create REQUIREMENTS.md in the budget-tracker-app folder with:
- Selected spending categories (with any income categories)
- Summary display style (text list or chart)
- Visual style description
- Icon decision
- Transaction entry style (full form or quick-add)
- Any additional notes from the conversation

Done! Open REQUIREMENTS.md and take a look. This is the spec I'll build from.

STOP: Does everything look right?

USER: Yes / [Corrections]

ACTION: Make any corrections if needed

---

**What you just learned:** How to define clear requirements before building - specifically for a data-driven app with categories and summaries.

**Where else this applies:**
- Briefing a designer or developer on any project
- Writing a product spec or PRD
- Planning any creative project - the clearer the vision, the better the result
- Working with AI tools - the more specific you are, the better the output

**Next up:** In 4.3, we actually BUILD this thing. You'll watch me create your budget tracker from scratch based on these requirements. This is where the magic happens.

STOP: Ready for 4.3? Say "let's build" or type /start-4-3

USER: Let's build

---

## Important Notes for Claude

- The AskUserQuestion tool should be used for the initial batched questions ONLY - after that, use regular conversation
- When generating style previews, make them actually visually distinct - don't just change colors slightly
- The REQUIREMENTS.md file is crucial - it's the spec for 4.3. Make sure it's complete and clear.
- If users want to mix styles, get specific about what elements from each
- Default to Option A (full form) for transaction entry if the user is unsure - it's more beginner-friendly
- If the user chose "income + expenses," make sure REQUIREMENTS.md reflects that income transactions should be tracked separately from expenses

## Success Criteria

- User has selected their spending categories
- User has chosen summary display style (text list vs chart)
- User has selected a visual style
- User has made a decision on icons
- User has chosen a transaction entry style
- REQUIREMENTS.md exists with all the above documented
- User is excited to build
