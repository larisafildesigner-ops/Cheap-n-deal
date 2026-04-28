# Figma Product Batch 02 Result

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Applied Changes

Product Batch 02 migrated spacing and radius bindings on product screens outside `Design-system`.

Migrations:

| Old variable | New alias | Property group |
| --- | --- | --- |
| `space/4m` | `primitive/space/16` | spacing, padding |
| `Radius/m` | `primitive/radius/m` | corner radius |
| `Radius/s` | `primitive/radius/s` | corner radius |
| `Radius/pill` | `primitive/radius/pill` | corner radius |

## Migration Result

- Migrated references: 76
- `space/4m`: 32 mutation references
- `Radius/m`: 28 mutation references
- `Radius/s`: 8 mutation references
- `Radius/pill`: 8 mutation references
- Mutated nodes: 26
- Skipped references: 0
- Errors: 0

## Validation

Post-migration validation outside `Design-system`:

| Check | Result |
| --- | ---: |
| Remaining `space/4m` references | 0 |
| Remaining `Radius/m` references | 0 |
| Remaining `Radius/s` references | 0 |
| Remaining `Radius/pill` references | 0 |
| New `primitive/space/16` references | 52 |
| New `primitive/radius/m` references | 56 |
| New `primitive/radius/s` references | 28 |
| New `primitive/radius/pill` references | 52 |
| Remaining old variable references outside `Design-system` | 62 |
| Nodes with old variable bindings outside `Design-system` | 46 |

## Remaining Old Bindings Outside `Design-system`

| Old variable | New alias | References |
| --- | --- | ---: |
| `background/muted` | `semantic/color/bg/muted` | 10 |
| `space/8m` | `primitive/space/32` | 8 |
| `icon/default` | `semantic/color/icon/default` | 8 |
| `space/2m` | `primitive/space/8` | 6 |
| `background/card` | `semantic/color/bg/card` | 6 |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` | 6 |
| `space/0m` | `primitive/space/0` | 5 |
| `accent/primary` | `semantic/color/accent/primary` | 5 |
| `btn/tertiary` | `component/button/content/tertiary/default` | 3 |
| `space/1m` | `primitive/space/4` | 2 |
| `background/base` | `semantic/color/bg/base` | 2 |
| `space/6m` | `primitive/space/24` | 1 |

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No `Design-system` bindings were migrated in this product-screen batch.

## Next Recommended Step

Product Batch 03 should migrate surface and icon bindings:

- `background/muted` -> `semantic/color/bg/muted`
- `background/card` -> `semantic/color/bg/card`
- `icon/default` -> `semantic/color/icon/default`

