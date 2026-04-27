# Figma Batch 17 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 17 migrated icon state and favorite icon bindings from old variables to semantic/component aliases.

Migrations:

| Old variable | Old ID | New alias | New ID | Property |
| --- | --- | --- | --- | --- |
| `icon/disabled` | `VariableID:91:647` | `semantic/color/icon/disabled` | `VariableID:190:69` | `strokes` |
| `icon/active` | `VariableID:48:147` | `semantic/color/icon/active` | `VariableID:190:68` | `strokes` |
| `btn/full` | `VariableID:91:750` | `component/icon/favorite/fill/active` | `VariableID:192:58` | `fills`, `strokes` |

## Migration Result

Initial migration script:

- Migrated references: 9
- `icon/disabled`: 4 mutation references
- `icon/active`: 3 mutation references
- `btn/full`: 2 mutation references
- Skipped references: 0
- Errors: 0

Validation found additional instance-level old bindings:

- `icon/active`: 1 remaining reference
- `btn/full`: 6 remaining references

Tail cleanup script:

- Migrated references: 7
- `icon/active`: 1 mutation reference
- `btn/full`: 6 mutation references
- Skipped references: 0
- Errors: 0

Final post-migration validation:

- Remaining `icon/disabled` references inside `Design-system`: 0
- Remaining `icon/active` references inside `Design-system`: 0
- Remaining `btn/full` references inside `Design-system`: 0
- New `semantic/color/icon/disabled` references inside `Design-system`: 4
- New `semantic/color/icon/active` references inside `Design-system`: 10
- New `component/icon/favorite/fill/active` references inside `Design-system`: 8

The additional validation counts come from instance-level bindings that were not covered by the first component-focused pass.

## Validation

Post-change validation:

- Old variables still exist.
- New aliases exist.
- No old icon state/favorite bindings from this batch remain inside the audited `Design-system` node.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No unrelated bindings were migrated.

## Next Recommended Step

Fresh remaining-binding audit inside `Design-system` shows 5 old references across 5 nodes:

- `background/muted`: 4 references on Select fills
- `space/0m`: 1 reference on frame item spacing

Recommended Batch 18:

- `background/muted` -> `semantic/color/bg/muted`
- `space/0m` -> `primitive/space/0`
