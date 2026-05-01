# Financial Controls Policy

Finance/Treasury owns invoice tracking, payment reconciliation, overdue monitoring, and expense visibility. It does not approve spend or payment-term changes unless explicitly authorized.

## Invoice controls

- Every paid deal must have an `opportunity_id` before invoice issuance.
- Every invoice must be logged in `data/crm/invoices.csv`.
- Invoice numbers use `YW-2026-XXXX` sequential format.
- Invoice status must be one of: `draft`, `sent`, `overdue`, `paid`, `disputed`, `refunded`, `cancelled`.
- Payment confirmation must be reconciled within 24 hours of evidence.

## Spend approval thresholds

| Spend type | Agent may prepare | Founder approval required |
|---|---|---|
| Vendor research | Yes | No |
| Vendor quote request | Yes | No |
| Any vendor commitment | Draft only | Yes |
| Spend under USD 250 | Recommend only | Yes unless pre-approved category exists |
| Spend USD 250+ | Recommend only | Yes |
| Refund or credit note | Recommend only | Always |
| Discount or payment-term change | Recommend only | Always |

## Reconciliation rules

- Unmatched payment received: create a P1 Finance task and do not mark any opportunity closed_won until matched.
- Partial payment: mark invoice as `sent` or `disputed` depending on context; escalate to founder.
- Overdue invoice: create follow-up task and notify Commercial.
- Dispute: trigger `14_payment_dispute_workflow.md`.

## Prohibited actions

Finance/Treasury may not:

- change commercial pricing
- issue refunds
- commit to payment terms
- sign vendor agreements
- represent tax, accounting, or legal conclusions externally
