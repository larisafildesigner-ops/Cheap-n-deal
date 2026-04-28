# Figma Product Screens Binding Audit

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node excluded: `39:162`

## Scope

Read-only audit of all Figma pages outside `Design-system`.

No Figma changes were made.

## Summary

| Check | Result |
| --- | ---: |
| Migration pairs checked | 36 |
| Missing old/new alias pairs | 0 |
| Old variable binding references outside `Design-system` | 207 |
| Nodes with old variable bindings outside `Design-system` | 128 |
| New alias binding references outside `Design-system` | 360 |

Old bindings outside `Design-system` are concentrated on one page:

| Page | Old references |
| --- | ---: |
| `Scenarios` (`31:302`) | 207 |
| blank page `90:342` | 0 |
| `Cart` (`0:1`) | 0 |
| `cover` | 0 |

Old references by node type:

| Node type | References |
| --- | ---: |
| `FRAME` | 103 |
| `TEXT` | 72 |
| `INSTANCE` | 24 |
| `VECTOR` | 8 |

## Old Binding References

| Old variable | New alias | References |
| --- | --- | ---: |
| `text/primary` | `semantic/color/text/primary` | 60 |
| `space/4m` | `primitive/space/16` | 32 |
| `Radius/m` | `primitive/radius/m` | 28 |
| `background/muted` | `semantic/color/bg/muted` | 10 |
| `text/secondary` | `semantic/color/text/secondary` | 9 |
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

## Highest-Impact Cleanup Order

Recommended product-screen migration batches:

1. Text colors:
   - `text/primary` -> `semantic/color/text/primary`
   - `text/secondary` -> `semantic/color/text/secondary`
2. Spacing and radius:
   - `space/4m` -> `primitive/space/16`
   - `Radius/m` -> `primitive/radius/m`
   - `Radius/s` -> `primitive/radius/s`
   - `Radius/pill` -> `primitive/radius/pill`
3. Surfaces and icons:
   - `background/muted` -> `semantic/color/bg/muted`
   - `background/card` -> `semantic/color/bg/card`
   - `icon/default` -> `semantic/color/icon/default`
4. Remaining small groups:
   - `space/8m`, `space/2m`, `space/0m`, `space/1m`, `space/6m`
   - `btn/secondary inverse`, `accent/primary`, `btn/tertiary`, `background/base`

## Recommendation

Do not delete old variables yet.

The audited `Design-system` node is clean, but product screens still depend on old variable names. Migrate product-screen bindings in small batches, then run a final whole-file audit before removing or hiding deprecated variables.
