# Template Materialization

This folder describes how the standalone template should be turned into a repo-specific `.ai/` layer.

## Principle

The standalone template may contain onboarding scaffolding, examples, and reference material that help bootstrap a repo.

After onboarding, the target repo should keep only the `.ai/` files it actually needs.

## Materialization Rules

- replace generic placeholder values with repo truth when evidence exists
- if a value is still unknown, mark it explicitly as unresolved
- do not leave silent generic defaults behind
- cite exact approved example file paths when selecting repo-native patterns
- keep onboarding-only scaffold material out of the target repo unless it is still useful there

## Goal

The result of onboarding should feel like a repo-specific operating system, not a copied generic template with leftovers.
