# Figma Old Variables Cleanup Result

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Applied Changes

Deprecated old variables were deleted from Figma after explicit user approval.

The user requested deletion without an additional pre-cleanup audit.

## Safety Step Applied During Deletion

Before deleting old variables, replacement variables were materialized where they were aliases to old variables.

This prevented replacement variables from depending on variables being removed.

| Check | Result |
| --- | ---: |
| Replacement values materialized | 36 |
| Deprecated variables deleted | 36 |
| Missing deprecated variables | 0 |
| Delete errors | 0 |

## Deleted Variables

| Old variable | Replacement |
| --- | --- |
| `Border/invers` | `semantic/color/border/inverse` |
| `text/disable` | `semantic/color/text/disabled` |
| `btn/disable` | `component/button/bg/disabled` |
| `Radius/s` | `primitive/radius/s` |
| `Radius/m` | `primitive/radius/m` |
| `Radius/pill` | `primitive/radius/pill` |
| `space/0m` | `primitive/space/0` |
| `space/1m` | `primitive/space/4` |
| `space/2m` | `primitive/space/8` |
| `space/3m` | `primitive/space/12` |
| `space/4m` | `primitive/space/16` |
| `space/5m` | `primitive/space/20` |
| `space/6m` | `primitive/space/24` |
| `space/8m` | `primitive/space/32` |
| `space/10m` | `primitive/space/40` |
| `background/base` | `semantic/color/bg/base` |
| `background/muted` | `semantic/color/bg/muted` |
| `background/card` | `semantic/color/bg/card` |
| `background/card inverse` | `semantic/color/bg/card-inverse` |
| `background/overlay` | `semantic/color/bg/overlay` |
| `accent/primary` | `semantic/color/accent/primary` |
| `text/primary` | `semantic/color/text/primary` |
| `text/secondary` | `semantic/color/text/secondary` |
| `text/inverse` | `semantic/color/text/inverse` |
| `icon/default` | `semantic/color/icon/default` |
| `icon/active` | `semantic/color/icon/active` |
| `icon/disabled` | `semantic/color/icon/disabled` |
| `state/success` | `semantic/color/state/success` |
| `state/warning` | `semantic/color/state/warning` |
| `state/error` | `semantic/color/state/error` |
| `state/info` | `semantic/color/state/info` |
| `Border/default` | `semantic/color/border/default` |
| `btn/full` | `component/icon/favorite/fill/active` |
| `btn/secondary` | `component/button/bg/secondary/default` |
| `btn/secondary inverse` | `component/button/bg/secondary/on-muted` |
| `btn/tertiary` | `component/button/content/tertiary/default` |

## Not Changed

- No styles were renamed.
- No component sets were renamed.
- No component variants were renamed.
- No new variables were created.
- Current semantic/component aliases were not renamed.

## Follow-Up Recommendation

Run a post-cleanup whole-file audit if visual or token regressions are suspected.

