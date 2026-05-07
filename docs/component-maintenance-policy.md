# Component Maintenance Policy

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Decision

Keep the current public component set stable.

The design system currently has 9 audited component sets with descriptions applied. No new component sets are planned until a reusable product pattern is confirmed.

## Safe Updates

- Update component descriptions and usage guidance.
- Fix confirmed typos in descriptions or documentation.
- Update token bindings to approved semantic/component aliases.
- Normalize variant axes or values when the meaning is already confirmed.
- Rename generated boolean/text properties only when the public meaning is clear.

## Requires Separate Decision

- Add a new public component set.
- Delete or detach an existing public component set.
- Change component structure or interaction behavior.
- Rename a public component family with medium/high consumer risk.
- Merge component sets that may represent different product roles.

## Deferred Questions

- Confirm whether `Tabbar` should remain spelled as `Tabbar` or become `Tab Bar`.
- Review Select Field and Input Field generated property suffixes before cleanup.
- Map Icon variants to code icon names after implementation consumers exist.

## Tabbar Decision

`Tabbar` variant `Chat` is a layout/content variant with a message entry row, not an interaction state.

Recommended future Figma batch:

1. Rename the Tabbar variant axis from `State` to `Variant`.
2. Keep variant values as `Default` and `Chat` unless product vocabulary prefers a more explicit value.
3. Keep the public component set name `Tabbar` unchanged until a separate naming decision is approved.

## Next Safe Batch

The next safe component batch should be documentation-first:

1. Keep component set names unchanged.
2. Add or refine usage notes in registry/docs only.
3. Prepare a focused Figma batch only for confirmed property label cleanup.
4. Avoid creating, deleting, merging, or structurally changing components.
