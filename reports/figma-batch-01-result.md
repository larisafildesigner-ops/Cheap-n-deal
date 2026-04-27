# Figma Batch 01 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 01 was applied as an additive variable alias batch. No components, styles, existing variables, or node bindings were deleted or renamed.

Created in local variable collection `Semantic`:

| New variable | ID | Source variable | Source ID | Scopes |
| --- | --- | --- | --- | --- |
| `semantic/color/border/inverse` | `VariableID:184:58` | `Border/invers` | `VariableID:103:445` | `STROKE_COLOR` |
| `semantic/color/text/disabled` | `VariableID:184:59` | `text/disable` | `VariableID:106:1206` | `TEXT_FILL` |
| `component/button/bg/disabled` | `VariableID:184:60` | `btn/disable` | `VariableID:91:635` | `FRAME_FILL`, `SHAPE_FILL` |

## Validation

Post-change validation:

- `Semantic` variable count: 48
- Existing source variables still exist:
  - `Border/invers`
  - `text/disable`
  - `btn/disable`
- New variables are aliases to the existing source variables.
- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.

## Not Changed

- No Button component sets were renamed.
- Header variant axis `Property 1` was not renamed.
- No nodes were rebound to new variables.
- No variables were deleted.
- No styles were renamed.

## Next Recommended Step

Review the new aliases in Figma. If they look correct, Batch 02 can either:

1. Add remaining low-risk aliases for radius casing, or
2. Rename the Header variant axis from `Property 1` to `Variant` after confirming no code automation depends on it.
