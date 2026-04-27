# Figma Batch 14 Binding Audit

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`
Mode: read-only

## Scope

This audit was run after binding migration Batches 09-13.

No Figma changes were made during this audit.

## Summary

Remaining old-variable binding inventory:

- Migration pairs checked: 27
- Complete old/new variable pairs: 27
- Missing pairs: 0
- Nodes with remaining old-variable bindings: 41
- Remaining old-variable binding references: 42

Component structure remained stable:

- Component sets: 9
- Components: 42
- Instances: 41

## Remaining Old Bindings

| Old variable | New alias | References | Paths | Primary usage |
| --- | --- | ---: | --- | --- |
| `state/error` | `semantic/color/state/error` | 8 | `strokes.0`, `fills.0` | Error field borders and error text |
| `text/disable` | `semantic/color/text/disabled` | 6 | `fills.0` | Disabled/descriptive text |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` | 5 | `fills.0` | Button/Back surfaces |
| `accent/primary` | `semantic/color/accent/primary` | 5 | `fills.0` | Primary button and badges |
| `background/muted` | `semantic/color/bg/muted` | 4 | `fills.0` | Disabled field surfaces |
| `icon/disabled` | `semantic/color/icon/disabled` | 4 | `strokes.0` | Disabled icons |
| `btn/secondary` | `component/button/bg/secondary/default` | 3 | `fills.0` | Secondary button surfaces |
| `icon/active` | `semantic/color/icon/active` | 3 | `strokes.0` | Active icons |
| `btn/full` | `component/icon/favorite/fill/active` | 2 | `fills.0`, `strokes.0` | Favorite icon active fill/stroke |
| `btn/disable` | `component/button/bg/disabled` | 1 | `fills.0` | Disabled primary button surface |
| `space/0m` | `primitive/space/0` | 1 | `itemSpacing` | Single frame spacing |

## Recommended Next Batch

Batch 15 should migrate field state bindings:

- `state/error` -> `semantic/color/state/error`
- `text/disable` -> `semantic/color/text/disabled`

Why:

- They are both field-state semantics.
- They affect small, reviewable areas.
- Together they account for 14 references.
- They are limited to fills/strokes and easy to validate.

## Later Batches

Suggested order after Batch 15:

1. Button surface/content bindings:
   - `btn/secondary inverse`
   - `btn/secondary`
   - `btn/disable`
   - `accent/primary`
2. Icon state bindings:
   - `icon/disabled`
   - `icon/active`
   - `btn/full`
3. Remaining background/spacing:
   - `background/muted`
   - `space/0m`

## Validation Pattern

For each migration batch:

- Migrate only the selected old variables.
- Validate old references equal 0 for those variables.
- Validate new references equal expected count.
- Confirm component set/component/instance counts remain stable.
- Keep old variables until all consumers and file-wide bindings are migrated.
