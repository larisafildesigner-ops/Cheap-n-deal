# Old Variables Cleanup Proposal

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Status

Cleanup is proposed and ready for a final pre-cleanup audit.

Reason: the current Figma file and local repository are clean, and the user confirmed the Figma library is not published.

## Completed Preconditions

- Whole-file Figma binding migration is complete.
- Whole-file old variable binding references: 0.
- Local repository consumer impact audit is complete.
- Deprecated variable registry exists: `registry/deprecated-variables.json`.
- Cleanup checklist exists: `docs/deprecated-variables-cleanup.md`.
- External consumer audit plan exists: `reports/external-consumer-audit.md`.
- External consumer confirmation exists: `reports/external-consumer-confirmation.md`.

## Remaining Gates

Do not delete, hide, rename, or move old variables until:

1. A final whole-file audit is run immediately before cleanup.
2. The user explicitly approves the Figma cleanup write action.
3. Automation/token exports outside this repo are either checked or accepted as out of scope.

## Proposed Cleanup Batch

When blockers are resolved, cleanup should happen as a separate reviewed batch.

Suggested sequence:

1. Re-run whole-file binding audit.
2. Re-check external consumer status.
3. Snapshot/export deprecated registry.
4. Hide or archive old variables first if Figma supports a reversible approach.
5. Delete variables only after a deprecation window and explicit approval.

## Variables In Scope

Use `registry/deprecated-variables.json` as the source of truth.

Variable families in scope:

- Border
- Text
- Icon
- Background
- State
- Button/component
- Radius
- Spacing
- Accent

## Not In Scope

- Renaming current semantic/component aliases.
- Changing component sets or variants.
- Changing styles.
- Changing product screen layout.
- Creating new tokens.

## Recommendation

Keep old variables for now.

Proceed only after the user explicitly confirms cleanup execution.

The recommended next step is a read-only final pre-cleanup audit, followed by a separate cleanup batch only if the audit is clean.
