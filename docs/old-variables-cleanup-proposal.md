# Old Variables Cleanup Proposal

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Status

Cleanup is complete.

Reason: the user explicitly approved deleting old variables without an additional pre-cleanup audit.

## Completed Preconditions

- Whole-file Figma binding migration is complete.
- Whole-file old variable binding references: 0.
- Local repository consumer impact audit is complete.
- Deprecated variable registry exists: `registry/deprecated-variables.json`.
- Cleanup checklist exists: `docs/deprecated-variables-cleanup.md`.
- External consumer audit plan exists: `reports/external-consumer-audit.md`.
- External consumer confirmation exists: `reports/external-consumer-confirmation.md`.
- Cleanup result exists: `reports/figma-old-variables-cleanup-result.md`.

## Cleanup Result

Deprecated variables deleted from Figma: 36

Replacement variables materialized before deletion: 36

## Proposed Cleanup Batch

Cleanup happened as a separate Figma write batch.

Suggested sequence:

1. Replacement values were materialized where replacements aliased old variables.
2. Deprecated variables were removed.
3. Registry and docs were updated.

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

Use semantic/component replacements only.

Optional next step: run a post-cleanup read-only audit if visual or token regressions are suspected.
