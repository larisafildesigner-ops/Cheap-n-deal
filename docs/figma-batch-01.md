# Figma Batch 01 Plan

Status: proposal-only
Source audit: `reports/figma-audit.md`
Registry inputs:

- `registry/components.json`
- `registry/tokens.json`
- `docs/design-system-naming.md`

## Goal

Prepare the first low-risk Figma cleanup batch for `Cheap-n-deal_design` without breaking published components, code mappings, or existing variables.

This plan intentionally avoids destructive edits:

- Do not delete variables.
- Do not delete styles.
- Do not detach or recreate components.
- Do not rename published component sets until consumer impact is checked.
- Do not change visual values in the first batch.

## Batch Scope

Batch 01 should focus on reviewable naming and documentation alignment.

Recommended items:

| Area | Current | Proposed | Risk | Action |
| --- | --- | --- | --- | --- |
| Token typo | `Border/invers` | `semantic/color/border/inverse` | Low | Add alias first; keep current variable. |
| Token grammar | `text/disable` | `semantic/color/text/disabled` | Low | Add alias first; keep current variable. |
| Token grammar | `btn/disable` | `component/button/bg/disabled` | Low | Add alias first; keep current variable. |
| Token casing | `Radius/s`, `Radius/m`, `Radius/pill` | `primitive/radius/s`, `primitive/radius/m`, `primitive/radius/pill` | Low | Add aliases first. |
| Header axis | `Property 1` | `Variant` | Low | Rename only after confirming no code automation depends on axis name. |
| Button duplicate names | `Button`, `Button`, `btn_primary`, `btn_secondary` | `Button/Icon`, `Button/Back`, `Button/Primary`, `Button/Secondary` | Medium | Confirm meaning before renaming in Figma. |

## Do First

1. Confirm that the four Button component sets are not consumed by Code Connect, generated code, or handoff docs by their current Figma names.
2. Confirm whether `Tabbar` is intentional product spelling.
3. Confirm whether `Tabbar` variant value `Chat` means selected tab, screen type, or state.
4. Confirm whether `btn/full` means filled, full-width, or a color role.
5. Confirm whether `Core/Border/line` should remain in `Core` or move into `Semantic`.

## Candidate Figma Changes After Confirmation

Apply these as a small, visible batch:

1. Rename obvious typo/grammar token aliases by adding new variables:
   - `semantic/color/border/inverse`
   - `semantic/color/text/disabled`
   - `component/button/bg/disabled`
2. Bind no nodes yet; keep existing bindings stable.
3. Rename only the Header variant axis from `Property 1` to `Variant` if no consumers depend on it.
4. Leave Button component set names unchanged until their purpose is confirmed.

## Validation Checklist

Before applying:

- Registry files are committed.
- Figma file has a saved version checkpoint.
- Current component IDs are still present.
- No one is actively editing the same Figma component sets.

After applying:

- Component set count remains 9.
- Component count remains 42.
- No components are detached.
- Existing variables still exist.
- New alias variables resolve to the same values as their current counterparts.
- Screens using Button, Header, Input Field, and Select Field still render without visible changes.

## Rollback Plan

If any issue appears:

1. Undo the Figma operation immediately with Figma undo.
2. If undo is unavailable, restore from Figma version history.
3. Do not delete current variables as a rollback mechanism; preserve old names until all consumers migrate.

## Out Of Scope For Batch 01

- Dark mode.
- Full token hierarchy rebuild.
- Deleting or moving existing variables.
- Rebinding all nodes to new aliases.
- Renaming all Button component sets.
- Creating Code Connect files.
- Component visual redesign.
