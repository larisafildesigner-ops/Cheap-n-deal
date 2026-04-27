# Figma Audit: Cheap-n-deal_design

Date: 2026-04-27
File key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`
Audit mode: read-only. No Figma nodes, styles, or variables were changed.

## Scope

The inspected node `39:162` is a Figma page named `Design-system` in file `Document`.

Top-level frames on the page:

- `Design system`
- `Select Field`
- `Input Field`
- `Buttons`
- `Avatar`
- `Card`
- `Tabbar`
- `Header`
- `Icons`

Inventory from the page:

- Total descendant nodes: 358
- Component sets: 9
- Components: 42
- Instances: 41
- Nodes with style references: 70
- Nodes with variable aliases: 226

## Components And Variants

| Component set | ID | Variants | Variant axes | Notes |
| --- | --- | ---: | --- | --- |
| `Select Field` | `98:634` | 6 | `State`: Default, Error, Disabled; `Value Type`: Default, Placeholder | Has boolean/text props with generated suffixes. |
| `Input Field` | `106:1067` | 6 | `State`: Default, Error, Disabled; `Value Type`: Default, Placeholder | Mirrors Select Field; `Open` default differs. |
| `Button` | `91:743` | 3 | `Property 1`: Default, active, disabled | Generic duplicate name and generic variant axis. |
| `Button` | `91:757` | 2 | `Property 1`: Default, disabled | Duplicate component set name. |
| `btn_secondary` | `91:761` | 3 | `Property 1`: Default, Pressed, disabled | Uses snake_case, mixed variant casing. |
| `btn_primary` | `91:764` | 3 | `Property 1`: Default, Pressed, disabled | Uses snake_case, mixed variant casing. |
| `Tabbar` | `56:990` | 2 | `State`: Default, Chat | Variant name `Chat` reads like a content target, not state. |
| `Header` | `119:632` | 2 | `Property 1`: Default, search | Generic variant axis, lower-case value. |
| `Icon` | `50:1140` | 11 | `Type`: Home, MessageCircle, PlusSquare, ArrowLeft, CircleUser, ImageIcon, Search, Close, Heart, Warning, Loading | Good candidate to normalize as icon names. |

Standalone components discovered outside component sets:

- `Avatar/Large`
- `Avatar/Medium`
- `Card 1`
- `Card 2`

## Styles And Variables

Local styles:

- Paint styles: none
- Effect styles: none
- Grid styles: none
- Text styles:
  - `H1`: Inter Regular, 24px, line-height 30px
  - `H2`: Inter Semi Bold, 16px, line-height 20px
  - `B`: Inter Medium, 12px, line-height 18px
  - `caption`: Inter Regular, 10px, line-height 14px
  - `button`: Inter Regular, 12px, line-height 18px

Local variable collections:

- `Semantic`: 45 variables, mode `light`
- `Core`: 1 variable, mode `Mode 1`

Notable Semantic variables:

- Color: `background/base`, `background/muted`, `background/card`, `background/card additional`, `background/card inverse`, `background/overlay`
- Color: `accent/primary`
- Color: `btn/primary`, `btn/secondary`, `btn/secondary inverse`, `btn/disable`, `btn/full`, `btn/tertiary`
- Color: `icon/default`, `icon/active`, `icon/disabled`
- Color: `text/primary`, `text/secondary`, `text/disable`, `text/inverse`
- Color: `state/success`, `state/warning`, `state/error`, `state/info`
- Color: `Border/default`, `Border/invers`
- Float: `text styles/h1`, `text styles/h2`, `text styles/b`, `text styles/button`, `text styles/caption`
- Float: `space/0m`, `space/1m`, `space/2m`, `space/3m`, `space/4m`, `space/5m`, `space/6m`, `space/8m`, `space/10m`
- Float: `Radius/s`, `Radius/m`, `Radius/pill`
- Float: `icon/thin`
- Float: `Number`

All inspected variables currently use `ALL_SCOPES`.

## Naming Issues

High priority:

- Duplicate component set name `Button` appears twice with different variant structures.
- Several component sets still use generic variant axis `Property 1`.
- Mixed naming styles are present: `Button`, `btn_primary`, `btn_secondary`, `Select Field`, `Input Field`, `Tabbar`, `Card 1`, `Avatar/Large`.
- Variant values mix casing: `Default`, `Pressed`, `active`, `disabled`, `search`.
- Component property names include Figma-generated suffixes such as `Has Label#57:0`, `Error#280:88`, `Show Text 2#119:3`.

Medium priority:

