# Codex AI Template

This project is a portable starter for a repo-local AI layer that can support both Codex and Copilot across different stacks and repos.

## Layout

- `.ai/`
  The AI-layer files you can copy into another repo

## Intended Use

1. Review and refine the files in `.ai/`
2. Copy `.ai/` into a target repo
3. Customize the manifest, overlays, commands, tools, and examples for that repo
4. Use the tool-specific adapter file:
   - `.ai/AGENT.codex.md`
   - `.ai/AGENT.copilot.md`

## Notes

- This is a draft starter generated from the workshop exploration
- The core structure is stack-neutral
- It should be treated as a reviewable base, not final production truth
