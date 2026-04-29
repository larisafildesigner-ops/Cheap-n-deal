# Figma Final Whole-File Binding Audit

Date: 2026-04-29
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Scope

Read-only whole-file validation after:

- Design-system migration batches 09-18
- Product-screen migration batches 01-05

## Result

| Scope | Old variable references | Nodes with old bindings |
| --- | ---: | ---: |
| `Design-system` | 0 | 0 |
| Product screens outside `Design-system` | 0 | 0 |
| Whole Figma file | 0 | 0 |

No old variable binding references from the migration plan remain anywhere in the Figma file.

## Product Batch 05 Validation

| Old variable | New alias | Remaining old refs | New refs outside `Design-system` |
| --- | --- | ---: | ---: |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` | 0 | 12 |
| `accent/primary` | `semantic/color/accent/primary` | 0 | 15 |
| `btn/tertiary` | `component/button/content/tertiary/default` | 0 | 3 |
| `background/base` | `semantic/color/bg/base` | 0 | 24 |

## Recommendation

Old variables can now be treated as deprecated compatibility variables at the file level. Do not delete them immediately if any published library consumers, external files, or code automation may still reference them.

Recommended next step:

1. Mark old variable names as deprecated in documentation.
2. Keep aliases stable.
3. Only plan deletion after consumer impact is checked outside this file.

