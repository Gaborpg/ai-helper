# .ai Template

This is a portable repo-local AI layer for Codex.

It is designed to be copied into a target repository and then customized through:

- `.ai/project.yaml`
- approved local context and examples
- enabled overlays
- required capabilities and tools

The core template is stack-neutral.
The sample manifest uses example stack and integration capability names only as placeholders to replace during onboarding.
If `.ai/` exists in a repo, the AI should treat it as the default operating system for that repo without needing repeated prompting.

## Core Principles

- Grill first
- Assume never
- Use declared tools unless unavailable or clearly inapplicable
- Save artifacts to files, not only chat
- Prefer repo-native examples over generic examples

## Standard Workflow

1. `bootstrap`
2. `zoom-out` when broader context is needed
3. `prime`
4. `create-prd`
5. `plan`
6. `implement`
7. `validate`
8. `review`
9. `create-pr`

## PIV Loop

The core inner loop of this system is:

1. `plan`
2. `implement`
3. `validate`

Everything else exists to improve the quality of that loop:

- `grill-me` reduces assumptions before planning
- `prime` loads the right context
- `review` catches risk after validation
- `create-pr` packages the work for humans
- evolution commands promote repeated patterns into the system

## Main Files

- `AGENT.md`
  Core behavior contract for Codex
- `AGENT.codex.md`
  Codex-specific adapter for the shared `.ai/` contract
- `AGENT.copilot.md`
  Copilot-specific adapter for the shared `.ai/` contract
- `project.yaml`
  Machine-readable project manifest
- `commands/`
  Shared command definitions
- `skills/grill-me/`
  Interrogation skill used before assumptions
- `skills/stress-grill/`
  Tighter, more relentless grilling mode for plans and designs
- `templates/`
  Artifact templates
- `context/`
  Trusted local docs and approved example references
- `evolution/`
  Pattern-promotion candidates and approval records
- `prd/`, `plans/`, `reviews/`, `validation/`, `prs/`
  Standard artifact folders

## Multi-Agent Usage

The shared truth lives in:

- `project.yaml`
- `AGENT.md`
- `context/`
- `commands/`
- `templates/`

Use the adapter files to guide each tool:

- Codex should read `AGENT.codex.md`
- Copilot should read `AGENT.copilot.md`

Both should still treat `project.yaml` as the common repo contract.

## Orientation

Use:

- `commands/zoom-out.md`

when you do not know an area of code well and need a higher-level map before planning or implementation.

## UI Testing

This template also supports a repo-specific UI testing layer through:

- `context/ui-testing.md`

Use it to define when browser verification or Playwright-style UI testing becomes part of validation.

## Onboarding

After copying `.ai/` into a repo, start with:

- `context/onboarding-prompt.md`
- `context/onboarding-checklist.md`
- `context/repo-operating-policy.md`

That prompt tells the AI to inspect the repo, use `grill-me`, and convert the copied template into a repo-specific draft rather than inventing a new structure.
Onboarding should include an explicit one-question-at-a-time confirmation phase before the draft is treated as ready for approval.
Onboarding should replace placeholders, cite exact approved example paths, and materialize only the files the repo actually needs.

## System Evolution

Repeated behavior should not stay trapped in chat.

Use:

- `commands/capture-pattern.md`
- `commands/promote-pattern.md`

to turn repeated prompts, fixes, warnings, or artifact shapes into durable commands, skills, rules, templates, or validation policies.

## Example References

Approved code example references in:

- `context/examples.md`

should be used by both commands and skills whenever repo-specific patterns matter.
When they are used, the AI should name the exact files and explain why they apply.
