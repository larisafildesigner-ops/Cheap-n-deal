# Figma Post-Cleanup Audit

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Scope

Read-only audit after deleting deprecated old variables.

This audit checks:

- deprecated variables from `registry/deprecated-variables.json`;
- replacement variables;
- old binding references;
- replacement binding references;
- replacement alias dependencies.

No Figma changes were made.

## Result

| Check | Result |
| --- | ---: |
| Deprecated variable names checked | 36 |
| Deprecated old variables found | 0 |
| Replacement variable names checked | 36 |
| Replacement variables found | 36 |
| Missing replacement variables | 0 |
| Replacement variables still aliasing other variables | 0 |
| Old binding references from migration plan | 0 |
| Nodes with old binding references | 0 |
| Replacement binding references | 832 |

## Variable Collections

| Collection | Modes | Variables |
| --- | --- | ---: |
| `Semantic` | `light` | 46 |
| `Core` | `Mode 1` | 1 |

## Structure Snapshot

| Page | Nodes | Component sets | Components | Instances |
| --- | ---: | ---: | ---: | ---: |
| `Design-system` | 358 | 9 | 42 | 41 |
| `Scenarios` (`31:302`) | 817 | 0 | 3 | 129 |
| blank page `90:342` | 0 | 0 | 0 | 0 |
| `Cart` (`0:1`) | 1706 | 0 | 0 | 0 |
| `cover` | 9 | 0 | 0 | 0 |

## Top Replacement Binding Counts

| Replacement variable | References |
| --- | ---: |
| `semantic/color/icon/default` | 154 |
| `semantic/color/text/primary` | 131 |
| `semantic/color/text/secondary` | 93 |
| `primitive/radius/m` | 84 |
| `primitive/radius/pill` | 84 |
| `primitive/space/16` | 65 |
| `primitive/radius/s` | 40 |
| `semantic/color/bg/base` | 34 |
| `semantic/color/accent/primary` | 20 |
| `semantic/color/border/inverse` | 19 |
| `component/button/bg/secondary/on-muted` | 17 |
| `semantic/color/bg/muted` | 14 |
| `semantic/color/icon/active` | 10 |
| `primitive/space/0` | 9 |
| `primitive/space/32` | 8 |
| `semantic/color/state/error` | 8 |
| `component/icon/favorite/fill/active` | 8 |
| `semantic/color/text/disabled` | 6 |
| `primitive/space/8` | 6 |
| `semantic/color/bg/card` | 6 |

## Notes

The audit found some bound variable IDs that were not part of the deprecated-variable cleanup list. They appear on properties such as font size, padding, stroke weights, and imported/hash-like variable IDs. They are outside the old-to-new migration plan and were not affected by the cleanup.

## Status

Post-cleanup audit passed.

Deprecated variables from the migration plan are absent, replacement variables are present, and no old binding references remain.

