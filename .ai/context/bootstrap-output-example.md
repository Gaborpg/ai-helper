# Bootstrap Output Example

This file shows what a useful first onboarding draft can look like after AI inspects a real repo and updates the copied `.ai/` folder.

It is an example only.
The real output should reflect the actual target repo.

## Expected Bootstrap Summary

Example summary:

```text
I inspected the repo and drafted the local `.ai/` layer for review.

Detected:
- stack: Angular
- workspace style: Nx monorepo
- package manager: pnpm
- likely UI test tooling: Playwright
- likely PR platform: Azure DevOps

Drafts updated:
- `.ai/project.yaml`
- `.ai/context/architecture.md`
- `.ai/context/examples.md`
- `.ai/context/tools.md`
- `.ai/context/repo-operating-policy.md`

I still need confirmation on:
- enabled overlays

Question: Should the primary overlay stay `angular`, with `github` and `ui-test` as secondary overlays?

Recommended answer: yes.

Why: The repo is clearly Angular-first, while GitHub and UI testing shape workflow and validation rather than core component architecture.
```

## Example Draft `project.yaml` Changes

Example:

```yaml
project:
  name: "customer-portal"
  purpose: "Customer-facing Angular portal for account management and service requests."
  repo_type: "application"
  primary_stack: "angular"
  workspace_style: "nx-monorepo"
  package_manager: "pnpm"

overlays:
  primary: "angular"
  secondary:
    - "azure"

capabilities:
  angular_mcp:
    required: true
    provider: "angular-mcp"
    notes:
      - "Use for Angular-aware repo inspection and implementation."
  azure_devops:
    required: true
    provider: "azure-devops"
    notes:
      - "Use for PR and work-item workflows."
  browser:
    required: false
    provider: "browser-use"
    notes:
      - "Use for interactive UI verification."
  ui_test:
    required: false
    provider: "playwright"
    notes:
      - "Use for end-to-end validation of critical UI flows."
```

## Example Draft `architecture.md`

Example:

```md
# Architecture Notes

- Apps live under `apps/`
- Shared libraries live under `libs/`
- Routing is feature-based with lazy-loaded areas
- State is primarily RxJS-based in feature facades
- Forms use Angular reactive forms
- UI tests live under `apps/customer-portal-e2e/`
- The repo's PIV loop should include Playwright validation for risky customer journeys
```

## Example Draft `examples.md`

Example:

```md
# Approved Examples

- `apps/customer-portal/src/app/orders/orders-page.component.ts` - page/container pattern
- `libs/orders/data-access/src/lib/orders.facade.ts` - facade and state orchestration pattern
- `libs/orders/data-access/src/lib/orders.service.ts` - API service pattern
- `libs/orders/ui/src/lib/order-filter-form.component.ts` - reactive form pattern
- `apps/customer-portal-e2e/src/orders.spec.ts` - UI test pattern
```

## Example Draft `tools.md`

Example:

```md
# Tool Notes

- Angular MCP is mandatory for Angular feature work when available
- Azure DevOps tooling is mandatory for PR and work-item workflows
- Browser verification is required for user-facing UI changes
- Playwright validation is required for risky flows involving forms, navigation, or multi-step journeys
```

## Example Draft `repo-operating-policy.md`

Example:

```md
# Repo Operating Policy

## Commands

- `plan` is mandatory for non-trivial onboarding, registration, and state-management changes
- `zoom-out` should be used when touching unfamiliar onboarding or Elf store areas
- direct implementation is acceptable only for narrow UI text or styling fixes

## Validation

- use `npm run lint`, `npm run test -- --watch=false`, and `npm run build`
- require browser verification for user-facing onboarding and registration changes
- require Playwright validation for risky multi-step flows

## Review

- prioritize onboarding regressions, registration validation bugs, and Elf state-flow issues

## PR Rules

- Azure DevOps is the PR platform
- PRs must include linked work items and validation evidence

## Tools And MCP Status

- Angular MCP: required
- Azure DevOps integration: required
- Browser automation: optional but recommended for UI verification
- Playwright: expected for risky flows
```

## Human Confirmation Checklist

After bootstrap, the human should confirm:

- repo purpose
- overlays
- mandatory capabilities
- validation commands
- PR platform
- approved examples
- whether UI testing is mandatory for certain flows

These confirmations should be asked one at a time, not as a bundled list in a single turn.

## What Good Bootstrap Does Not Do

Good bootstrap does not:

- pretend uncertain facts are final
- invent examples without showing them
- skip review of validation commands
- silently choose tools that were not confirmed
- implement product features during onboarding
