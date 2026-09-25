# Example: User Profile API Clarification

## QST-001 — Profile Update Concurrency

**Origin:** Architecture review

**Question:** What should happen when two authenticated requests update the
same profile concurrently?

**Why it matters:** The persistence and API design depend on the required
concurrency behavior.

**Status:** Resolved

## CLR-001 — Concurrency Resolution

**Question:** QST-001

**Resolution:** The API uses optimistic concurrency. Updates must include the
current version of the profile; a stale version is rejected without partially
applying the update.

**Authority:** Approved by the product owner and technical owner.

## Impact Analysis

The resolution affects:

- specification error behavior;
- API contract;
- architecture persistence strategy;
- update task;
- acceptance criteria;
- concurrency tests.

## Required Updates

| Artifact | Action |
| --- | --- |
| specification.md | Add the concurrency rule and acceptance criterion |
| api-contract.md | Document version / conflict response |
| architecture.md | Document optimistic concurrency |
| tasks.md | Add implementation and test work |
| test-plan.md | Add concurrent update scenario |
| verification.md | Verify conflict behavior |

## Methodological Point

The question was discovered during Architecture, but it did not remain an
informal architectural assumption. Ptilon records the question, records the
authorized resolution, updates the authoritative specification, performs impact
analysis, and only then continues downstream work.
