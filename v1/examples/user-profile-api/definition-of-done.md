# Definition of Done — User Profile API Example

A change is considered complete only when all applicable conditions
below are satisfied.

## Specification

- [ ] Requirements are explicit and testable.
- [ ] Acceptance criteria are defined.
- [ ] Requirement changes are reflected in the traceability matrix.
- [ ] No unresolved requirement ambiguity remains.

## Architecture

- [ ] The implementation follows the documented architectural
  boundaries.
- [ ] Authentication and authorization responsibilities are preserved.
- [ ] Data ownership rules are enforced server-side.
- [ ] Material architectural changes are documented through an ADR.

## Implementation

- [ ] All related tasks are completed.
- [ ] Input validation is enforced.
- [ ] Authorization is enforced.
- [ ] Protected fields cannot be modified through unsupported paths.
- [ ] Error handling follows the defined contract.
- [ ] Observability requirements are implemented without exposing
  sensitive data.

## Verification

- [ ] Unit tests pass.
- [ ] Integration tests pass.
- [ ] API tests pass.
- [ ] Negative tests pass.
- [ ] Security tests pass.
- [ ] All applicable acceptance criteria are verified.
- [ ] Test evidence is available and traceable.

## Security

- [ ] Authentication controls are verified.
- [ ] Ownership authorization is verified.
- [ ] Sensitive data exposure risks are addressed.
- [ ] Input validation controls are verified.
- [ ] Error responses do not expose secrets or unnecessary
  implementation details.
- [ ] Threat-model controls are verified.

## Quality

- [ ] No known critical or high-severity defect remains unresolved.
- [ ] API compatibility has been verified.
- [ ] Documentation reflects the implemented behavior.
- [ ] Traceability is complete from requirement to verification.

## Release

- [ ] Release checklist is complete.
- [ ] Exceptions are explicitly documented.
- [ ] Any accepted residual risk has an identified owner and
  follow-up action.

## Final Principle

A task is not done merely because the code works locally.

It is done when the intended behavior is specified, implemented,
verified, secured, traceable, and ready to be maintained.
