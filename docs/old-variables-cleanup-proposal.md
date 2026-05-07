# Old Variables Cleanup Proposal

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Status

Cleanup is proposed but blocked.

Reason: the current Figma file and local repository are clean, but external Figma consumers and external automation have not been confirmed.

## Completed Preconditions

- Whole-file Figma binding migration is complete.
- Whole-file old variable binding references: 0.
- Local repository consumer impact audit is complete.
- Deprecated variable registry exists: `registry/deprecated-variables.json`.
- Cleanup checklist exists: `docs/deprecated-variables-cleanup.md`.
- External consumer audit plan exists: `reports/external-consumer-audit.md`.

## Blockers

Do not delete, hide, rename, or move old variables until:

1. Published library status is confirmed.
2. Downstream Figma consumers are identified or ruled out.
3. External automation and token exports are checked.
4. A final whole-file audit is run immediately before cleanup.

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

Proceed only after the user confirms one of these:

- the Figma file is not published as a library and has no external consumers;
- all external consumers have migrated;
- deletion risk is accepted explicitly.

