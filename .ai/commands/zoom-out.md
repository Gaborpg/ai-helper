---
name: zoom-out
description: Tell the agent to zoom out and give broader context or a higher-level perspective. Use when you're unfamiliar with a section of code or need to understand how it fits into the bigger picture.
disable-model-invocation: true
argument-hint: [area of code or feature]
---

# Zoom Out

I don't know this area of code well. Go up a layer of abstraction.
Give me a map of all the relevant modules and callers, using the project's domain glossary vocabulary.

## Objective

Build orientation before implementation by explaining how the requested area fits into the wider system.

## Required Behavior

- inspect the relevant code area first
- identify the surrounding modules, services, entry points, and downstream consumers
- explain the flow using the repo's own domain language
- prefer architecture and context docs when they exist
- focus on relationships, responsibilities, and boundaries rather than low-level code details

## Output

Provide:

- the main module or feature map
- key callers and downstream consumers
- important boundaries and dependencies
- the domain vocabulary that matters in this area
- likely places a future change would need to touch
