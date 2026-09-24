# Behavior-Driven Development (BDD)

## 1. Purpose

Document how Behavior-Driven Development (BDD) is used as an engineering
practice within Ptilon.

BDD focuses on describing system behavior in a form that can be understood by
both technical and non-technical stakeholders.

---

## 2. Role in Ptilon

BDD complements requirements engineering and Specification-Driven Development
by expressing expected behavior through concrete examples.

A typical flow is:

Requirement → Example → Acceptance Criterion → Executable Specification →
Implementation → Verification

BDD is particularly useful when shared understanding of behavior is more
important than implementation detail.

---

## 3. Relationship with Ptilon

Ptilon's broader workflow is:

Specify → Clarify → Plan → Tasks → Implement → Converge

BDD primarily strengthens the specification and verification activities.

It should not replace the governing specification. Instead, behavioral
examples provide concrete evidence of how the requirement is expected to work.

---

## 4. Behavior-focused specification

BDD specifications should describe observable behavior.

A useful structure is:

```text
Feature: <feature name>

Scenario: <scenario name>

Given <initial context>
When <action or event>
Then <expected outcome>
```

Additional `Given`, `When`, or `Then` steps may be used when necessary.

The scenario should remain focused on behavior rather than implementation
details.

---

## 5. Given / When / Then

### Given

Defines the relevant initial context.

Examples include:

- authenticated user;
- existing record;
- configured environment;
- required dependency;
- initial system state.

### When

Defines the action or event being evaluated.

Examples include:

- submitting a request;
- updating a profile;
- triggering a workflow;
- invoking an API;
- attempting an unauthorized operation.

### Then

Defines the observable expected outcome.

Examples include:

- returned response;
- state change;
- error;
- notification;
- persisted data;
- security control being enforced.

---

## 6. Scenario quality

Good scenarios should be:

- understandable;
- focused;
- deterministic;
- observable;
- relevant to a requirement;
- independent where practical.

A scenario should demonstrate meaningful behavior rather than merely exercise
implementation statements.

---

## 7. Scenario coverage

BDD scenarios should cover the behaviors that matter to the feature.

Depending on context, this may include:

- primary flows;
- alternative flows;
- validation failures;
- boundary conditions;
- authorization failures;
- integration behavior;
- important quality requirements.

Not every possible input requires a separate scenario.

---

## 8. BDD and acceptance criteria

BDD scenarios can serve as concrete examples of acceptance criteria.

A useful relationship is:

Requirement → Acceptance Criterion → Scenario → Test Evidence

When scenarios are automated, the execution result provides verification
evidence.

When scenarios remain manual, they should still provide clear verification
conditions.

---

## 9. AI-assisted BDD

AI may assist with:

- identifying candidate scenarios;
- generating examples;
- identifying edge cases;
- translating requirements into Given/When/Then structures;
- reviewing scenario completeness;
- identifying ambiguous behavior.

AI-generated scenarios require human validation.

Particular attention should be given to:

- invented business rules;
- unsupported assumptions;
- duplicated scenarios;
- implementation-specific language;
- missing failure conditions.

---

## 10. BDD and implementation

BDD should not prescribe unnecessary implementation details.

For example, a scenario should generally describe:

```text
When the user submits an invalid email address
Then the request is rejected with a validation error
```

rather than specifying internal classes, database queries, or private methods.

This keeps the behavioral specification stable when implementation changes.

---

## 11. BDD and security

Security behavior can be expressed through behavioral scenarios.

Examples include:

```text
Given the user is authenticated
When the user requests another user's private profile
Then access is denied
```

Security scenarios should be connected to relevant security requirements and
threats when appropriate.

---

## 12. BDD and quality requirements

Behavioral scenarios can also verify selected quality requirements.

Examples include:

- response behavior under defined conditions;
- availability behavior;
- compatibility;
- error handling;
- accessibility;
- security behavior.

Quantitative quality requirements may require specialized verification beyond
BDD scenarios.

---

## 13. BDD and regression

Stable scenarios provide a useful regression suite.

When a defect is discovered, a regression scenario may be added when the
behavior is important enough to preserve.

The regression scenario should represent the expected behavior rather than the
implementation that happened to fix the defect.

---

## 14. BDD and change impact

When a requirement changes, review affected scenarios.

Impact analysis should consider:

- acceptance criteria;
- existing scenarios;
- automated tests;
- implementation;
- documentation;
- security behavior.

Outdated scenarios should be updated or removed rather than retained merely
to preserve historical test counts.

---

## 15. Ptilon principles

Ptilon applies the following BDD principles:

1. behavior should be expressed in terms understandable to relevant
   stakeholders;
2. scenarios should focus on observable outcomes;
3. scenarios should remain traceable to requirements;
4. implementation details should be minimized;
5. important failure and security behaviors should be represented;
6. AI-generated scenarios require validation;
7. scenarios should evolve with requirements.

---

## 16. References

- Dan North — Introducing BDD
- Ptilon Requirements Engineering:
  `references/standards/iso-29148.md`
- Ptilon Quality:
  `references/standards/iso-25010.md`
- Ptilon Methodology:
  `docs/methodology/README.md`
- Ptilon Workflow:
  `docs/workflow/README.md`

---

## 17. Status

This document defines BDD as a recommended engineering practice within Ptilon.

Projects should determine where behavior-driven scenarios provide sufficient
value and define the appropriate level of automation for their context.
