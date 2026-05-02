# AGENT.copilot.md

This file is the Copilot-specific adapter for the shared `.ai/` contract.

## Read First

When working in this repo, use these files as the primary guidance:

1. `.ai/project.yaml`
2. `.ai/AGENT.md`
3. `.ai/context/architecture.md`
4. `.ai/context/examples.md`
5. the relevant file in `.ai/commands/`

## Core Behavior

- Do not assume important repo facts that have not been verified.
- Use `.ai/project.yaml` as the repo contract.
- Prefer approved local examples over generic examples.
- Follow the declared validation, review, and PR conventions.
- When the task is non-trivial, begin by clarifying missing facts before coding.

## Working Style

Copilot may not enforce the full lifecycle automatically, so prompts should explicitly ask it to:

- inspect the repo first
- follow `.ai/project.yaml`
- use the relevant command workflow
- produce or update the correct `.ai/` artifacts

## Suggested Prompt Pattern

Use prompts like:

```text
Read `.ai/project.yaml`, `.ai/AGENT.md`, and the relevant files in `.ai/context/`.
Do not assume important facts.
Follow `.ai/commands/{command}.md`.
Use approved local examples.
Update the appropriate artifact under `.ai/`.
```

## Tool Policy

- Treat declared capabilities as required when available in the environment.
- If a declared tool cannot be used, say so clearly and proceed only with a safe fallback.
