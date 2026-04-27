# Figma Batch 02 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 02 was applied as an additive radius and spacing alias batch. No components, styles, existing variables, or node bindings were deleted or renamed.

Created in local variable collection `Semantic`:

| New variable | ID | Source variable | Source ID | Scopes |
| --- | --- | --- | --- | --- |
| `primitive/radius/s` | `VariableID:187:58` | `Radius/s` | `VariableID:91:639` | `CORNER_RADIUS` |
| `primitive/radius/m` | `VariableID:187:59` | `Radius/m` | `VariableID:91:638` | `CORNER_RADIUS` |
| `primitive/radius/pill` | `VariableID:187:60` | `Radius/pill` | `VariableID:91:651` | `CORNER_RADIUS` |
| `primitive/space/0` | `VariableID:187:61` | `space/0m` | `VariableID:91:547` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/4` | `VariableID:187:62` | `space/1m` | `VariableID:91:538` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/8` | `VariableID:187:63` | `space/2m` | `VariableID:91:539` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/12` | `VariableID:187:64` | `space/3m` | `VariableID:91:541` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/16` | `VariableID:187:65` | `space/4m` | `VariableID:91:543` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/20` | `VariableID:187:66` | `space/5m` | `VariableID:91:544` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/24` | `VariableID:187:67` | `space/6m` | `VariableID:91:545` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/32` | `VariableID:187:68` | `space/8m` | `VariableID:91:548` | `WIDTH_HEIGHT`, `GAP` |
| `primitive/space/40` | `VariableID:187:69` | `space/10m` | `VariableID:91:546` | `WIDTH_HEIGHT`, `GAP` |

## Validation

Post-change validation:

- `Semantic` variable count: 60
- All 12 new aliases exist.
- All 12 source variables still exist.
- New variables are aliases to the existing source variables.
- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.

## Not Changed

- No component sets were renamed.
- No variant axes were renamed.
- No nodes were rebound to new variables.
- No variables were deleted.
- No styles were renamed.

## Next Recommended Step

Review the new aliases in Figma. If they look correct, Batch 03 can focus on one of:

1. Add low-risk semantic color aliases for background, text, icon, and state tokens, or
2. Rename the Header variant axis from `Property 1` to `Variant` after confirming no code automation depends on it.
