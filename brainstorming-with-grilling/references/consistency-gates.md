# Consistency Gates

Run these gates before presenting the written spec as ready for user review.

## Gate 1: Placeholder Scan

Fail if the spec contains unresolved placeholders:

- TBD
- TODO
- To be decided
- Appropriate
- Reasonable
- Fast
- Simple
- Robust
- Intuitive
- User-friendly
- Etc.

These words may appear only if they are explicitly defined in measurable or observable terms.

## Gate 2: Term Consistency

Every important term must have one meaning.

Fail if:

- The same term means different things in different sections.
- Different terms refer to the same concept without explanation.
- A role, state, or object appears in requirements but not in the glossary or actor table.

## Gate 3: Goal Coverage

Every goal must be supported by at least one requirement or acceptance criterion.

Fail if:

- A goal is aspirational but unimplemented.
- A requirement does not map to any goal.
- A non-goal is contradicted by a requirement.

## Gate 4: Requirement Completeness

Every functional requirement must define:

- Trigger
- Preconditions
- Observable behavior
- Outcome
- Acceptance criterion

Fail incomplete requirements instead of filling gaps with assumptions.

## Gate 5: Conflict Scan

Look for two requirements that demand different behavior under the same condition.

Common conflicts:

- Speed vs accuracy
- Automation vs user control
- Privacy vs analytics
- Backward compatibility vs simplified data model
- Admin override vs auditability
- Strict validation vs forgiving import

When a conflict exists, ask the user which priority wins.

## Gate 6: Boundary Coverage

Check important edge cases:

- Empty input
- Duplicate input
- Invalid input
- Missing permissions
- Partial success
- Cancellation
- Retry
- Timeout
- Offline or unavailable dependency
- Concurrent edits
- Existing data migration
- Irreversible action

Not every case needs a feature, but every relevant case needs an explicit decision.

## Gate 7: Acceptance Coverage

Every requirement must be verifiable.

Acceptable proof types:

- Automated test
- Manual review step
- UI inspection
- Log or audit record
- API response
- Data state check
- Performance measurement

Fail if acceptance says only "works correctly" or "looks good."

## Gate 8: Scope Discipline

Deferred work must appear in non-goals, future work, or blocking open questions.

Fail if:

- Deferred behavior is implied by a goal.
- A phrase like "later" hides a required decision.
- The spec relies on implementation to decide product behavior.

## Gate 9: Implementation Readiness

The spec is ready for implementation planning only if:

- All previous gates pass.
- The ambiguity ledger has no undecided blocking rows.
- The user explicitly approves the written spec.

If any gate fails, return to the workflow and ask the next single question needed to fix it.
