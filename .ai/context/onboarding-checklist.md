# Onboarding Checklist

Use this checklist during repo onboarding after copying `.ai/` into a target repo.

The goal is to separate:

- what AI should infer from the repo
- what AI should propose as a draft
- what a human must confirm before finalizing

## Onboarding Flow

1. start with `grill-me`
2. inspect the repo
3. draft `.ai/` updates
4. ask for confirmation on uncertain or policy-level choices
5. finalize the repo-specific `.ai/` setup

## AI Should Infer When Possible

AI should inspect the repo first and draft these when evidence exists:

- stack and framework
- workspace style or monorepo shape
- package manager
- likely validation commands
- likely PR platform
- likely test tooling
- candidate example files
- likely overlays
- likely capabilities and tools

## Human Must Confirm

These should not be silently finalized when uncertain:

- repo purpose
- enabled overlays
- mandatory capabilities
- approved example files
- final validation commands
- PR platform
- whether UI testing is mandatory for certain flows
- whether memory integration is desired

## Human Optional Input

These are useful but not always required on day one:

- org-specific review policy
- rollout expectations
- naming preferences for artifacts
- stricter promotion policy for evolution candidates

## Good Onboarding Behavior

Good onboarding:

- starts with `grill-me`
- uses repo inspection before asking
- proposes drafts instead of pretending certainty
- asks only for the highest-value confirmations
- leaves a reviewable paper trail in `.ai/`

## Bad Onboarding Behavior

Bad onboarding:

- invents stack rules without checking the repo
- finalizes tools without confirmation
- chooses example files without showing them
- hardcodes validation commands without evidence
- implements product features during setup
