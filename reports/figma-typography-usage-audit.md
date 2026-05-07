# Figma Typography Usage Audit

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Scope

Read-only audit after typography style normalization.

No Figma changes were made.

## Summary

| Check | Count |
| --- | ---: |
| Text nodes | 734 |
| Local text styles | 5 |
| Text style spec groups | 46 |

Current local text style usage:

| Style | Usage |
| --- | ---: |
| `typography/heading/h1` | 3 |
| `typography/heading/h2` | 17 |
| `typography/body/s` | 107 |
| `typography/caption` | 0 |
| `typography/button/s` | 10 |

## Page Summary

| Page | Text nodes | Local styled | External/imported styled | Unstyled |
| --- | ---: | ---: | ---: | ---: |
| `Design-system` | 113 | 40 | 25 | 48 |
| `Scenarios` (`31:302`) | 235 | 97 | 20 | 118 |
| `Cart` (`0:1`) | 379 | 0 | 0 | 379 |
| `cover` | 7 | 0 | 0 | 7 |

## Main Findings

- Many text nodes are intentionally documentation-like, especially on `Cart`.
- `Design-system` and `Scenarios` include external/imported text style IDs that do not match the current local style IDs.
- Only exact spec matches should be rebound in a write batch.
- Do not mass-apply local styles to `Cart` documentation text without a separate design decision.

## Highest-Volume Groups

| Spec | Count | Current state | Recommended action |
| --- | ---: | --- | --- |
| Inter Medium 12/18 | 107 | Already local `typography/body/s` | No action |
| Inter Regular 11/16.5 | 67 | Unstyled, mostly `Cart` docs | Do not batch yet |
| Inter Semi Bold 10/15, letter 0.4px | 66 | Unstyled, mostly state labels | Consider new style later |
| Inter Regular 12/140% | 50 | Unstyled labels/values | Candidate for dedicated field style, not exact existing style |
| Inter Regular 12/15 | 46 | Product copy | Candidate for new body/caption style later |
| Inter Semi Bold 13/19.5 | 44 | Documentation labels | Do not batch yet |
| Inter Regular 16/140% | 36 | External/imported style IDs | Audit imported style source before rebinding |
| Inter Regular 10/15 | 35 | Tab labels and product meta | Candidate for caption/tab label style later |

## Candidate Batch 02

Recommended next Figma write batch:

1. Rebind only exact existing-style spec matches that are unstyled or external-styled.
2. Start with `Design-system` text nodes only.
3. Avoid `Cart` documentation text.
4. Do not introduce new text styles until naming is confirmed.

Potential exact-match targets:

- Existing local style specs with candidate unstyled/external nodes, if any are found in a focused re-scan.
- Otherwise create a proposal for missing styles first:
  - `typography/body/m` for Inter Regular 16/140%
  - `typography/body/xs` or `typography/label/s` for Inter Regular 12/140%
  - `typography/caption/strong` for Inter Semi Bold 10/15 with 0.4px letter spacing
  - `typography/tab/label` for Inter Regular 10/15

## Recommendation

Do not mass-rebind all unstyled text.

The safest next step is to create missing typography style proposals for repeated specs, then apply them in small scoped batches.

