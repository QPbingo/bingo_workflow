# Brainstorming With Grilling Workflow

Use this workflow from the first requirements question through final spec approval.

## 1. Explore Context

If the task is attached to an existing project, inspect available context before asking questions:

- Existing docs, specs, issue descriptions, README files, and architecture notes
- Existing UI, code paths, data models, APIs, and tests relevant to the request
- Recent changes if the request modifies current behavior

If context is not available, say what is unknown and continue by questioning the user.

## 2. Detect Scope Size

Before drilling into details, decide whether the request is too broad for one spec.

Split the work when it contains independent subsystems, user journeys, platforms, or release phases that can be specified and validated separately. Ask the user which sub-project to specify first.

Do not produce one giant spec for unrelated systems.

## 3. Offer Visual Support When Useful

If upcoming decisions are primarily visual, offer to create sketches, diagrams, mockups, or side-by-side comparisons. Keep this offer separate from clarifying questions.

Use visual support for layouts, flows, diagrams, and spatial comparisons. Use text for scope, terminology, acceptance criteria, tradeoffs, and policy decisions.

## 4. Establish The Problem Frame

Write a compact frame and ask the user to correct it:

- Problem: who has what problem, and why now
- Desired outcome: what must be true when this succeeds
- Users or actors: who initiates, who receives value, who is affected
- Constraints: business, technical, time, compatibility, security, privacy, legal
- Non-goals: what this will not solve

Completion criterion: the frame is specific enough that two agents would describe the same problem.

## 5. Clarify One Question At A Time

Ask exactly one question per turn. Each question should include:

- The decision being made
- Why it matters
- Your recommended answer
- The tradeoff if the user chooses differently

Prefer multiple-choice questions when the options are known. Use open-ended questions only when the choice space is genuinely unknown.

## 6. Maintain The Ambiguity Ledger

Track every unresolved interpretation in a visible ledger:

| ID | Ambiguity | Possible meanings | Recommendation | Decision |
|----|-----------|-------------------|----------------|----------|

Add a row when a term, behavior, priority, boundary, or outcome can reasonably be read in more than one way.

Do not remove a row silently. Mark it decided, excluded, or blocking.

## 7. Grill The Requirement Tree

Walk one branch at a time:

1. Actors: who can do this, who cannot, who is affected
2. Scenarios: happy path, alternate path, failure path
3. State: before, during, after; ownership; permissions
4. Data: inputs, outputs, validation, retention, migration
5. Boundaries: empty, duplicate, invalid, delayed, unauthorized, partial, cancelled
6. Conflicts: what wins when goals compete
7. Risks: misuse, irreversible action, privacy, security, operations

For each branch, ask:

- What happens if this is absent, duplicated, late, invalid, unauthorized, or partially complete?
- What should the system do instead of silently guessing?
- What observable result proves this branch works?

## 8. Define Goals And Non-Goals

Goals must describe outcomes, not implementation ideas.

Non-goals must be concrete enough to prevent scope creep. "Not doing analytics in v1" is useful. "Keep it simple" is not.

Every requirement later in the spec must map to a goal, or be removed.

## 9. Normalize Requirements

Before drafting the final spec, read `spec-template.md`.

Convert decisions into requirement statements. Each requirement must have:

- Trigger
- Preconditions
- Observable behavior
- Intended outcome
- Exception or boundary behavior when relevant
- Acceptance criteria

## 10. Compare Approaches

When there are meaningful alternatives, present 2-3 approaches. Lead with your recommendation.

For each approach, include:

- What it satisfies
- What it excludes or defers
- Main tradeoff
- Risk
- Which ambiguity decision would invalidate it

If there is only one sensible approach, say why and do not invent weak alternatives.

## 11. Present Sections For Approval

Present requirements in sections scaled to complexity. After each section, ask whether it matches the user's intent.

If the user corrects a section, update the ambiguity ledger and affected requirements before continuing.

## 12. Write The Final Spec

Use `spec-template.md` as the structure. The spec may live in the conversation or in a file if the user asked for a file.

Do not call it final until consistency gates pass.

## 13. Run Self-Review

Read `consistency-gates.md` and apply every gate. Fix failures inline.

If a gate cannot pass without user input, add a blocking open question and ask the next single question.

## 14. User Review Gate

Ask the user to review the written spec. If they request changes, update the spec and re-run consistency gates.

Only after explicit approval should you transition to implementation planning.

## 15. Transition

When the user approves the written spec, summarize:

- Spec approval status
- Any deferred non-goals
- Recommended next step for implementation planning

Do not implement unless the user explicitly asks.
