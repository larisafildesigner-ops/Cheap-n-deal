# Figma Final Binding Audit

Date: 2026-04-28
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Scope

Final read-only audit after migration batches 09-18.

This audit checks the `Design-system` page only. It does not inspect product screens outside the audited design-system node.

## Structure

| Metric | Count |
| --- | ---: |
| Component sets | 9 |
| Components | 42 |
| Instances | 41 |
| Text nodes | 113 |
| Frames | 87 |

Component sets:

| ID | Name | Variants |
| --- | --- | ---: |
| `98:634` | `Select Field` | 6 |
| `106:1067` | `Input Field` | 6 |
| `91:743` | `Button/Icon` | 3 |
| `91:757` | `Button/Back` | 2 |
| `91:761` | `Button/Secondary` | 3 |
| `91:764` | `Button/Primary` | 3 |
| `56:990` | `Tabbar` | 2 |
| `119:632` | `Header` | 2 |
| `50:1140` | `Icon` | 11 |

## Variables

Variable collections:

| Collection | Mode | Variables |
| --- | --- | ---: |
| `Semantic` | `light` | 82 |
| `Core` | `Mode 1` | 1 |

Migration pairs checked: 36
Missing old/new alias pairs: 0

## Binding Result

| Check | Result |
| --- | ---: |
| Old variable binding references from migration plan | 0 |
| New alias binding references from migration plan | 265 |

The audited `Design-system` node has no remaining old variable bindings from the migration plan.

## New Alias Usage

| Alias | References |
| --- | ---: |
| `semantic/color/border/inverse` | 9 |
| `semantic/color/text/disabled` | 6 |
| `component/button/bg/disabled` | 1 |
| `primitive/radius/s` | 12 |
| `primitive/radius/m` | 28 |
| `primitive/radius/pill` | 32 |
| `primitive/space/0` | 1 |
| `primitive/space/16` | 13 |
| `semantic/color/bg/base` | 10 |
| `semantic/color/bg/muted` | 4 |
| `semantic/color/accent/primary` | 5 |
| `semantic/color/text/primary` | 32 |
| `semantic/color/text/secondary` | 34 |
| `semantic/color/icon/default` | 53 |
| `semantic/color/icon/active` | 3 |
| `semantic/color/icon/disabled` | 4 |
| `semantic/color/state/error` | 8 |
| `component/icon/favorite/fill/active` | 2 |
| `component/button/bg/secondary/default` | 3 |
| `component/button/bg/secondary/on-muted` | 5 |

## Styles

Paint styles: 0
Effect styles: 0
Grid styles: 0

Text styles:

- `H1`
- `H2`
- `B`
- `caption`
- `button`

## Status

Binding migration is complete inside the audited `Design-system` node.

Old variables should remain in the file for now as deprecated compatibility variables. Do not delete them until product screens and any external consumers are audited.

## Recommended Next Step

Run a separate product-screen audit outside `Design-system` before deleting or hiding old variables. The final design-system result does not prove that old variables are unused elsewhere in the file.

