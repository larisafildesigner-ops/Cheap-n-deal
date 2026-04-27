# Figma Batch 12 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 12 migrated field/header surface bindings from old variables to semantic aliases.

Migrations:

| Old variable | Old ID | New alias | New ID | Property |
| --- | --- | --- | --- | --- |
| `background/base` | `VariableID:39:395` | `semantic/color/bg/base` | `VariableID:190:58` | `fills` |
| `Border/invers` | `VariableID:103:445` | `semantic/color/border/inverse` | `VariableID:184:58` | `strokes` |

## Migration Result

Initial migration script:

- Migrated references: 19
- `background/base`: 10 references
- `Border/invers`: 9 references
- Skipped references: 0
- Errors: 0

Post-migration validation:

- Remaining `background/base` references inside `Design-system`: 0
- Remaining `Border/invers` references inside `Design-system`: 0
- New `semantic/color/bg/base` references inside `Design-system`: 10
- New `semantic/color/border/inverse` references inside `Design-system`: 9

## Validation

Post-change validation:

- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.
- Old variables still exist.
- New aliases exist.
- No old `background/base` or `Border/invers` bindings remain inside the audited `Design-system` node.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No non-surface bindings were migrated.

## Next Recommended Step

Review field/header surfaces visually in Figma, especially:

- Select Field default and placeholder variants
- Input Field default and placeholder variants
- Header search field
- Card 1 surface

If the visual check is clean, Batch 13 can migrate spacing bindings, starting with:

- `space/4m` -> `primitive/space/16`
