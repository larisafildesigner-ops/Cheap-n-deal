# Design System Naming

Status: proposal-only
Source audit: `reports/figma-audit.md`
Figma file key: `GmkQmekrao6tl5mbVFOrGo`
Design-system node: `39:162`

## Goals

- Keep published Figma components stable until consumer impact is known.
- Make component names unique and readable.
- Replace generic variant axes such as `Property 1` with intentional names.
- Move token names toward predictable lowercase slash paths.
- Avoid deleting or renaming existing variables in the first applied batch.

## Component Names

Use readable Pascal/Title Case names for public components:

```text
Button/Primary
Button/Secondary
Button/Icon
Button/Back
Input Field
Select Field
Tab Bar
Header
Icon
Avatar/Large
Avatar/Medium
Card/Default
Card/Compact
```

Rules:

- Public component names should be unique.
- Use `/` only when expressing component family or size/type nesting.
- Avoid snake_case in public component names.
- Avoid numeric names such as `Card 1` and `Card 2` unless the number is part of product vocabulary.
- Internal documentation/layout frames can be less strict, but should not use multiple spellings for the same concept.

## Variant Axes

Preferred axes:

| Axis | Use for | Examples |
| --- | --- | --- |
| `State` | Interaction or validation state | `Default`, `Pressed`, `Disabled`, `Error` |
| `Variant` | Visual or structural variant | `Primary`, `Secondary`, `Search` |
| `Size` | Component size | `Small`, `Medium`, `Large` |
| `Intent` | Semantic meaning | `Info`, `Success`, `Warning`, `Error` |
| `Type` | Icon or content type | `Home`, `Search`, `Heart` |
| `Value Type` | Field value display | `Default`, `Placeholder` |

Rules:

- Do not use `Property 1` in new or renamed component sets.
- Use consistent title case for public variant values.
- Prefer `Pressed` over `active` when describing button press state.
- Prefer `Disabled` over `disabled` in Figma variant values.
- Use `Variant=Search` instead of `Property 1=search` for Header.

## Component Properties

Recommended display names:

| Current pattern | Proposed |
| --- | --- |
| `Has Label#57:0` | `Has Label` |
| `Has Error#72:6` | `Has Error` |
| `Label#280:85` | `Label` |
| `Error#280:88` | `Error` |
| `Description#611:0` | `Description` |
| `Has Description#611:4` | `Has Description` |
| `Value#630:7` | `Value` |
| `Show Text 2#119:3` | `Show Subtitle` |
| `Show text1#119:4` | `Show Title` |
| `Show Right#119:5` | `Show Right Slot` |

Apply these only after confirming that published component property names are not consumed by code or design automation.

## Token Names

Preferred pattern:

```text
<layer>/<type>/<group>/<role>/<state>
```

Examples:

```text
primitive/color/neutral/0
primitive/space/4
primitive/radius/m
semantic/color/bg/base
semantic/color/text/disabled
semantic/color/border/inverse
component/button/bg/primary/default
component/input/border/error
```

Rules:

- Use lowercase token paths.
- Avoid spaces inside token names.
- Prefer adjectives for states: `disabled`, not `disable`.
- Fix typos through aliases first: keep the existing variable until consumers migrate.
- Move ambiguous floats such as `Number` into a named category or retire them after usage audit.

## First Applied Batch Criteria

A Figma batch is safe when it is:

- Additive or typo-only.
- Backed by a registry proposal.
- Limited to a small set of names.
- Easy to review visually.
- Reversible without deleting existing tokens.

Recommended first applied batch:

1. Add registry-backed aliases for duplicate Button sets.
2. Rename only non-public documentation frames if needed.
3. Prepare token aliases for `Border/invers`, `btn/disable`, and `text/disable`.
4. Leave current variables and component sets intact until consumers are checked.
