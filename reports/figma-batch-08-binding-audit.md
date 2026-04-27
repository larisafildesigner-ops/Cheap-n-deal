# Figma Batch 08 Binding Audit

Date: 2026-04-27
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`
Mode: read-only

## Scope

Batch 08 inspected existing node bindings to old variables and mapped them to the alias variables created in Batches 01-05.

No Figma bindings were changed during this audit.

## Summary

Binding migration inventory:

- Migration pairs checked: 36
- Complete old/new variable pairs: 36
- Missing pairs: 0
- Nodes with old-variable bindings: 177
- Old-variable binding references found: 265

Component structure remained stable:

- Component sets: 9
- Components: 42
- Instances: 41

## Highest-Impact Old Bindings

The largest old-variable binding groups found:

| Old variable | New alias | References | Primary usage |
| --- | --- | ---: | --- |
| `icon/default` | `semantic/color/icon/default` | 53 | Icon/vector strokes |
| `text/secondary` | `semantic/color/text/secondary` | 34 | Text fills for descriptions, secondary labels, tab labels |
| `text/primary` | `semantic/color/text/primary` | 32 | Text fills for labels, values, names |
| `Radius/pill` | `primitive/radius/pill` | 32 | Avatar and pill-like radius bindings |
| `Radius/m` | `primitive/radius/m` | 28 | Button and card radius bindings |
| `space/4m` | `primitive/space/16` | 13 | Button horizontal padding and one frame padding |
| `Radius/s` | `primitive/radius/s` | 12 | Header/right-slot radius bindings |
| `background/base` | `semantic/color/bg/base` | 10 | Field/card/header select fills |
| `Border/invers` | `semantic/color/border/inverse` | 9 | Field/header select strokes |

## Recommended Migration Order

Use small, reversible binding migration batches:

1. Icon stroke bindings:
   - `icon/default` -> `semantic/color/icon/default`
2. Text fill bindings:
   - `text/primary` -> `semantic/color/text/primary`
   - `text/secondary` -> `semantic/color/text/secondary`
3. Radius bindings:
   - `Radius/pill` -> `primitive/radius/pill`
   - `Radius/m` -> `primitive/radius/m`
   - `Radius/s` -> `primitive/radius/s`
4. Field/header surface bindings:
   - `background/base` -> `semantic/color/bg/base`
   - `Border/invers` -> `semantic/color/border/inverse`
5. Spacing bindings:
   - `space/4m` -> `primitive/space/16`
   - then lower-volume `space/*` bindings

Do not migrate all 265 references in one operation. Start with a single high-confidence category, validate visually, then continue.

## Suggested Batch 09

Batch 09 should be a focused binding migration for icon strokes only:

- Old: `icon/default`
- New: `semantic/color/icon/default`
- Expected references from audit: 53
- Primary property path: `strokes.0`

Why this is the best first migration:

- It is high impact.
- It is semantically clear.
- It affects one old variable and one alias variable.
- It is easier to visually validate than a mixed color/radius/spacing batch.

## Validation Checklist For Binding Migration

Before applying:

- Confirm the new alias exists.
- Confirm source variable still exists.
- Save/confirm a Figma version checkpoint.
- Limit the batch to one old variable.

After applying:

- Count migrated references.
- Confirm component set/component/instance counts remain stable.
- Verify no old binding remains for that variable inside the design-system node.
- Visually inspect icons in Select Field, Button, Tabbar, Header, and Icon sections.

## Out Of Scope

- Deleting old variables.
- Migrating all bindings at once.
- Changing visual values.
- Renaming remaining components.
- Text style cleanup.
