# UI Testing Layer

Use this file to define when browser-based UI testing is important in this repo.

## Purpose

UI testing protects behavior that unit tests and static analysis often miss:

- real navigation
- browser interaction
- multi-step flows
- form validation
- rendering and timing issues
- end-to-end regressions

## Recommended Tools

- Playwright for end-to-end and browser interaction testing
- browser automation capability for targeted manual verification

## When This Layer Matters

This layer is especially useful when the repo includes:

- forms with validation
- auth or guarded navigation
- multi-page user journeys
- data loading states
- modal, drawer, or overlay interactions
- responsive UI behavior

## Validation Policy Ideas

- require targeted Playwright coverage for risky user flows
- require browser verification after UI-heavy changes
- escalate from unit tests to UI tests when regressions are likely to hide in integration boundaries

## Repo-Specific Notes

Document here:

- where Playwright tests live
- how to run them
- which flows are most critical
- when UI testing is mandatory versus optional
