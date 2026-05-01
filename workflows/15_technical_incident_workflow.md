# 15 — Technical Incident Workflow

## Purpose

Handle website, payment, Luma, CRM, data export, email, registration, and infrastructure failures.

## Trigger

Any technical failure, outage, broken integration, suspicious access, data exposure, payment failure, or registration issue.

## Primary owner

Tech/Engineer Agent.

## Supporting agents

Operations, Finance/Treasury, Legal/Compliance, Product, Orchestrator.

## Steps

1. Create technical item in `technical_items.csv` with severity.
2. If personal data, payment, or public-facing systems are affected, create `risks.csv` entry.
3. For critical incidents, notify Orchestrator and founder immediately.
4. Identify affected system, user impact, workaround, owner, and deadline.
5. If data breach is suspected, trigger `governance/data_breach_response.md`.
6. If payment system is affected, notify Finance/Treasury.
7. If registration or attendee journey is affected, notify Operations and Product.
8. Resolve, document root cause, and update status.
9. Add lessons to relevant playbook if incident reveals process gap.

## Done state

Incident is resolved, workaround approved, or risk accepted by founder with next action logged.

## Required data writes

- `technical_items.csv`: incident details and resolution.
- `risks.csv`: high/critical or privacy/payment incidents.
- `tasks.csv`: owner and deadlines.

## Human approval gates

Founder approval required for public incident disclosure, data breach response, payment workaround, or accepted critical risk.

## Success metrics

- Critical incidents escalated immediately.
- Every incident has owner, severity, and resolution status.
- No attendee/payment data incident remains unlogged.
