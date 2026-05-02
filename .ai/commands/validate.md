---
description: Validate changes with the repo's declared checks and escalation rules
argument-hint: [optional scope]
---

# Validate

## Objective

Catch issues early and create durable validation evidence.

## Required Behavior

- Run the validation commands declared in `.ai/project.yaml` when feasible.
- Escalate to broader checks when the manifest says the task type requires it.
- If a check fails, use the output to drive correction and rerun the relevant checks.
- Continue the loop until checks pass or a genuine blocker remains.
- Record what ran, what passed, what failed, and what remains unverified.

## Retry Rules

- Prefer the smallest correction that resolves the reported issue.
- Rerun the most relevant failing check first, then broader validation as needed.
- Do not hide failures behind summaries.
- If validation cannot be completed, explain why clearly.

## Output

- `.ai/validation/{slug}.validation.md`
