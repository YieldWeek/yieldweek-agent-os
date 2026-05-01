# Invoice Reconciliation Workflow

## Purpose

Ensure every confirmed badge or sponsor deal is invoiced, collected, reconciled, and reflected in the weekly cash position.

## Trigger

A sponsor package or Type A badge listing is confirmed by Commercial Agent and approved for invoicing.

## Agents involved

- Primary agent: Finance / Treasury Agent
- Supporting agents: Commercial Agent, Legal / Compliance Agent, Operations Agent, Orchestrator Agent

## Inputs

- Confirmed deal record
- Deal type: badge / sponsor / other
- Company or organiser name
- Billing entity details
- Amount and currency
- Payment method: Stripe / wire / other
- Payment terms
- Contract or order reference
- CRM deal link

## Steps

1. Confirm invoice readiness
   - Owner: Commercial Agent
   - Output: confirmed deal handoff to Finance / Treasury

2. Check legal/payment terms
   - Owner: Legal / Compliance Agent
   - Output: approved payment terms or escalation

3. Issue invoice
   - Owner: Finance / Treasury Agent
   - Output: invoice issued within 24h of confirmed deal

4. Track receivable
   - Owner: Finance / Treasury Agent
   - Output: invoice status in finance log

5. Reconcile payment
   - Owner: Finance / Treasury Agent
   - Output: Stripe or wire receipt matched to CRM deal

6. Escalate discrepancies
   - Owner: Finance / Treasury Agent
   - Output: anomaly report to Orchestrator

7. Weekly cash summary
   - Owner: Finance / Treasury Agent
   - Output: cash position for weekly CEO review

## Human approval points

Founder approval required for refunds, payment term changes, disputed invoices, expense approvals, bank account changes, and any unmatched payment anomaly.

## Outputs

- Invoice record
- Payment status
- Reconciliation status
- Cash position update
- Overdue invoice list
- Payment anomaly log

## Success metrics

- invoices issued within 24h
- all payments matched to CRM deals
- no unapproved refunds or spend
- weekly cash position accurate
