# Onboarding Prompt

Use this prompt after copying `.ai/` into a target repo.

```text
Set up the copied `.ai/` folder for this repo.

Start with grill-me and do not assume anything important.
Inspect the repo first, then update the existing `.ai/` setup into a repo-specific draft for review.

Requirements:
- treat everything as draft until I approve it
- detect stack, workspace style, package manager, validation commands, and likely tools/MCPs
- update `.ai/project.yaml`
- update `.ai/AGENT.md` only where repo-specific behavior is needed
- update `.ai/context/architecture.md`
- update `.ai/context/examples.md`
- update `.ai/context/tools.md`
- harvest candidate repo-native examples for UI patterns, services or business logic, tests, and state or workflow patterns
- after inspection, ask me confirmation questions one at a time with grill-me before finalizing the draft
- ask me to confirm overlays, mandatory capabilities, PR platform, validation commands, and approved examples
- save artifacts under `.ai/`

Do not implement app features yet. Only onboard the repo.
```

## Notes

- This prompt is intentionally strict about `grill-me` and assumption control.
- The goal is to adapt the copied `.ai/` structure, not regenerate a new one.
- Human review is required before treating the onboarding output as final.
