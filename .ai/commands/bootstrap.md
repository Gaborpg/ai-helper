---
description: Inspect a repo, ask a small required questionnaire, and generate a draft local .ai layer
argument-hint: [target repo path]
---

# Bootstrap

## Objective

Create a first draft `.ai/` layer for a target repo without pretending unknown facts are settled.

## Required Behavior

- Start with `grill-me`.
- Inspect the repo before asking avoidable questions.
- Detect likely stack, package manager, workspace style, tools, and integrations.
- Harvest candidate repo-native examples.
- After repo inspection, run an explicit human confirmation phase with `grill-me`.
- Ask confirmation questions one at a time, not as a bundle.
- Do not finalize the onboarding draft until unresolved policy choices have been asked interactively.
- Generate draft `.ai/` files and clearly mark them as review-required.

## Minimum Human Confirmations

- repo purpose
- enabled overlays
- mandatory capabilities and tools
- validation commands
- PR platform
- review policy
- example approvals
- memory integration intent

## Outputs

- draft `.ai/project.yaml`
- draft `.ai/AGENT.md`
- draft `.ai/context/` files
- standard artifact folders
