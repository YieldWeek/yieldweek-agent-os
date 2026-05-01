# 11 — Payment Invoice Workflow

## Purpose

Issue, track, and reconcile invoices for closed badge, sponsorship, franchise, or other paid opportunities.

## Trigger

An opportunity reaches invoice-ready state, normally `stage=closed_won` or founder-approved invoice request.

## Primary owner

Finance/Treasury Agent.

## Supporting agents

Commercial, Legal/Compliance, Orchestrator.

## Inputs

- `opportunities.csv` opportunity record
- approved commercial terms
- contract status where applicable
- billing contact in `contacts.csv`

## Steps

1. Confirm the opportunity has `opportunity_id`, `account_id`, `contact_id`, amount, currency, edition, and city.
2. Confirm Legal/Compliance has cleared contract or standard terms where applicable.
3. Create invoice record in `invoices.csv` with `payment_status=draft`.
4. Generate invoice number using `YW-2026-XXXX`.
5. Submit invoice draft for founder approval if first-time client, non-standard terms, refund, discount, or unusual payment method.
6. Send invoice only after approval where required.
7. Update `payment_status=sent` and log external communication in `interactions.csv`.
8. On payment evidence, update `payment_status=paid`, `payment_received_date`, `reconciled`, and `reconciled_date`.
9. If payment cannot be matched, create P1 Finance task in `tasks.csv` and do not mark opportunity complete.
10. If disputed, trigger `14_payment_dispute_workflow.md`.

## Done state

Invoice is paid and reconciled, or the opportunity is closed/lost/cancelled with reason logged.

## Required data writes

- `invoices.csv`: invoice status and reconciliation fields.
- `opportunities.csv`: stage and notes.
- `interactions.csv`: invoice send and payment communication.
- `tasks.csv`: follow-ups or blockers.
- `risks.csv`: disputes, unmatched payments, refund requests.

## Human approval gates

Founder approval required for refunds, discounts, non-standard payment terms, first-time high-value invoice, or disputed resolution.

## Success metrics

- Invoice issued within 24h of invoice-ready opportunity.
- Payment reconciled within 24h of confirmation.
- 0 unmatched payments older than 48h.
