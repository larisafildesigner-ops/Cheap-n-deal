# Figma Product Batch 05 Result

Date: 2026-04-29
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Applied Changes

Product Batch 05 migrated the final color and component bindings on product screens outside `Design-system`.

Migrations:

| Old variable | New alias | Property |
| --- | --- | --- |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` | `fills` |
| `accent/primary` | `semantic/color/accent/primary` | `fills` |
| `btn/tertiary` | `component/button/content/tertiary/default` | `fills` |
| `background/base` | `semantic/color/bg/base` | `strokes` |

## Migration Result

- Migrated references: 16
- `btn/secondary inverse`: 6 mutation references
- `accent/primary`: 5 mutation references
- `btn/tertiary`: 3 mutation references
- `background/base`: 2 mutation references
- Mutated nodes: 16
- Skipped references: 0
- Errors: 0

## Validation

Post-migration validation outside `Design-system`:

| Check | Result |
| --- | ---: |
| Remaining `btn/secondary inverse` references | 0 |
| Remaining `accent/primary` references | 0 |
| Remaining `btn/tertiary` references | 0 |
| Remaining `background/base` references | 0 |
| New `component/button/bg/secondary/on-muted` references | 12 |
| New `semantic/color/accent/primary` references | 15 |
| New `component/button/content/tertiary/default` references | 3 |
| New `semantic/color/bg/base` references | 24 |
| Remaining old variable references outside `Design-system` | 0 |
| Nodes with old variable bindings outside `Design-system` | 0 |

## Whole-File Validation

Final whole-file validation after Product Batch 05:

| Scope | Old variable references | Nodes with old bindings |
| --- | ---: | ---: |
| `Design-system` | 0 | 0 |
| Product screens outside `Design-system` | 0 | 0 |
| Whole Figma file | 0 | 0 |

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No component sets were renamed.
- No `Design-system` bindings were migrated in this product-screen batch.

## Result

The whole Figma file now has zero old variable binding references from the migration plan.

