# 14 — Payment Dispute Workflow

## Purpose

Handle disputed invoices, delayed wires, refund requests, mistaken invoices, chargebacks, and payment mismatches.

## Trigger

Invoice status becomes `disputed`, sponsor requests refund, payment is delayed beyond agreed terms, or payment arrives without matching deal.

## Primary owner

Finance/Treasury Agent.

## Supporting agents

Commercial, Legal/Compliance, Orchestrator.

## Steps

1. Update `invoices.csv` `payment_status=disputed` where applicable.
2. Create a financial risk in `risks.csv` with severity based on amount and exposure.
3. Create P1/P2 task in `tasks.csv` with owner and due date.
4. Collect dispute facts: invoice number, opportunity ID, amount, contract terms, email history, payment evidence.
5. Ask Commercial for client context and Legal/Compliance for contract/refund exposure.
6. Prepare founder approval request with options: enforce, amend, credit, refund, cancel, or escalate.
7. Do not promise refund, credit, cancellation, or changed terms before founder approval.
8. Once approved, update invoice status and log external response in `interactions.csv`.

## Done state

Dispute is resolved, invoice corrected, payment received, refund approved/completed, or legal escalation opened.

## Required data writes

- `invoices.csv`: payment status and notes.
- `risks.csv`: financial/legal risk.
- `tasks.csv`: dispute task.
- `interactions.csv`: client communication.
- `opportunities.csv`: commercial status if changed.

## Human approval gates

Founder approval required for refund, credit note, cancellation, amended invoice, payment-term change, or settlement offer.

## Success metrics

- 100% disputes logged within same business day.
- 0 refund/payment-term promises without approval.
- 0 disputed invoices without owner and next action.
