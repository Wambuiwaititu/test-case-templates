# Test Case Templates

Reusable, lightweight QA templates I use for planning and documenting manual testing, plus a worked example for an ERP **purchase-to-pay** flow.

## Contents
| File | Use it for |
|---|---|
| [templates/test-plan.md](templates/test-plan.md) | Scope, approach, environments, entry/exit criteria, risks |
| [templates/test-cases.csv](templates/test-cases.csv) | Test cases, which you can import into Excel, Google Sheets, Jira (Xray/Zephyr) or TestRail |
| [templates/bug-report.md](templates/bug-report.md) | Clear, reproducible defect reports |
| [templates/uat-signoff.md](templates/uat-signoff.md) | Business acceptance and go-live decision |
| [examples/purchase-to-pay/](examples/purchase-to-pay/) | Worked example: RFQ → PO → approval → receipt → bill → payment |

## How to use
1. Copy the `templates/` folder into your project.
2. Fill in the test plan first, then derive test cases from requirements or user stories.
3. Open `test-cases.csv` in a spreadsheet and track Status (Not Run / Pass / Fail / Blocked).
4. Log failures with the bug report template and link the defect ID back to the test case.

## Sample (from the P2P example)
| ID | Title | Expected | Type |
|---|---|---|---|
| TC-04 | PO above threshold blocked for normal user | Error asking for manager approval; PO stays draft | Negative |
| TC-09 | Bill matches received qty (3-way match) | Bill qty = 6, not 10 | Functional |

The example data is fictional.
