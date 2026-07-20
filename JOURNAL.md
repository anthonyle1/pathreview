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