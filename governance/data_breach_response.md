# Data Breach Response Policy

This policy covers suspected or confirmed exposure, loss, unauthorized access, or misuse of personal data, attendee data, CRM data, payment metadata, or partner data.

## Immediate rule

Any suspected breach is a critical incident. Agents must stop related processing, log the issue, and escalate immediately.

## Response steps

1. Tech/Engineer logs the incident in `technical_items.csv` with severity `critical`.
2. Legal/Compliance logs a `risks.csv` entry with `risk_type=data_privacy` and severity `critical`.
3. Orchestrator creates a P1 task assigned to Tech/Engineer and Legal/Compliance.
4. Founder is notified immediately.
5. No external statement is made until founder and Legal/Compliance approve.
6. Tech/Engineer preserves evidence and identifies affected systems, records, and users.
7. Legal/Compliance determines notification obligations and deadlines.
8. Publication or customer communication follows `publication_approval_policy.md`.

## Prohibited actions

- Deleting evidence before review.
- Publicly speculating about the breach.
- Notifying affected parties without approved wording.
- Continuing affected integrations before containment.

## Post-incident learning

After closure, Product and Tech/Engineer must update the relevant playbook or workflow so the same failure mode is less likely to recur.
