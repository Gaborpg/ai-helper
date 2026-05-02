# PIV Loop

PIV stands for:

1. Plan
2. Implement
3. Validate

This is the core delivery loop of the `.ai/` system.

## Why It Exists

The loop reduces low-quality AI work by forcing three separate responsibilities:

- planning before code
- implementation against a concrete plan
- validation with self-correction before handoff

## Command Mapping

- Plan: `.ai/commands/plan.md`
- Implement: `.ai/commands/implement.md`
- Validate: `.ai/commands/validate.md`

## Supporting Workflow

These steps strengthen the loop:

- `grill-me` before PIV when assumptions are risky
- `prime` before PIV to load the right code and patterns
- `review` after validation to catch residual risk
- `create-pr` after review to package the change

## Hard Rules

- Non-trivial work should not skip planning.
- Code is not done when written; it is done after validation passes or a blocker is clearly stated.
- Validation failures should trigger correction and rerun, not handoff.
- Repeated failures or workflows should be promoted into the `.ai/` layer through evolution artifacts.
