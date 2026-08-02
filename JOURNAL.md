## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/101

**Issue title:** Add a "Copy link" button to share a public review summary

**Tier:** [ ] Tier 1  [x] Tier 2  [ ] Tier 3

**Problem summary:**

The issue asks to implement a system where users are able to share a read-only view of their review summary. The link should be accessible without the need to login and expires after 30 days. Even though `frontend/src/services/shareService.ts ` does not exist, there are exisiting APIs I can use to help build the frontend-backend connection to populate the page. A share button exists, but the link generation, public view and expiration needs to be implemented. A successful fix would have the previously stated features implemented.

**Branch name:** feat/101-review-copy-link

**Setup confirmation:** [x] App runs locally at localhost:5173

**Cohort ledger:** [x] Issue added to cohort ledger

** Is this Issue Right for Me?*

*Part 1*: The issue asks to implement a feature where the user can share the results of pathreview. I need to implement methods to handle link generation, expiration, and privacy. Additionally, I need to ensure there are API endpoints exist for the data provided.

The relevant files are listed by the issue:
*`frontend/src/pages/ReviewPage.tsx`
*`frontend/src/services/shareService.ts`
*`api/routes/reviews.py`

However, `frontend/src/services/shareService.ts` does not exist, so I would need to look into `frontend/src/services/api.ts`.

The "done" should allow the user to physically generate a link and open it to see a summary of their review from the reviews API route. On the summary page, the page should include how much time left does the page have until expiration (or when the page expires). Additionally, the link should be accessible by any user.

*Part 2*: I chose a Tier 2 issue since I've worked on open-source style projects in the past, especially as a technical lead for a project at my university. I've worked on a few development teams also! I'm also fairly familiar with front-end development (especially in React) and would like to expand my knowledge through working thorugh this issue.

*Part 3* The relevant code is found in the relevant files above. The button is found in `frontend/src/pages/ReviewPage.tsx` I will be using the `get_review_endpoint` endpoint found in `api/routes/reviews.py`.

I would need to write a new test case to check for the 30-day deletion system, and unique link generation, which would be found in `tests/unit/test_review_service.py` or `frontend/src/test/setup.ts`.

*Part 4* The issue provides an estimate of 5-8 hours for completing this issue, which should be ample time for Weeks 8-9. The only major thing I'm doing is working on a game jam and contributing towards other projects. Only 1 student within my section is already working on the issue. There are no open blockers or dependencies for issue #101 also.

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** https://github.com/anthonyle1/pathreview/commit/eb3dd4fc8da32c4244912066f22102dcf492f4ec

**Reproduction summary:**
I reproduced the issue by following the user workflow to "share" the link they provided. The link is able to be shared, but when opening the link to an incognito tab that is signed out, the user is prompted to log-in instead of viewing the shared review page.


**PLAN.md link:** https://github.com/anthonyle1/pathreview/blob/feat/101-review-copy-link/PLAN.md

**Walkthrough video (recommended):** [link to your Loom video, ≤2 min — recommended, not graded]

**Blockers or open questions:**
How to handle link regeneration + privacy? 

## Week 9 — Solution building & PR submission

### Check-in 1 (mid-week)

**Current progress:**
I implemented the entire changes defined in PLAN.md, making new API endpoints and editing the database schema, creating a new share page accessible by any user, and implemented tests to ensure link expiration.

**Next steps:**
I'm working on doing a PR review through Slack and getting ready for submission!

**Blockers:**
[Anything slowing you down? Or leave blank.]

---

### Check-in 2 (end of week)

**PR link:** [link to your submitted pull request]

**Branch:** [the branch name you worked on, e.g. `fix/123-short-description`]

**What you built:**
[1–3 sentences summarizing what your fix does and how it works]

**Tests added or updated:**
[Which test files did you touch? What do they cover?]

**Self-review confirmation:** [ ] make check passes  [ ] make test-unit passes

**Draft PR feedback received from:** [name or Slack handle, or "none"]