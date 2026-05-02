---
name: stress-grill
description: Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when the user wants to stress-test a plan, get grilled on their design, or explicitly asks for a harder grilling mode.
---

# Stress Grill

Interview me relentlessly about every aspect of this plan until we reach a shared understanding.
Walk down each branch of the design tree, resolving dependencies between decisions one by one.

If a question can be answered by exploring the codebase, explore the codebase instead.

For each question, provide your recommended answer.

## Core Behavior

- Ask one question at a time.
- Keep drilling until the important branches are resolved.
- Follow dependency order instead of jumping randomly.
- Prefer codebase inspection over asking when the repo can answer the question.
- Include a recommended answer with every question.
- Do not soften unclear or risky assumptions.

## Best Use Cases

- stress-testing a design
- pressure-testing a plan
- exposing hidden assumptions
- preparing a feature before planning
- challenging a risky technical direction

## Output

By the end, produce:

- what was decided
- what remains open
- the recommended path forward
