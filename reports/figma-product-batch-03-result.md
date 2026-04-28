# Figma Product Batch 03 Result

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Applied Changes

Product Batch 03 migrated surface and icon bindings on product screens outside `Design-system`.

Migrations:

| Old variable | New alias | Property |
| --- | --- | --- |
| `background/muted` | `semantic/color/bg/muted` | `fills` |
| `background/card` | `semantic/color/bg/card` | `fills` |
| `icon/default` | `semantic/color/icon/default` | `strokes` |

## Migration Result

- Migrated references: 24
- `background/muted`: 10 mutation references
- `background/card`: 6 mutation references
- `icon/default`: 8 mutation references
- Mutated nodes: 24
- Skipped references: 0
- Errors: 0

## Validation

Post-migration validation outside `Design-system`:

| Check | Result |
| --- | ---: |
| Remaining `background/muted` references | 0 |
| Remaining `background/card` references | 0 |
| Remaining `icon/default` references | 0 |
| New `semantic/color/bg/muted` references | 10 |
| New `semantic/color/bg/card` references | 6 |
| New `semantic/color/icon/default` references | 101 |
| Remaining old variable references outside `Design-system` | 38 |
| Nodes with old variable bindings outside `Design-system` | 31 |

## Remaining Old Bindings Outside `Design-system`

| Old variable | New alias | References |
| --- | --- | ---: |
| `space/8m` | `primitive/space/32` | 8 |
| `space/2m` | `primitive/space/8` | 6 |
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

Product Batch 04 should migrate remaining spacing bindings:

- `space/8m` -> `primitive/space/32`
- `space/2m` -> `primitive/space/8`
- `space/0m` -> `primitive/space/0`
- `space/1m` -> `primitive/space/4`
- `space/6m` -> `primitive/space/24`

