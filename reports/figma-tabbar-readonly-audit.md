# Figma Tabbar Read-Only Audit

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Component set: `Tabbar` (`56:990`)

## Scope

Initial read-only inspection of the `Tabbar` component set.

No Figma changes were made during the initial inspection. A later applied follow-up batch is recorded below.

## Current Structure

| Item | Value |
| --- | --- |
| Component set name | `Tabbar` |
| Component set ID | `56:990` |
| Current variant axis | `State` |
| Current variants | `Default`, `Chat` |
| Boolean property | `Show badge` |

## Findings

- `State=Default` is a regular bottom navigation layout with labels: `Home`, `Favorite`, `Sell`, `Messages`, `Profile`.
- `State=Chat` includes a `Message...` entry row and compact tab labels.
- `Chat` does not describe interaction state. It describes a layout/content mode for the tab bar.
- The current axis name `State` is therefore semantically misleading.

## Decision

Treat `Chat` as a Tabbar layout/content variant, not as a component state.

Keep the Figma component set name unchanged for now because the component library is local and the broader component policy favors stability.

## Original Recommended Figma Batch

Only after approval:

1. Rename Tabbar variant axis from `State` to `Variant`.
2. Keep variant values as `Default` and `Chat` unless product vocabulary prefers a more explicit value.
3. Optionally update the Figma component description to say: `Bottom tab bar with default navigation and chat/message entry variants.`
4. Do not rename the public component set from `Tabbar` to `Tab Bar` in the same batch.

## Registry Status

The decision is recorded in `registry/components.json`.

## Applied Follow-Up Batch

Date: 2026-05-07

Applied Figma changes:

- Renamed Tabbar variant axis from `State` to `Variant`.
- Kept variant values `Default` and `Chat`.
- Updated component description to `Bottom tab bar with default navigation and chat/message entry variants.`
- Kept public component set name as `Tabbar`.

No structure, layout, values, or child nodes were changed.
