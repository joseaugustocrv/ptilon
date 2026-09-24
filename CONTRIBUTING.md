# Ptilon Contribution Guidelines

Thank you for contributing to Ptilon.

Ptilon is maintained as an engineering methodology, so contributions should
preserve clarity, traceability, consistency, and practical applicability.

## 1. Before Making a Change

Before creating a contribution:

- review the relevant existing documentation;
- identify the methodology area affected;
- check whether an existing artifact should be updated instead of creating
  a duplicate;
- preserve the relationship between requirements, workflow, quality,
  security, and governance.

## 2. Documentation Standards

Documentation should:

- use clear technical English;
- use consistent terminology;
- prefer normative language where requirements are intended;
- distinguish requirements, guidance, examples, and references;
- include links to authoritative sources where appropriate;
- avoid unnecessary duplication;
- remain implementation-agnostic unless a specific technology is part of
  the intended scope.

## 3. Methodology Changes

Changes to the methodology should explain:

- the problem being addressed;
- the proposed change;
- affected artifacts;
- traceability implications;
- quality or security implications;
- compatibility with the existing workflow.

Material changes should update the relevant templates, prompts, examples,
or reference documents when necessary.

## 4. Templates and Prompts

Templates and prompts are reusable methodology assets.

Changes should:

- preserve their intended structure;
- avoid hidden assumptions;
- make inputs and expected outputs explicit;
- maintain consistency with the methodology workflow;
- avoid duplicating mechanisms already provided by referenced tools.

## 5. Examples

Examples should demonstrate the methodology without introducing
unnecessary technology-specific complexity.

Example artifacts should remain mutually consistent across:

- specification;
- architecture;
- tasks;
- tests;
- security;
- traceability;
- release readiness.

## 6. Validation

Before submitting a contribution:

- run the repository documentation checks;
- verify Markdown formatting;
- verify links;
- review affected cross-references;
- check for terminology inconsistencies;
- confirm that referenced files exist;
- review the resulting documentation as a coherent workflow.

## 7. Pull Requests

A pull request should contain:

- a concise description of the change;
- the motivation or problem addressed;
- the main affected artifacts;
- relevant validation performed.

Keep unrelated changes out of the same pull request.

## 8. Review Criteria

Contributions are reviewed for:

- correctness;
- clarity;
- internal consistency;
- traceability;
- maintainability;
- security implications;
- practical applicability;
- alignment with Ptilon's scope.

## 9. Versioning

Changes that materially alter methodology behavior should be identifiable
in the repository history and, when appropriate, accompanied by updates
to affected documentation and examples.

## 10. Scope

Ptilon is intended to integrate disciplined software engineering practices
with AI-assisted development.

Contributions should strengthen that objective rather than turn the
repository into a collection of unrelated AI prompts, coding tricks, or
technology-specific recipes.
