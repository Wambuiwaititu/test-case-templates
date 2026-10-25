# Test Plan: Purchase-to-Pay (example)

## Scope
**In scope:** RFQ creation, PO confirmation, approval above threshold, receipts (full/partial), vendor bills, 3-way match, vendor payments, cancellations.
**Out of scope:** landed costs, multi-company, EDI vendor integrations.

## Approach
- Functional system testing of each step, then end-to-end scenarios across Purchase, Inventory and Accounting.
- Negative and boundary tests on approval threshold, quantities and bill amounts.
- Regression: the end-to-end happy path is re-run on every build.
- UAT: the procurement and finance teams run scenarios E2E-01 to E2E-03.

## Test data
- Vendors: "Acme Supplies Ltd" (KES), "Global Parts Inc" (USD)
- Products: Office Chair (storable, KES 8,000), Printer Toner (consumable)
- Approval threshold: KES 100,000
- Users: Purchase User, Purchase Manager, Accountant

## Entry / exit
- Entry: modules installed on staging, master data loaded, chart of accounts configured.
- Exit: all High priority cases passed, no open Critical/High defects, finance sign-off on bill/payment postings.

## Key risks
| Risk | Mitigation |
|---|---|
| Wrong journal entries on bill posting | Accountant reviews postings for each E2E case |
| Partial receipts billed in full | Dedicated 3-way match cases (TC-09, TC-10) |
