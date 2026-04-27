# Figma Final Audit After Batches 01-07

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Scope

This is a read-only final audit after Batches 01-07. No additional Figma changes were made during this final audit.

## Summary

Final inventory:

- Total descendant nodes: 358
- Component sets: 9
- Components: 42
- Instances: 41
- Text styles: 5
- Paint styles: 0
- Effect styles: 0
- Grid styles: 0

Variable collections:

- `Semantic`: 82 variables, mode `light`
- `Core`: 1 variable, mode `Mode 1`

## Applied Batch Outcomes

Completed batches:

- Batch 01: added typo/grammar aliases for border inverse, text disabled, and button disabled background.
- Batch 02: added radius and spacing aliases.
- Batch 03: added semantic background, accent, text, icon, state, and border aliases.
- Batch 04: clarified `btn/full` and added favorite icon fill alias.
- Batch 05: added button token aliases, renamed Button component sets, and normalized Header variant naming.
- Batch 06: normalized Button variant axes and state values.
- Batch 07: cleaned Header component property display names.

Total additive alias variables created: 37.

No variables were deleted. No node bindings were migrated. Counts remained stable after every batch.

## Component Sets

| Component set | ID | Variants / axes | Status |
| --- | --- | --- | --- |
| `Select Field` | `98:634` | `State`, `Value Type` | Stable. Visible property names are already clean. |
| `Input Field` | `106:1067` | `State`, `Value Type` | Stable. Visible property names are already clean. |
| `Button/Icon` | `91:743` | `State`: Default, Pressed, Disabled | Renamed and normalized. |
| `Button/Back` | `91:757` | `State`: Default, Disabled | Renamed and normalized. |
| `Button/Secondary` | `91:761` | `State`: Default, Pressed, Disabled | Renamed and normalized. |
| `Button/Primary` | `91:764` | `State`: Default, Pressed, Disabled | Renamed and normalized. |
| `Tabbar` | `56:990` | `State`: Default, Chat | Still needs product decision. |
| `Header` | `119:632` | `Variant`: Default, Search | Normalized. Properties cleaned. |
| `Icon` | `50:1140` | `Type` | Stable. |

## Header Properties

Header now exposes:

- `Show Subtitle#119:3`
- `Show Title#119:4`
- `Show Right Slot#119:5`
- `Variant`

## Select/Input Property Note

`Select Field` and `Input Field` still show API keys like:

- `Has Label#57:0`
- `Label#280:85`
- `Value#630:7`

These suffixes are Figma's internal unique IDs for non-variant component properties. Their visible display names are already clean (`Has Label`, `Label`, `Value`). The Plugin API rejects renaming a property to the same visible name, so these were intentionally left unchanged.

## Token State

The `Semantic` collection now contains both original variables and additive aliases.

Key alias groups now exist:

- `semantic/color/bg/*`
- `semantic/color/accent/primary`
- `semantic/color/text/*`
- `semantic/color/icon/*`
- `semantic/color/state/*`
- `semantic/color/border/*`
- `primitive/space/*`
- `primitive/radius/*`
- `component/button/bg/*`
- `component/button/content/tertiary/default`
- `component/icon/favorite/fill/active`

Original variables remain in place and still use their original names and scopes. This is intentional until binding migration is planned.

## Remaining Issues

High confidence:

- `Tabbar` naming should be reviewed. Decide whether product vocabulary prefers `Tabbar`, `Tab Bar`, or `TabBar`.
- `Tabbar` variant `State=Chat` may be semantically odd. It may represent selected tab/content rather than component state.
- `Card 1` and `Card 2` are still numeric standalone component names.
- Text styles still use mixed naming: `H1`, `H2`, `B`, `caption`, `button`.
- Original variables still use `ALL_SCOPES`.
- Original variables remain alongside aliases, so future users may see both naming systems until migration is complete.

Lower confidence / needs usage audit:

- `Number` remains an unclassified float token.
- `Core/Border/line` remains separate from `Semantic`.
- `background/card additional` still needs product/design meaning before aliasing.
- `btn/primary` still exists but is not the recommended source for the new primary button background alias; `component/button/bg/primary/default` aliases to `accent/primary` by design decision.

## Recommended Next Steps

1. Review the Figma variables panel to confirm alias groups are understandable.
2. Decide whether to begin node binding migration to aliases, starting with the lowest-risk Button tokens.
3. Decide whether to rename `Tabbar` and clarify `State=Chat`.
4. Decide whether to normalize text style names.
5. Keep old variables until consumers and bindings have been migrated.

## Suggested Batch 08 Options

Option A: read-only binding audit.

- Identify which nodes are bound to old variables.
- Produce a migration list from old variable IDs to alias variable IDs.
- Do not change bindings yet.

Option B: Tabbar naming cleanup.

- Confirm spelling and semantics first.
- Rename only after product decision.

Option C: text style naming cleanup.

- Propose text style names such as `Typography/H1`, `Typography/H2`, `Typography/Body`, `Typography/Caption`, `Typography/Button`.
- Apply only after confirming downstream usage.
