# Figma Batch 15 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 15 migrated field state bindings from old variables to semantic aliases.

Migrations:

| Old variable | Old ID | New alias | New ID | Property |
| --- | --- | --- | --- | --- |
| `state/error` | `VariableID:91:643` | `semantic/color/state/error` | `VariableID:190:72` | `fills`, `strokes` |
| `text/disable` | `VariableID:106:1206` | `semantic/color/text/disabled` | `VariableID:184:59` | `fills` |

## Migration Result

Initial migration script:

- Migrated references: 14
- `state/error`: 8 references
- `text/disable`: 6 references
- Skipped references: 0
- Errors: 0

Post-migration validation:

- Remaining `state/error` references inside `Design-system`: 0
- Remaining `text/disable` references inside `Design-system`: 0
- New `semantic/color/state/error` references inside `Design-system`: 8
- New `semantic/color/text/disabled` references inside `Design-system`: 6

## Validation

Post-change validation:

- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.
- Old variables still exist.
- New aliases exist.
- No old `state/error` or `text/disable` bindings remain inside the audited `Design-system` node.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No unrelated bindings were migrated.

## Next Recommended Step

Review field error and disabled states visually in Figma, especially:

- Select Field error variants
- Input Field error variants
- Disabled button labels
- Disabled field descriptions

If the visual check is clean, Batch 16 can migrate button surface/content bindings:

- `btn/secondary inverse` -> `component/button/bg/secondary/on-muted`
- `btn/secondary` -> `component/button/bg/secondary/default`
- `btn/disable` -> `component/button/bg/disabled`
- `accent/primary` -> `semantic/color/accent/primary`
