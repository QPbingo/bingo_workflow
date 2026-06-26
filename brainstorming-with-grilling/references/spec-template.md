# Requirements Spec Template

Use this template for the final written requirements spec.

## Requirement Statement Format

Write individual requirements in this form:

```text
REQ-001: [Short name]
When [trigger]
Given [preconditions]
The system/user must [observable behavior]
So that [intended outcome]
If [exception or boundary condition]
Then [explicit fallback, rejection, recovery, or failure behavior]
Acceptance: [testable or inspectable proof]
```

Rules:

- Use one behavior per requirement.
- Avoid vague words unless defined in measurable or observable terms.
- Use stable IDs so review comments can reference requirements.
- If a requirement has no acceptance criterion, it is not ready.

## Final Spec Structure

```markdown
# [Feature Or Project Name] Requirements Spec

## 1. Problem Statement
[Who has what problem, why it matters now, and what changes when solved.]

## 2. Goals
- G-001: [Outcome, not implementation]

## 3. Non-Goals
- NG-001: [Explicitly excluded behavior, phase, audience, platform, or metric]

## 4. Glossary
| Term | Definition | Notes |
|------|------------|-------|

## 5. Actors And Permissions
| Actor | Can Do | Cannot Do | Notes |
|-------|--------|-----------|-------|

## 6. Scenarios
### Scenario S-001: [Name]
- Trigger:
- Main path:
- Alternate paths:
- Failure paths:
- Expected result:

## 7. Functional Requirements
[Use REQ format.]

## 8. Non-Functional Requirements
[Performance, reliability, security, privacy, accessibility, compatibility, observability, maintainability.]

## 9. Failure And Boundary Behavior
| Case | Expected Behavior | User/System Feedback |
|------|-------------------|----------------------|

## 10. Ambiguity Ledger Decisions
| ID | Ambiguity | Decision | Rationale |
|----|-----------|----------|-----------|

## 11. Acceptance Criteria
| ID | Verifies | Method |
|----|----------|--------|

## 12. Open Questions Blocking Implementation
- [Question, owner, why it blocks]
```

## Blocking Rule

If section 12 is not empty, state clearly: "Implementation should not begin until these questions are resolved or excluded from scope."

## Optional Sections

Add only when useful:

- Dependencies
- Migration requirements
- Rollout plan
- Analytics or measurement
- Localization
- Compliance or audit requirements
- Out-of-scope future work
