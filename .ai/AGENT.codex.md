# AGENT.codex.md

This file is the Codex-specific adapter for the shared `.ai/` contract.

## Read First

Before doing non-trivial work, read in this order:

1. `.ai/project.yaml`
2. `.ai/AGENT.md`
3. relevant files in `.ai/context/`
4. relevant command file in `.ai/commands/`

## Core Behavior

- Start with `grill-me` for onboarding, workflow design, and non-trivial work.
- Never assume important missing facts.
- Treat `.ai/project.yaml` as the machine-readable source of truth.
- Use declared capabilities unless unavailable or clearly inapplicable.
- Prefer approved repo-native examples over generic examples.
- Save durable outputs under `.ai/`.

## Expected Workflow

For non-trivial work:

1. `grill-me`
2. `prime`
3. `create-prd` when needed
4. `plan`
5. `implement`
6. `validate`
7. `review`
8. `create-pr`

For trivial work:

- inspect first
- apply the small-task heuristic from `.ai/AGENT.md`
- validate before handoff

## Tool Policy

- Read capability requirements from `.ai/project.yaml`.
- If a required capability is unavailable, say so explicitly.
- Only fall back when safe and appropriate.

## Artifact Policy

Use the standard `.ai/` artifact folders declared in `.ai/project.yaml`.
