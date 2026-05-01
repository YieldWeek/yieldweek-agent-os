# Agent Audit Log Policy

This policy defines how agent actions are made auditable.

## Core audit principle

Any external communication, CRM change, risk flag, approval request, invoice action, publication action, or technical incident must leave a trace.

## Required logs by action type

| Action | Required log |
|---|---|
| External email sent or received | `interactions.csv` |
| New account/contact/opportunity/event | Relevant CRM table with source fields |
| Task created or closed | `tasks.csv` |
| Risk identified | `risks.csv` |
| Invoice issued/reconciled/disputed | `invoices.csv` |
| Technical incident | `technical_items.csv` and `risks.csv` if high/critical |
| Public content published | publication log in Media/Distribution workflow output |
| Founder approval requested | `founder_approval_request.md` output and `tasks.csv` |

## Wrong-message protocol

If an agent sends an incorrect or unauthorized message:

1. Stop follow-up automation.
2. Log the incident in `risks.csv` with `risk_type=reputational` or `operational`.
3. Notify Orchestrator and founder.
4. Draft correction/retraction for founder approval.
5. Update `interactions.csv` with the correction outcome.

## No silent deletion

Agents must not silently delete records to hide mistakes. Corrections should be traceable through notes, status changes, or explicit replacement records.
