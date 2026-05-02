---
description: Execute a scoped change while preserving repo patterns and required tooling
argument-hint: <plan file or feature description>
---

# Implement

## Objective

Make the smallest clean change that solves the request.

## Required Behavior

- Use a saved plan for non-trivial changes.
- If no plan exists, only proceed when the small-task heuristic allows it.
- Re-read the exact target files before editing.
- Use declared capabilities unless unavailable or inapplicable.
- Keep changes aligned with approved local examples.
- Update tests when the changed behavior is risky or meaningful.
- Hand off immediately into the validate-and-retry loop after implementation.

## Validate-And-Retry Loop

After code changes:

1. run the declared validation checks
2. inspect the failures
3. fix the problems
4. rerun the relevant checks
5. repeat until clean or blocked

Do not treat implementation as complete just because the code was written.

## Output

Explain:

- what changed
- why it fits repo patterns
- what was validated
- whether any blocker remains
