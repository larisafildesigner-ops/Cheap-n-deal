# Figma Batch 06 Result

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Applied Changes

Batch 06 normalized Button variant axes and state values.

Renamed Button variants:

| Component set | Node ID | From | To |
| --- | --- | --- | --- |
| `Button/Icon` | `91:742` | `Property 1=Default` | `State=Default` |
| `Button/Icon` | `91:744` | `Property 1=active` | `State=Pressed` |
| `Button/Icon` | `91:754` | `Property 1=disabled` | `State=Disabled` |
| `Button/Back` | `91:690` | `Property 1=Default` | `State=Default` |
| `Button/Back` | `91:758` | `Property 1=disabled` | `State=Disabled` |
| `Button/Secondary` | `91:738` | `Property 1=Default` | `State=Default` |
| `Button/Secondary` | `110:1358` | `Property 1=Pressed` | `State=Pressed` |
| `Button/Secondary` | `91:762` | `Property 1=disabled` | `State=Disabled` |
| `Button/Primary` | `91:733` | `Property 1=Default` | `State=Default` |
| `Button/Primary` | `110:1360` | `Property 1=Pressed` | `State=Pressed` |
| `Button/Primary` | `91:765` | `Property 1=disabled` | `State=Disabled` |

## Validation

Post-change validation:

- `Button/Icon` exposes `State` with `Default`, `Pressed`, `Disabled`.
- `Button/Back` exposes `State` with `Default`, `Disabled`.
- `Button/Secondary` exposes `State` with `Default`, `Pressed`, `Disabled`.
- `Button/Primary` exposes `State` with `Default`, `Pressed`, `Disabled`.
- No Button variants still use `Property 1`.
- No Button variants still use lowercase `active` or `disabled`.
- Component set count remains 9.
- Component count remains 42.
- Instance count remains 41.

## Not Changed

- No variables were created or deleted.
- No styles were renamed.
- No nodes were rebound to variables.
- Non-Button component sets were not changed.

## Next Recommended Step

Review Button variants in Figma. If they look correct, Batch 07 can inspect remaining component/property naming issues in `Select Field`, `Input Field`, and `Header` component properties.
