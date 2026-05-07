# External Consumer Audit

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Scope

Planning audit for consumers outside the current Figma file and local repository.

This report does not delete, hide, rename, or move any Figma variables.

## Current Confirmed Status

| Area | Status |
| --- | --- |
| Current Figma file bindings | Complete: 0 old variable binding references |
| Local repository references | Checked: old names appear only in docs/registry/reports |
| Deprecated variable registry | Complete |
| Cleanup checklist | Complete |
| External Figma files | Not directly discoverable from the local repo |
| Published library consumers | Requires manual Figma library/usage check |
| Automation outside this repo | Requires owner confirmation |

## What Must Be Checked Manually

Before any old variable cleanup in Figma:

1. Open `Cheap-n-deal_design` in Figma.
2. Check whether the file is published as a library.
3. If published, identify downstream files or teams that consume it.
4. Ask downstream file owners to accept library updates.
5. Search downstream files for old variable names from `registry/deprecated-variables.json`.
6. Check any token export, Code Connect, handoff, or design-to-code automation outside this repository.
7. Confirm no external consumer depends on old variable names.

## Decision Matrix

| External consumers found? | Recommended action |
| --- | --- |
| No | Prepare a cleanup batch proposal, but keep deletion separate and reviewed. |
| Yes, but migrated | Run a final consumer confirmation, then prepare cleanup proposal. |
| Yes, not migrated | Do not delete old variables. Create a consumer migration plan first. |
| Unknown | Do not delete old variables. Keep deprecated compatibility variables. |

## Recommendation

Current recommendation: keep old variables as deprecated compatibility variables.

The next safe deliverable is a cleanup proposal that remains blocked until external consumer status is confirmed.

