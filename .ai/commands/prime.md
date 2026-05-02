---
description: Build focused understanding of the repo before planning or implementation
argument-hint: [feature description or path]
---

# Prime

## Objective

Load the smallest useful amount of context needed to understand the request correctly.

## Required Behavior

- Start with `grill-me` unless the task is clearly trivial or the facts are already verified.
- Read `.ai/project.yaml` and `.ai/AGENT.md`.
- Inspect the relevant code paths, tests, build config, and approved local examples.
- Use required capabilities when the manifest declares them.
- Prefer repo-native patterns over generic examples.

## Output

Produce a concise summary of:

- current behavior
- relevant files or layers
- patterns to preserve
- risks or unknowns
- validation path
