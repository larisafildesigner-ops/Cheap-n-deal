# Figma Product Batch 04 Result

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Applied Changes

Product Batch 04 migrated the remaining spacing bindings on product screens outside `Design-system`.

Migrations:

| Old variable | New alias | Property group |
| --- | --- | --- |
| `space/8m` | `primitive/space/32` | spacing, padding |
| `space/2m` | `primitive/space/8` | spacing, padding |
| `space/0m` | `primitive/space/0` | spacing |
| `space/1m` | `primitive/space/4` | spacing |
| `space/6m` | `primitive/space/24` | spacing |

## Migration Result

- Migrated references: 22
- `space/8m`: 8 mutation references
- `space/2m`: 6 mutation references
- `space/0m`: 5 mutation references
- `space/1m`: 2 mutation references
- `space/6m`: 1 mutation reference
- Mutated nodes: 15
- Skipped references: 0
- Errors: 0

## Validation

Post-migration validation outside `Design-system`:

| Check | Result |
| --- | ---: |
| Remaining `space/8m` references | 0 |
| Remaining `space/2m` references | 0 |
| Remaining `space/0m` references | 0 |
| Remaining `space/1m` references | 0 |
| Remaining `space/6m` references | 0 |
| New `primitive/space/32` references | 8 |
| New `primitive/space/8` references | 6 |
| New `primitive/space/0` references | 8 |
| New `primitive/space/4` references | 2 |
| New `primitive/space/24` references | 1 |
| Remaining old variable references outside `Design-system` | 16 |
| Nodes with old variable bindings outside `Design-system` | 16 |

## Remaining Old Bindings Outside `Design-system`

| Old variable | New alias | References |
| --- | --- | ---: |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` | 6 |
| `accent/primary` | `semantic/color/accent/primary` | 5 |
| `btn/tertiary` | `component/button/content/tertiary/default` | 3 |
| `background/base` | `semantic/color/bg/base` | 2 |

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No `Design-system` bindings were migrated in this product-screen batch.

## Next Recommended Step

Product Batch 05 should migrate the final color/component binding groups:

- `btn/secondary inverse` -> `component/button/bg/secondary/on-muted`
- `accent/primary` -> `semantic/color/accent/primary`
- `btn/tertiary` -> `component/button/content/tertiary/default`
- `background/base` -> `semantic/color/bg/base`

