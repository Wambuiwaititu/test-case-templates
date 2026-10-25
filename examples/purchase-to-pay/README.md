# Worked example: ERP Purchase-to-Pay (P2P)

A fictional example showing how the templates are used to test a standard ERP purchase-to-pay flow (based on Odoo Purchase, Inventory and Accounting):

**RFQ → Purchase Order → (Approval) → Goods Receipt → Vendor Bill (3-way match) → Payment**

Files:
- [test-plan.md](test-plan.md): scope and approach
- [test-cases.csv](test-cases.csv): 14 test cases, positive and negative
- [bug-report-example.md](bug-report-example.md): a sample defect write-up

All data (vendors, amounts, IDs) is made up for demonstration.
