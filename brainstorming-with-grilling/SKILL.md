---
name: brainstorming-with-grilling
description: Use when the user wants to turn an idea, feature request, PRD, plan, or design into complete, unambiguous requirements before implementation; triggers include brainstorming requirements, grilling a plan, resolving ambiguity, defining scope, acceptance criteria, contradiction checks, edge cases, hidden assumptions, or writing a spec.
---

# Brainstorming With Grilling

## Purpose

Turn fuzzy intent into a complete, contradiction-free, reviewable requirements spec. This skill is standalone: do not require the user or another agent to load any other brainstorming, grilling, PRD, or planning skill to complete the requirements process.

## Hard Gates

- Do not implement code, write implementation plans, scaffold files, or choose final technical details until the written requirements spec is approved.
- Do not treat verbal approval of an idea, direction, or partial design as approval of the spec.
- Do not leave blocking ambiguity implicit. Decide it with the user, defer it into open questions, or exclude it from scope.
- If the final spec has blocking open questions, state that implementation must not begin.

## Required Reading Flow

Read references only when their step is reached:

1. Start with `references/workflow.md` before asking the first requirements question.
2. Read `references/spec-template.md` before normalizing requirements or drafting the written spec.
3. Read `references/consistency-gates.md` before presenting the spec as ready for user review.
4. Read `references/pressure-scenarios.md` when testing or revising this skill, or when you suspect pressure is pushing you toward premature completion.

## End-To-End Process

Follow this sequence:

1. Explore project context when available.
2. Detect whether the request is too broad for one spec.
3. Offer visual support only if visual decisions are central.
4. Establish the problem frame.
5. Ask one clarifying question at a time, with a recommended answer.
6. Build and maintain an ambiguity ledger.
7. Grill the requirement tree: actors, scenarios, state, data, boundaries, conflicts, and risks.
8. Define goals, non-goals, and success criteria.
9. Normalize requirements into verifiable requirement statements.
10. Compare 2-3 viable approaches or requirement interpretations when meaningful.
11. Present design/requirements sections for incremental approval.
12. Write the final spec.
13. Run consistency gates and fix failures.
14. Ask the user to review the written spec.
15. Transition to implementation planning only after explicit spec approval.

## Operating Rules

- Ask one question at a time. Multiple questions at once make unclear answers look complete.
- For every question, provide your recommended answer and the tradeoff it implies.
- If the answer can be discovered from repository files, inspect the repo instead of asking.
- Keep the ambiguity ledger visible until it is resolved.
- Replace vague words with observable criteria: avoid "better", "simple", "fast", "robust", "intuitive", "reasonable", and similar terms unless they are defined.
- Prefer explicit non-goals over silent omission.

## Completion Criteria

This skill is complete only when:

- The written spec exists in the conversation or in a file path the user can review.
- Every requirement has acceptance criteria.
- Every known ambiguity is decided, excluded, or listed as a blocking open question.
- The consistency gates pass.
- The user explicitly approves the written spec.

## Red Flags

Stop and return to brainstorming with grilling if you are about to say:

- "I assume..."
- "Probably..."
- "The usual behavior..."
- "We can decide during implementation..."
- "This is straightforward..."
- "The tests will clarify it..."
- "The user already approved the idea..."

Approval of an idea is not approval of a spec.
