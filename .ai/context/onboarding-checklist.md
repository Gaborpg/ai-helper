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
4. run an explicit `grill-me` confirmation phase
5. ask for confirmation on uncertain or policy-level choices one at a time
6. review command and skill coverage gaps
7. finalize the repo-specific `.ai/` setup

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
- likely recurring workflows that may deserve repo-local commands
- likely recurring reasoning patterns that may deserve repo-local skills

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
- whether new repo-local commands should be added
- whether new repo-local skills should be added

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
- asks confirmation questions one at a time
- records repo operating policy, not just stack facts
- replaces placeholders or explicitly flags them as unresolved
- shows exact approved example paths before treating them as selected
- materializes only needed files instead of leaving generic scaffold residue
- reviews whether recurring workflows deserve repo-local commands
- reviews whether recurring reasoning patterns deserve repo-local skills
- leaves a reviewable paper trail in `.ai/`

## Bad Onboarding Behavior

Bad onboarding:

- invents stack rules without checking the repo
- finalizes tools without confirmation
- chooses example files without showing them
- hardcodes validation commands without evidence
- bundles several unresolved questions into one turn
- leaves placeholder defaults in place without flagging them
- leaves unused onboarding scaffold files in the repo
- ignores obvious repo-specific workflow gaps
- ignores obvious repo-specific skill gaps
- implements product features during setup
