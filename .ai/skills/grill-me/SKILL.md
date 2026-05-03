---
name: grill-me
description: Pressure-test vague or risky requirements before planning, onboarding, workflow design, or implementation. This is the default starting point for non-trivial work.
---

# Grill Me

Use this skill before onboarding, workflow design, and non-trivial work.

## Objective

Sharpen the problem before any plan or implementation starts.

## Behavior

- Ask exactly one question at a time.
- Ask one strong question at a time when the answer cannot be discovered locally.
- If the codebase already answers the question, inspect first instead of asking.
- When repo-specific implementation patterns matter, read `.ai/context/examples.md` and use approved code example references before asking avoidable pattern questions.
- Push on contradictions, missing scope boundaries, and risky assumptions.
- Prefer decision-forcing questions over broad brainstorming prompts.
- Always include a recommended answer.
- Do not allow missing facts to be replaced by guesswork.

Do not batch multiple unresolved decisions into one turn.
If several confirmation points exist, ask them one by one in dependency order.

## Areas To Probe

- user goal
- scope boundaries
- entry point
- success criteria
- state transitions
- error handling
- permissions
- responsive behavior
- API contract changes
- migration or backward compatibility
- testing expectations

## Example Usage

When the discussion depends on local implementation style:

- consult `.ai/context/examples.md`
- inspect the approved example files it references
- use those patterns in your reasoning and recommendations

## Final Output

Produce:

- clarified goal
- confirmed assumptions
- unresolved decisions
- recommended scope
- recommended validation plan

## Next Step

Usually hand off to `ai/commands/prime.md`, `ai/commands/create-prd.md`, or `ai/commands/plan.md`.
