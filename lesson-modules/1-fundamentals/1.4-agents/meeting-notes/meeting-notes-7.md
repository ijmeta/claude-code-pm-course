PRODUCT SYNC - AI CATEGORIZATION ACCURACY REVIEW
Date: January 14, 2026
Attendees: Priya Sharma (Head of Product), Jordan Lee (PM, Core Experience), Sam Okafor (PM, Integrations), David Chen (CTO), ML Lead (Aisha Brennan)

DISCUSSION:
Aisha opened with the current state of AI categorization accuracy. The model is performing at 87% accuracy overall — meaning roughly 1 in 8 transactions is categorized incorrectly on first pass. This is up from 83% six months ago but well below our internal goal of 95%.

The accuracy gap breaks down by merchant type:
- Large national retailers (Walmart, Target, Costco): 94% accuracy — good
- Subscription services (Netflix, Spotify, etc.): 96% accuracy — very good
- Amazon: 71% accuracy — the single biggest drag on overall numbers
- Local/regional merchants: 79% accuracy — hard due to data sparsity
- "Venmo" and peer-to-peer payments: 61% accuracy — structurally difficult (no merchant context)

Jordan noted that Amazon's 71% accuracy is particularly damaging because it's such a high-volume merchant — Amazon transactions account for 11% of all transactions processed but disproportionately drive user complaints (ticket #2042 and many others). The problem is that Amazon sells everything — the AI can't reliably distinguish Amazon Fresh (Groceries) from Amazon Basics household items (Shopping) from a Kindle book (Entertainment) from an AWS charge (Business) based on merchant name alone.

Aisha proposed two approaches: (1) use purchase amount and user history as additional signals — e.g., an Amazon charge of $129.99 with no business history is probably not Business Expenses; (2) for known high-ambiguity merchants, prompt users to confirm category on first occurrence and use that as a personalized signal going forward.

David confirmed the infrastructure to support user-confirmed category signals already exists (it's what powers the "always categorize as" rule), the issue is the model isn't reading those rules correctly in all cases (bug FT-1892, in progress).

Team agreed on a combined approach: fix the rule-reading bug, add amount-based signals to the model, and design a lightweight category confirmation prompt for the top 10 ambiguous merchants.

ACTION ITEMS:
- Aisha to retrain model with purchase amount as additional feature by Jan 28
- Engineering to fix merchant rule persistence bug (FT-1892) by Jan 21 (already in sprint)
- Jordan to design category confirmation prompt UX for top-10 ambiguous merchants
- Sam to compile list of top 10 merchants by categorization error rate
- Priya to set categorization accuracy milestone: 91% by March 31, 95% by June 30

DECISION: Pursue combined fix: bug resolution + model improvement + UX confirmation prompt. Accuracy target: 91% by end of Q1, 95% by end of Q2.
