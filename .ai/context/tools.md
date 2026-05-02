# Tool Notes

Use this file to explain how required capabilities should be used in this repo.

Suggested contents:

- which MCPs are mandatory
- when browser verification is required
- when UI test tooling such as Playwright is required
- when PR tooling must be used
- fallback rules if a tool is unavailable

## Recommended Capability Adoption Order

For many frontend or full-stack repos, a practical adoption order is:

1. stack-specific MCP or repo-aware tooling
2. PR and work-item integration
3. browser verification
4. UI test tooling such as Playwright
5. memory integration after the local AI layer is stable

## Why Playwright Can Be Valuable

Playwright is useful when the repo has meaningful UI behavior that static code review and unit tests do not fully protect.

Typical value:

- verifies forms, buttons, navigation, and page transitions
- catches browser-level regressions
- checks end-to-end flows across multiple screens
- validates loading, error, and success states
- helps confirm fixes that depend on real rendering and interaction

Use Playwright or a comparable UI-test layer when:

- route changes affect navigation
- forms or validation behavior change
- complex interactive UI is touched
- a bug only reproduces in the browser
- cross-page user flows matter

Playwright is especially useful inside the `validate` phase of the PIV loop.
