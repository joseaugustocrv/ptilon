# Prompt Version Metadata Template

## Prompt Metadata

- **Prompt ID:** `PRM-001`
- **Name:** `<prompt name>`
- **Version:** `<MAJOR.MINOR.PATCH>`
- **Status:** `Draft | Active | Deprecated | Retired`
- **Owner:** `<person/team>`
- **Created:** `<YYYY-MM-DD>`
- **Last reviewed:** `<YYYY-MM-DD>`

## Purpose

`<what this prompt is intended to accomplish>`

## Workflow

- **Ptilon workflow:** `<workflow>`
- **Phase:** `<phase>`
- **Related artifacts:** `<references>`

## Inputs

- `<input artifact>`
- `<input artifact>`

## Output Contract

`<expected output structure>`

## Constraints

- `<constraint>`
- `<constraint>`

## Evaluation

### Functional Evaluation

- [ ] Output follows the defined objective.
- [ ] Output follows the required format.
- [ ] Output remains traceable to authoritative inputs.
- [ ] Unsupported assumptions are identified.
- [ ] Missing information is surfaced.

### Engineering Evaluation

- [ ] Requirements are preserved.
- [ ] Security constraints are preserved.
- [ ] Quality constraints are preserved.
- [ ] Relevant edge cases are addressed.
- [ ] Human review remains explicit.

## Change History

| Version | Date | Change | Reason |
| --- | --- | --- | --- |
| `<version>` | `<date>` | `<change>` | `<reason>` |

## Review Record

- **Reviewed by:** `<person/team>`
- **Review date:** `<YYYY-MM-DD>`
- **Evaluation reference:** `<path or issue>`
- **Decision:** `Accepted | Changes Required | Retired`

## Usage Notes

`<specific guidance or limitations>`

## Principles

1. Prompt versions must be identifiable.
2. Material prompt changes must be reviewable.
3. Prompt behavior must be evaluated against representative scenarios.
4. Prompt changes must not silently alter authoritative project requirements.
5. Human accountability remains explicit.
