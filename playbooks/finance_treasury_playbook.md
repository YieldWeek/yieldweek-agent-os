# Finance / Treasury Playbook

## Objective

Keep cash, invoicing, reconciliation, expenses, and HK entity records clean during the Singapore validation phase.

## Core gates

- invoice issued within 24h of confirmed deal
- Stripe and wire receipts reconciled weekly
- overdue invoices flagged weekly
- approved expenses logged before payment
- weekly cash position available for CEO review

## Source systems

- CRM for confirmed commercial deals
- Stripe / Airwallex / bank records for payments
- `data/finance_log.csv` for operating log
- contract records for payment terms

## Weekly checklist

1. Review closed-won badge and sponsor deals.
2. Confirm invoice status.
3. Match receipts to CRM deals.
4. Flag overdue invoices.
5. Review approved expenses.
6. Update cash position.
7. Add finance summary to weekly CEO review.

## Escalation

Escalate unmatched payments, disputed invoices, refunds, missing approvals, bank/account changes, and any HK entity issue.
