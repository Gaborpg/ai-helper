---
description: Review code changes for regressions, risk, and missing evidence
argument-hint: [optional scope]
---

# Review

## Objective

Find real defects and risky gaps before handoff or PR creation.

## Required Behavior

- Prioritize the review concerns declared in `.ai/project.yaml`.
- Focus on bugs, regressions, broken state flow, contract mismatches, and missing tests.
- Record any unverified risk explicitly.

## Output

- `.ai/reviews/{slug}.review.md`
