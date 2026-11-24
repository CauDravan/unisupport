# PA-05 — Proposal Version & Client Baseline

## Objective
Prepare a traceable proposal copy for simulated-client review and define version/approval-record handling without implying actual client approval.

## Corrective changes
1. Created `docs/08-project/sent/UniSupport-Project-Proposal-v1.0.md` as a copy of the maintained Proposal.
2. Created/updated `sent/README.md` to explain folder purpose, version/status, source and record handling.
3. Added `sent/proposal-version-record.md` to track proposal version and simulated review status.
4. Recorded v1.0 dated 24 November 2026 as **Draft for simulated client review**, not approved.

## Proposal and Master Plan formula verification (recalculated)
The `master-plan.xlsx` workbook was recalculated using LibreOffice for formula-result verification.

| Milestone | Target week | Calculated target date | WBS effort | Milestone check |
|---|---:|---|---:|---|
| MS-01 | 9 | 15 January 2027 | 124h | OK |
| MS-02 | 11 | 29 January 2027 | 48h | OK |
| MS-03 | 13 | 12 February 2027 | 33h | OK |
| MS-04 | 15 | 26 February 2027 | 72h | OK |

All four calculated WBS end dates were at or before milestone target dates. Milestone check cells returned `OK`.

## Effort verification
- PM: 68h allocated / 68h baseline
- BA: 78h allocated / 78h baseline
- FE: 79h allocated / 79h baseline
- BE: 79h allocated / 79h baseline
- Planned effort: 304h
- Contingency reserve: 16h
- Total cap: 320h

The Resources sheet role allocations match baseline totals. No formula error values (`#REF!`, `#VALUE!`, `#NAME?`, `#DIV/0!`) were observed in the recalculated workbook sheets reviewed.

## Important limitation
This verifies workbook recalculation and cited milestone/effort formula results. It is not a complete manual audit of every WBS dependency, formula logic, every FR/AC/Test Scenario ID, live GitHub issue links, or client approval. Workbook formulas were recalculated in LibreOffice, not Excel desktop.

## PA-05 status
Corrective changes completed for proposal version and simulated client review record. Actual simulated-client review evidence remains pending until review is conducted and documented.
