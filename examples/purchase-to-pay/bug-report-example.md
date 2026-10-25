# BUG-P2P-004: Vendor bill created from partially received PO uses ordered quantity instead of received quantity

| Field | Value |
|---|---|
| Severity | High |
| Priority | P1 |
| Environment | Staging (example), Odoo 17, Chrome |
| Related test case | TC-09 |

## Steps to reproduce
1. Create PO for Office Chair x10 from Acme Supplies and confirm.
2. Validate the receipt with 6 units and create a backorder for 4.
3. On the PO, click **Create Bill**.

## Expected result
Bill line quantity = 6 (billing control policy = received quantities).

## Actual result
Bill line quantity = 10. The vendor could be paid for 4 chairs that have not been received.

## Evidence
Screenshot of bill line and the product's purchase tab showing Control Policy = "On ordered quantities".

## Notes
Always reproducible. Likely cause: the product's billing policy was imported as "ordered" during data migration. Suggest a data fix plus a check on all migrated products.
