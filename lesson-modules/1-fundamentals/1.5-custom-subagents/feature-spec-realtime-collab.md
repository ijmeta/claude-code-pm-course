# Shared Household Budgets Feature Spec (Draft)

## Overview
Add shared budget functionality to FinTrack so couples and families can manage their finances together. Multiple users can view and edit the same budget, track joint and individual spending separately, and set household financial goals as a team.

## Goals
- Allow 2-6 household members to share a single FinTrack account and budget
- Support mixed account visibility: joint accounts shared, personal accounts optionally private
- Enable household members to set and track shared financial goals together
- Sync budget changes in real time so partners always see the same picture
- Works on web and mobile

## User Stories
- As one half of a couple, I want to invite my partner so we can manage our joint checking account together without emailing screenshots
- As a partner, I want to see my spouse's spending categories so we can spot where our household budget is going over
- As a parent, I want to add family members at view-only access so my teenager can see the grocery budget without editing bill payments
- As a household admin, I want to see who made what budget changes so I can understand why a category limit moved
- As a couple saving for a home, I want to set a shared savings goal and see both of our contributions toward it in one place

## Technical Approach
- Multi-user account model: one primary account owner invites additional members via email
- Permission levels: Owner (full access), Editor (view + edit budgets and goals), Viewer (read-only)
- Shared vs. private accounts: each linked bank account can be marked as shared (visible to all members) or personal (visible to owner only)
- Real-time sync between members using WebSockets so budget edits and new transactions propagate instantly
- Conflict resolution for simultaneous edits to the same budget category limit
- Audit log of who changed what and when, surfaced in a simple activity feed

## Success Metrics
- % of new signups who invite a partner within the first 30 days (target: 25%)
- Household account 90-day retention vs. solo account retention (target: household retains 15% better)
- % of invited partners who complete onboarding and connect at least one bank account (target: 60%)
- NPS delta between household users and solo users (target: +8 points)
- Support ticket volume related to "my partner can't see my budget" (target: near zero after launch)

## Timeline
- Phase 1: Invite system and permission model (3 weeks)
- Phase 2: Shared account visibility controls (2 weeks)
- Phase 3: Real-time sync between members (3 weeks)
- Phase 4: Shared goals and household activity feed (2 weeks)
- Phase 5: Mobile support and polish (2 weeks)

## Open Questions
- Should inviting a partner require both users to have paid subscriptions, or does one paid seat cover the household?
- How do we handle divorce or relationship changes — easy account separation is critical for trust
- Do we surface a "household net worth" view that combines both members' assets and liabilities?
- What happens to shared budget history if a member is removed?
- Should we allow more than two adults (e.g., roommates splitting expenses)?

## Resources Needed
- 2 backend engineers (multi-user account model, permissions, real-time sync)
- 2 frontend engineers (UI for sharing flows, household dashboard)
- 1 mobile engineer (iOS/Android parity)
- 1 designer (invitation UX, permission settings, shared goal UI)
- QA support for edge cases around data visibility and concurrent edits
