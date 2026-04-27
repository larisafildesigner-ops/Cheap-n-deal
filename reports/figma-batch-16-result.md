# Figma Batch 16 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 16 migrated button surface/accent fill bindings from old variables to semantic/component aliases.

Migrations:

| Old variable | Old ID | New alias | New ID | Property |
| --- | --- | --- | --- | --- |
| `btn/secondary inverse` | `VariableID:91:640` | `component/button/bg/secondary/on-muted` | `VariableID:195:60` | `fills` |
| `btn/secondary` | `VariableID:91:634` | `component/button/bg/secondary/default` | `VariableID:195:59` | `fills` |
| `btn/disable` | `VariableID:91:635` | `component/button/bg/disabled` | `VariableID:184:60` | `fills` |
| `accent/primary` | `VariableID:56:1112` | `semantic/color/accent/primary` | `VariableID:190:63` | `fills` |

## Migration Result

Initial migration script:

- Migrated references: 10
- `btn/secondary inverse`: 2 mutation references
- `btn/secondary`: 3 mutation references
- `btn/disable`: 1 mutation reference
- `accent/primary`: 4 mutation references
- Skipped references: 0
- Errors: 0

Post-migration validation:

- Remaining `btn/secondary inverse` references inside `Design-system`: 0
- Remaining `btn/secondary` references inside `Design-system`: 0
- Remaining `btn/disable` references inside `Design-system`: 0
- Remaining `accent/primary` references inside `Design-system`: 0
- New `component/button/bg/secondary/on-muted` references inside `Design-system`: 5
- New `component/button/bg/secondary/default` references inside `Design-system`: 3
- New `component/button/bg/disabled` references inside `Design-system`: 1
- New `semantic/color/accent/primary` references inside `Design-system`: 5

Instance-level bindings resolved to the aliases after component-level updates, so validation counts for `btn/secondary inverse` and `accent/primary` are higher than the direct mutation counts.

## Validation

Post-change validation:

- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.
- Old variables still exist.
- New aliases exist.
- No old button/accent bindings from this batch remain inside the audited `Design-system` node.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No unrelated bindings were migrated.

## Next Recommended Step

Review button and accent fills visually in Figma, especially:

- Button/Back variants
- Button/Secondary variants
- Button/Primary variants
- Badge/accent fills

If the visual check is clean, Batch 17 can migrate icon state bindings:

- `icon/disabled` -> `semantic/color/icon/disabled`
- `icon/active` -> `semantic/color/icon/active`
- `btn/full` -> `component/icon/favorite/fill/active`
