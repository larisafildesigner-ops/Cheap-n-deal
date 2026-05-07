# Deprecated Variables Cleanup

Date: 2026-04-29
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Current Status

The variable binding migration is complete for the whole Figma file.

Final audit:

- `Design-system`: 0 old variable binding references
- Product screens outside `Design-system`: 0 old variable binding references
- Whole Figma file: 0 old variable binding references

Deprecated variable registry: `registry/deprecated-variables.json`
Consumer impact audit: `reports/consumer-impact-audit.md`
External consumer audit: `reports/external-consumer-audit.md`
External consumer confirmation: `reports/external-consumer-confirmation.md`
Cleanup proposal: `docs/old-variables-cleanup-proposal.md`
Cleanup result: `reports/figma-old-variables-cleanup-result.md`
Post-cleanup audit: `reports/figma-post-cleanup-audit.md`

## Policy

Old variables were deleted from the current Figma file after explicit user approval.

Do not use old variable names for new work. Use the replacements in `registry/deprecated-variables.json`.

## Deprecated Variable Families

Deprecated groups:

- Border: `Border/default`, `Border/invers`
- Text: `text/primary`, `text/secondary`, `text/disable`, `text/inverse`
- Icon: `icon/default`, `icon/active`, `icon/disabled`
- Background: `background/base`, `background/muted`, `background/card`, `background/card inverse`, `background/overlay`
- State: `state/success`, `state/warning`, `state/error`, `state/info`
- Button/component: `btn/secondary`, `btn/secondary inverse`, `btn/disable`, `btn/full`, `btn/tertiary`
- Radius: `Radius/s`, `Radius/m`, `Radius/pill`
- Spacing: `space/0m`, `space/1m`, `space/2m`, `space/3m`, `space/4m`, `space/5m`, `space/6m`, `space/8m`, `space/10m`
- Accent: `accent/primary`

Use the replacements in `registry/deprecated-variables.json`.

## Consumer Impact Checklist

Before deleting, hiding, or archiving old variables:

1. Confirm whether this Figma file is published as a library.
2. Identify downstream Figma files using this library.
3. Open downstream files after library updates and check whether old variable names still appear.
4. Check token export scripts and any design-to-code automation.
5. Check Code Connect, handoff docs, QA docs, and implementation references.
6. Announce a deprecation window to designers and developers.
7. Run a final whole-file audit immediately before cleanup.
8. Perform cleanup as a separate reviewed batch.

## Cleanup Plan

Recommended sequence:

1. Documentation-only deprecation: complete.
2. Local repository consumer impact audit: complete.
3. External file/library usage audit plan: complete.
4. External file/library confirmation: complete; user confirmed library is not published.
5. Cleanup proposal: complete.
6. Final pre-cleanup audit: skipped by explicit user request.
7. Figma deletion batch: complete.
8. Post-cleanup audit: complete.

## Do Not Do

- Do not recreate old variables.
- Do not bind new work to old variable names.
- Do not rename current semantic/component aliases back to old names.
