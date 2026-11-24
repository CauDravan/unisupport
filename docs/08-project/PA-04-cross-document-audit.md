# PA-04 — Cross-document Alignment Audit

## Purpose
Rà soát và xử lý các điểm đồng bộ giữa Project Proposal, Assumptions, Constraints, Quotation, Master Plan, WBS, Requirements, Acceptance/Testing, Quality, Risk, RACI và Governance.

## Source-of-truth rules
- `master-plan.xlsx`: official source for WBS, milestone dates, detailed schedule/dependencies, effort/resource allocation and Change Log.
- Functional Requirements: authoritative source for requirement-level Acceptance Criteria.
- `master-plan.xlsx` sheet `Milestones`: milestone-level acceptance summary and regression/verification reference.
- `quotation.xlsx`: cost estimate and pricing breakdown; `assumptions.md` records the rationale for pricing assumption A-01.
- GitHub Issues/Milestones: execution tracking; must align with approved WBS and MS IDs/dates.

## Corrective changes made in PA-04
1. **WBS Markdown:** reduced `wbs.md` to a structural explanation and explicit source-of-truth pointer. Removed duplicated detailed task tables so the Markdown no longer maintains a parallel WBS/schedule/effort baseline.
2. **Risk Register:** added a Status column and initial `Open` status to R01–R07, so risk monitoring has a status field in the register itself.

## Alignment checks and remaining verification
| Area | Audit outcome | Status |
|---|---|---|
| Proposal / Modules | Proposal describes M01–M04 and the prototype/non-production boundary. | Aligned in reviewed text |
| Proposal / Milestones | MS-01 to MS-04 dates are stated as 15 Jan, 29 Jan, 12 Feb, 26 Feb 2027. Excel milestones are week 9/11/13/15; detailed formula/date validation should be recalculated in Excel. | Needs formula recalculation/validation |
| Proposal / Acceptance | Proposal points to FR and Master Plan Milestones rather than maintaining a separate detailed AC set. | Aligned in reviewed text |
| Assumptions / Quotation | A-01 records estimate basis, 304h baseline and separately managed 16h reserve. | Aligned in reviewed text; formulas not recalculated |
| Constraints / Master Plan | Constraints points to the proposed 15-week, 4-milestone plan and the 320h cap. | Aligned in reviewed text |
| WBS / Master Plan | Excel is declared the source; Markdown now explains the structure only. | Corrected |
| Risk Register | R01–R07 have owner, response and now Status. | Corrected |
| FR / AC / Test Scenarios | Detailed crosswalk and scenario coverage require manual ID-level verification; not certified in this PA-04 pass. | Pending |
| Quality / Milestones | Quality criteria and milestone acceptance are broadly referenced; full release criteria and defect severity/response threshold review remains separate. | Partial |
| Governance / GitHub | Governance defines monitoring and baseline changes, but actual issue/parent task/date/owner links must be checked in live GitHub. | Pending live verification |
| Proposal sent-to-client version | `docs/08-project/sent/` requires verification of whether an approved client version exists; this is treated separately in PA-05. | Pending PA-05 |

## PA-04 scope boundary
PA-04 addresses cross-document consistency in repository documents. It does not verify live GitHub Issues, recalculate workbook formulas in Excel, establish client approval, or certify all FR/AC/Test Scenario links. Those require separate evidence/verification.

## Next step
PA-05 — Proposal Version & Client Baseline: review the sent/client-facing proposal folder and establish version, date, approval/record status without implying simulated-client approval that has not occurred.