- `B`, `caption`, and `button` text style names mix abbreviation and lower-case labels.
- Token categories mix lower-case and PascalCase: `space/*` vs `Radius/*` vs `Border/*`.
- `Border/invers` appears misspelled and should likely be `border/inverse`.
- `btn/disable` and `text/disable` should likely use adjective form `disabled`.
- `btn/full` is ambiguous; it is unclear whether it means full-width, filled, or a color role.
- `background/card additional` and `btn/secondary inverse` include spaces inside token leaves.
- `Number` is an unclassified float token.
- `Core` collection has generic mode name `Mode 1` and only one variable.

Lower priority:

- Internal layout frames named `.item`, `item`, `Item`, and `Icon-btn` are inconsistent.
- `Tabbar` may be better aligned to product vocabulary as `Tab Bar` or `TabBar`, but changing public component names should be deferred until consumer impact is known.

## Proposed Token Scheme

Suggested direction, not applied:

```text
primitive/color/<palette>/<step>
primitive/space/<step>
primitive/radius/<step>
primitive/font-size/<role>
primitive/line-height/<role>
primitive/stroke-width/<role>

semantic/color/bg/base
semantic/color/bg/muted
semantic/color/bg/card
semantic/color/bg/card-subtle
semantic/color/bg/overlay
semantic/color/text/primary
semantic/color/text/secondary
semantic/color/text/disabled
semantic/color/text/inverse
semantic/color/icon/default
semantic/color/icon/active
semantic/color/icon/disabled
semantic/color/border/default
semantic/color/border/inverse
semantic/color/accent/primary
semantic/color/state/success
semantic/color/state/warning
semantic/color/state/error
semantic/color/state/info

component/button/bg/primary/default
component/button/bg/primary/pressed
component/button/bg/primary/disabled
component/button/bg/secondary/default
component/button/bg/secondary/pressed
component/button/bg/secondary/disabled
component/button/text/primary
component/button/text/secondary

component/input/bg/default
component/input/bg/disabled
component/input/border/default
component/input/border/error
component/input/text/value
component/input/text/placeholder
component/input/text/error
```

Recommended collections:

- `Primitive`: raw color, spacing, radius, typography scale, stroke width
- `Semantic`: product-level aliases with modes such as `light` and later `dark`
- `Component`: component-specific aliases for Button, Input Field, Select Field, Tab Bar, Header, Card, Avatar, Icon

Recommended scopes:

- Color background variables: `FRAME_FILL`, `SHAPE_FILL`
- Text color variables: `TEXT_FILL`
- Border variables: `STROKE_COLOR`
- Spacing variables: `GAP`, `WIDTH_HEIGHT`, `ALL_FILLS` only where appropriate
- Radius variables: corner radius scopes
- Typography size variables: text content scopes only

## First Safe Batch

No Figma changes were applied. The safest first batch should be prepared as proposals only, then reviewed by designers/consumers before any rename or token migration.

Recommended batch 1:

1. Document a canonical component naming convention in repo docs/registry before touching Figma.
2. Add aliases/proposed names in the registry for duplicate and generic names, especially the four button sets.
3. Decide whether `Button` sets represent icon button, back button, primary button, and secondary button before renaming.
4. Normalize future variant axes to `State`, `Variant`, `Size`, `Intent`, `Type`, and `Value Type`.
5. Rename only private/non-published layout frames later, such as `.item`, `item`, and `Icon-btn`, after confirming they are not consumed.
6. Create a token migration plan mapping current variables to proposed names; do not delete current variables in the first applied batch.
7. In a later applied batch, fix typo-only or additive aliases first: `Border/invers` -> `border/inverse`, `btn/disable` -> `button/bg/disabled`, `text/disable` -> `text/disabled`.

## Registry Recommendations

Suggested registry entries should track current Figma IDs and proposed canonical names without mutating Figma:

- `button.icon.favorite`: current set `91:743`, proposed component name `Button/Icon`
- `button.icon.back`: current set `91:757`, proposed component name `Button/Back`
- `button.secondary`: current set `91:761`, proposed component name `Button/Secondary`
- `button.primary`: current set `91:764`, proposed component name `Button/Primary`
- `input-field`: current set `106:1067`, proposed component name `Input Field`
- `select-field`: current set `98:634`, proposed component name `Select Field`
- `tab-bar`: current set `56:990`, proposed component name `Tab Bar`
- `header`: current set `119:632`, proposed component name `Header`
- `icon`: current set `50:1140`, proposed component name `Icon`

## Open Questions

- Are the duplicate `Button` component sets published or already consumed by code?
- Is `Tabbar` intentionally spelled this way in product/code naming?
- Should `Chat` in `Tabbar` be a state, a selected tab, or a content variant?
- Should `Core` remain separate, or should `Border/line` move into `Semantic`/`Primitive`?
- Is `btn/full` a color role, a fill style, or a sizing state?
