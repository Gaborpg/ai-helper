# Quickstart

This guide shows how to use the `.ai/` template in a real repo.

## 1. Copy The AI Layer

Copy the `.ai/` folder from this template project into your target repo.

## 2. Onboard The Repo

Use the prompt in:

- `.ai/context/onboarding-prompt.md`

That onboarding flow should:

- start with `grill-me`
- inspect the repo
- draft repo-specific `.ai/` files
- ask for confirmation on critical facts

## 3. Review The Draft

Confirm or correct:

- `.ai/project.yaml`
- `.ai/AGENT.md`
- `.ai/context/architecture.md`
- `.ai/context/examples.md`
- `.ai/context/tools.md`

Do not treat the first draft as final truth until reviewed.

## 4. Daily Working Loop

For non-trivial work:

1. `grill-me`
2. `zoom-out` if you need broader context
3. `prime`
4. `create-prd` if needed
5. `plan`
6. `implement`
7. `validate`
8. `review`
9. `create-pr`

## 5. PIV Core Loop

The core inner loop is:

1. `plan`
2. `implement`
3. `validate`

Implementation is not done until validation passes or a blocker is clearly documented.

## 6. Small Fixes

Small tasks may skip a saved plan only when they are:

- one narrow behavior change
- a few closely related files
- no architecture change
- no new integration
- easy to validate

Even then, validation still happens.

## 7. Evolve The System

When patterns repeat:

- use `capture-pattern`
- review the candidate
- use `promote-pattern`

This turns repeated prompts, fixes, or warnings into durable AI-layer behavior.

## 8. Main Files

- `.ai/project.yaml`
  Machine-readable repo contract
- `.ai/AGENT.md`
  Shared behavior contract
- `.ai/AGENT.codex.md`
  Codex adapter
- `.ai/AGENT.copilot.md`
  Copilot adapter
- `.ai/context/`
  Trusted local context
- `.ai/commands/`
  Workflow definitions
- `.ai/templates/`
  Artifact templates

## 9. Main Commands

- `bootstrap`
- `zoom-out`
- `prime`
- `create-prd`
- `plan`
- `implement`
- `validate`
- `review`
- `create-pr`
- `capture-pattern`
- `promote-pattern`
