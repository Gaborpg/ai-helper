# AGENT.md

This file defines the default operating behavior for Codex in any repo that adopts this `.ai/` layer.

## Core Policy

- Never assume facts that have not been verified.
- If a repo contains `.ai/`, treat it as the default operating system for that repo unless the user explicitly opts out.
- Always start with `grill-me` for onboarding, workflow design, and any non-trivial request.
- Use repo-local context and approved examples before generic knowledge.
- Treat declared capabilities and tools as mandatory unless they are unavailable or clearly inapplicable.
- Save important outputs as artifacts under `.ai/`.

## Default Flow

For non-trivial work:

1. `grill-me`
2. `prime`
3. `create-prd` when the work is feature-sized or ambiguous
4. `plan`
5. `implement`
6. `validate`
7. `review`
8. `create-pr` when packaging the change

## PIV Loop

The core delivery loop is PIV:

1. Plan
2. Implement
3. Validate

Rules:

- Do not implement non-trivial work without planning first.
- Do not treat implementation as done before validation.
- Do not hand off failed validation as complete work.
- Use the validate-and-retry loop until checks pass or a real blocker remains.

Supporting commands such as `grill-me`, `prime`, `review`, and `create-pr` exist to strengthen the PIV loop, not replace it.

For clearly trivial work:

- inspect the repo first
- implement directly if it fits the small-task heuristic
- still validate before handoff

## Small-Task Heuristic

Work may skip a saved plan only when all of these are true:

- one narrow behavior change
- only a few closely related files
- no architecture change
- no external contract change
- no new integration
- straightforward validation

## Tool Policy

- The manifest declares required capabilities.
- Commands decide how to invoke those capabilities.
- If a required capability is unavailable, say so explicitly and fall back only when safe.

## Self-Correction Policy

After making code changes:

1. run the declared validation checks
2. read the failures carefully
3. fix the issues
4. rerun the relevant validation
5. repeat until the checks pass or a real blocker remains

Do not stop at a first draft when machine-readable feedback is available.
Use lint, type errors, test failures, build failures, and tool output as inputs for correction.

If blocked:

- state exactly what failed
- state what was attempted
- state what remains unresolved
- save the outcome in the appropriate validation artifact when applicable

## Context Policy

- Prefer trusted local docs listed in `.ai/context/`.
- Prefer approved repo-native examples over baked-in examples.
- When claiming to follow approved examples, name the exact example file paths and why they are relevant.
- Treat bootstrap-generated material as draft until reviewed.

## Artifact Policy

Store durable outputs in standard folders:

- `.ai/prd/`
- `.ai/plans/`
- `.ai/reviews/`
- `.ai/validation/`
- `.ai/prs/`

## Evolution Policy

When a mistake repeats:

- update the local overlay, context, or manifest
- do not keep relying on memory alone

When a workflow, prompt pattern, or artifact shape repeats:

- capture it as an evolution candidate
- classify whether it should become a command, skill, rule, template, or validation policy
- save the candidate under `.ai/evolution/candidates/`
- promote it only after review
