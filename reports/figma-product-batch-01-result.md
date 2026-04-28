# Figma Product Batch 01 Result

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Applied Changes

Product Batch 01 migrated text color bindings on product screens outside `Design-system`.

Migrations:

| Old variable | New alias | Property |
| --- | --- | --- |
| `text/primary` | `semantic/color/text/primary` | `fills` |
| `text/secondary` | `semantic/color/text/secondary` | `fills` |

## Migration Result

- Migrated references: 69
- `text/primary`: 60 mutation references
- `text/secondary`: 9 mutation references
- Mutated nodes: 69
- Skipped references: 0
- Errors: 0

## Validation

Post-migration validation outside `Design-system`:

| Check | Result |
| --- | ---: |
| Remaining `text/primary` references | 0 |
| Remaining `text/secondary` references | 0 |
| New `semantic/color/text/primary` references | 99 |
| New `semantic/color/text/secondary` references | 59 |
| Remaining old variable references outside `Design-system` | 138 |
| Nodes with old variable bindings outside `Design-system` | 59 |

## Remaining Old Bindings Outside `Design-system`

| Old variable | New alias | References |
| --- | --- | ---: |
| `space/4m` | `primitive/space/16` | 32 |
| `Radius/m` | `primitive/radius/m` | 28 |
| `background/muted` | `semantic/color/bg/muted` | 10 |
| `Radius/s` | `primitive/radius/s` | 8 |
| `Radius/pill` | `primitive/radius/pill` | 8 |
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

Product Batch 02 should migrate spacing and radius bindings:

- `space/4m` -> `primitive/space/16`
- `Radius/m` -> `primitive/radius/m`
- `Radius/s` -> `primitive/radius/s`
- `Radius/pill` -> `primitive/radius/pill`

