# Figma Batch 05 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Context

Product/design clarified the remaining button token roles:

- `btn/primary` had an incorrect mapping for the intended primary button background. The new primary button background alias uses `accent/primary`.
- `btn/secondary` is the default secondary button background.
- `btn/secondary inverse` is the secondary button background for gray surfaces.
- `btn/tertiary` is the tertiary button text/icon color.
- Header variant axis can be renamed from `Property 1` to `Variant`.
- Button component sets can be renamed.

## Applied Changes

Created in local variable collection `Semantic`:

| New variable | ID | Source variable | Source ID | Scopes |
| --- | --- | --- | --- | --- |
| `component/button/bg/primary/default` | `VariableID:195:58` | `accent/primary` | `VariableID:56:1112` | `FRAME_FILL`, `SHAPE_FILL` |
| `component/button/bg/secondary/default` | `VariableID:195:59` | `btn/secondary` | `VariableID:91:634` | `FRAME_FILL`, `SHAPE_FILL` |
| `component/button/bg/secondary/on-muted` | `VariableID:195:60` | `btn/secondary inverse` | `VariableID:91:640` | `FRAME_FILL`, `SHAPE_FILL` |
| `component/button/content/tertiary/default` | `VariableID:195:61` | `btn/tertiary` | `VariableID:93:442` | `SHAPE_FILL`, `TEXT_FILL` |

Renamed component sets:

| Node ID | From | To |
| --- | --- | --- |
| `91:743` | `Button` | `Button/Icon` |
| `91:757` | `Button` | `Button/Back` |
| `91:761` | `btn_secondary` | `Button/Secondary` |
| `91:764` | `btn_primary` | `Button/Primary` |

Renamed Header variants:

| Node ID | From | To |
| --- | --- | --- |
| `48:182` | `Property 1=Default` | `Variant=Default` |
| `119:633` | `Property 1=search` | `Variant=Search` |

## Validation

Post-change validation:

- `Semantic` variable count: 82
- All 4 new button aliases exist.
- Header component set now exposes variant axis `Variant` with options `Default` and `Search`.
- Button component set names match the registry proposals.
- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.

## Not Changed

- No variables were deleted.
- No styles were renamed.
- No nodes were rebound to new variables.
- Button variant axes still need separate cleanup.

## Next Recommended Step

Review the renamed Button component sets and Header variants in Figma. If they look correct, Batch 06 can clean up Button variant axes from `Property 1` to `State` and normalize values such as `active` and `disabled`.
