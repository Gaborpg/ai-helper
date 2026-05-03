# Repo Operating Policy

Use this file during onboarding to record how the AI should actually operate in this repo.

This is more than stack detection. It should capture the repo's working rules.

## Commands

Document:

- which commands are used most often
- when `plan` is mandatory
- when `create-prd` is expected
- when `zoom-out` should be used before implementation
- when direct small-task implementation is acceptable
- when commands should load approved example references from `.ai/context/examples.md`
- when commands must cite exact example file paths in their reasoning

## Validation

Document:

- the real lint, test, and build commands
- whether multiple builds or variants exist
- when browser verification is required
- when Playwright or UI testing is required
- any domain-specific validation expectations

## Review

Document:

- the highest-risk areas in this repo
- what review should focus on
- what evidence is required before handoff
- what common regressions matter most

## Skills

Document:

- which skills are used most often
- when `grill-me` is the default
- when `stress-grill` is preferred
- when skills must inspect approved example references before reasoning about local patterns
- when skills must show exact approved example file paths instead of vaguely referring to "existing patterns"

## PR Rules

Document:

- target PR platform
- title/body expectations
- linked issue or work-item expectations
- validation evidence expectations
- rollout or release note expectations

## Tools And MCP Status

Document:

- which declared capabilities are mandatory
- which are optional
- which are already configured
- which are still missing setup
- what human follow-up is required

## Workflow Exceptions

Document:

- when the normal PIV loop needs extra steps
- when some validations can be skipped
- when special approvals are required
