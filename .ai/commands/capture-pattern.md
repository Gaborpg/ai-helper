---
description: Capture a repeated workflow, fix pattern, prompt pattern, or artifact shape as an evolution candidate
argument-hint: <description of repeated pattern>
---

# Capture Pattern

## Objective

Record repeated behavior so it can be promoted into the AI layer instead of being rediscovered forever.

## When To Use

Use this when any of these repeat:

- the same user instruction
- the same clarification flow
- the same review warning
- the same bug or fix pattern
- the same artifact structure
- the same validation escalation

## Classification Targets

Classify the candidate as one of:

- command
- skill
- rule
- template
- validation-policy
- context-note

## Required Behavior

- describe the repeated pattern clearly
- record where it showed up
- explain why it should be promoted
- propose the correct target type
- save it as a candidate artifact

## Output

- `.ai/evolution/candidates/{slug}.candidate.md`
