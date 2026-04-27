# Figma Batch 11 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 11 migrated radius bindings from old radius variables to primitive aliases.

Migrations:

| Old variable | Old ID | New alias | New ID | Property |
| --- | --- | --- | --- | --- |
| `Radius/pill` | `VariableID:91:651` | `primitive/radius/pill` | `VariableID:187:60` | corner radius |
| `Radius/m` | `VariableID:91:638` | `primitive/radius/m` | `VariableID:187:59` | corner radius |
| `Radius/s` | `VariableID:91:639` | `primitive/radius/s` | `VariableID:187:58` | corner radius |

## Migration Result

Initial migration script:

- Migrated references: 52
- `Radius/pill`: 12 mutation references
- `Radius/m`: 28 mutation references
- `Radius/s`: 12 mutation references
- Skipped references: 0
- Errors: 0

Post-migration validation:

- Remaining `Radius/pill` references inside `Design-system`: 0
- Remaining `Radius/m` references inside `Design-system`: 0
- Remaining `Radius/s` references inside `Design-system`: 0
- New `primitive/radius/pill` references inside `Design-system`: 32
- New `primitive/radius/m` references inside `Design-system`: 28
- New `primitive/radius/s` references inside `Design-system`: 12

The validation count for `primitive/radius/pill` is higher than the initial mutation count because instance-level bindings resolved to the alias after component/frame-level radius updates.

## Validation

Post-change validation:

- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.
- Old variables still exist.
- New aliases exist.
- No old `Radius/*` bindings remain inside the audited `Design-system` node.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No non-radius bindings were migrated.

## Next Recommended Step

Review radius-sensitive components visually in Figma, especially:

- Button variants
- Avatar components
- Card 2
- Header right slot

If the visual check is clean, Batch 12 can migrate field/header surface bindings:

- `background/base` -> `semantic/color/bg/base`
- `Border/invers` -> `semantic/color/border/inverse`
