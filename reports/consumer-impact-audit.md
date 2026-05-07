# Consumer Impact Audit

Date: 2026-05-07
Figma file key: `GmkQmekrao6tl5mbVFOrGo`

## Scope

Local repository audit after the Figma whole-file binding migration.

Checked local files for deprecated variable names from `registry/deprecated-variables.json`.

## Result

| Area | Status |
| --- | --- |
| Figma whole-file bindings | Complete: 0 old variable binding references |
| Local registry/docs/reports | Deprecated names appear only as migration history, replacement mapping, and cleanup documentation |
| Local production code | No production code files found in this audit scope |
| External Figma consumers | Not checked |
| Published library consumers | Not checked |
| Automation/token export consumers | Not checked |

## Local References

Deprecated token names still appear in:

- `registry/deprecated-variables.json`
- `registry/binding-migration-plan.json`
- `registry/tokens.json`
- `docs/deprecated-variables-cleanup.md`
- `docs/design-system-naming.md`
- historical reports in `reports/`

These references are expected and should remain. They document the migration and old-to-new replacement mapping.

## Interpretation

The local repository does not show an active implementation dependency on deprecated variable names. This repository is documentation/registry-heavy; no application source code was found in the audited local scope.

The remaining risk is outside this repository:

- published Figma library consumers;
- duplicated/external Figma files;
- design-to-code automation;
- token export scripts outside this repo;
- handoff docs stored elsewhere.

## Cleanup Gate

Old variables should not be deleted, hidden, or renamed in Figma until these checks are complete:

1. Confirm whether `Cheap-n-deal_design` is published as a Figma library.
2. Identify downstream Figma files that use the library.
3. Open downstream files and accept library updates.
4. Search downstream files for old variable references.
5. Check external automation and token export scripts.
6. Communicate a deprecation window.
7. Run a final whole-file audit immediately before cleanup.
8. Perform deletion/hiding as a separate reviewed cleanup batch.

## Recommendation

Keep old variables as deprecated compatibility variables for now.

Next safe step: collect the list of known downstream Figma files or confirm that there are no external library consumers. If there are no consumers, prepare a cleanup proposal, but still do not delete variables in the same step.

