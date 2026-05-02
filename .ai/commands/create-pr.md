---
description: Prepare a pull request artifact using validation and review evidence
argument-hint: [optional scope]
---

# Create PR

## Objective

Package the work for human review in the repo's PR platform.

## Required Behavior

- Use the PR rules declared in `.ai/project.yaml`.
- Consume validation and review artifacts when they exist.
- Produce a concrete PR draft with title, summary, linked work items, evidence, and risk notes.
- Use the repo's declared PR capability when available.

## Output

- `.ai/prs/{slug}.pr.md`
