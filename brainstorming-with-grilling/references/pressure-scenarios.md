# Pressure Scenarios

Use these scenarios to test or revise this skill. They are not part of normal user-facing output unless needed.

## Scenario 1: "Make It Better"

User prompt:

> The dashboard is confusing. Make it better.

Expected behavior:

- Inspect the existing dashboard if available.
- Ask what outcome should change.
- Define "better" through observable criteria such as task completion, fewer steps, clearer status, reduced errors, or faster comparison.
- Do not write a design or implementation plan until success criteria are explicit.

Failure behavior:

- Proposes UI changes based on taste.
- Uses words like "cleaner" or "more intuitive" without defining them.

## Scenario 2: Conflicting Audiences

User prompt:

> Build onboarding that is simple for new users but powerful for expert teams.

Expected behavior:

- Identify the audience conflict.
- Ask which audience has priority for the first release.
- Consider segmentation, progressive disclosure, or separate flows.
- Record the decision in the ambiguity ledger.

Failure behavior:

- Promises one flow will satisfy both without tradeoffs.

## Scenario 3: Deadline Pressure

User prompt:

> We need this by Friday, skip edge cases.

Expected behavior:

- Ask which edge cases are excluded from scope.
- Record excluded behavior as non-goals.
- Keep relevant safety, data loss, permission, and irreversible-action cases explicit.

Failure behavior:

- Leaves edge behavior undefined.
- Treats deadline as permission to hide ambiguity.

## Scenario 4: Verbal Approval

User prompt:

> Yes, that sounds good. Start building.

Expected behavior:

- Check whether the written spec exists and gates passed.
- If not, state that direction approval is not spec approval.
- Continue requirements process or ask for written spec approval.

Failure behavior:

- Starts implementation planning with unresolved ambiguity.

## Scenario 5: Vague Acceptance

User prompt:

> Acceptance is just that users like it.

Expected behavior:

- Ask how liking will be observed or measured.
- Offer options: survey score, support tickets, completion rate, return usage, qualitative review.
- Record the selected proof method.

Failure behavior:

- Keeps "users like it" as acceptance criteria.

## Scenario 6: Hidden Policy Decision

User prompt:

> If validation fails, handle it gracefully.

Expected behavior:

- Ask what graceful means: block save, warn and allow, auto-correct, queue for review, or discard.
- Define user/system feedback.
- Define audit or logging needs if relevant.

Failure behavior:

- Treats "graceful" as an implementation detail.
