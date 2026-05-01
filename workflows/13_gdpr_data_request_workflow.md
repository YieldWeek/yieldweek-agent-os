# 13 — GDPR Data Request Workflow

## Purpose

Handle opt-out, deletion, export, correction, and attendee-data requests without accidental privacy breach or commercial misuse.

## Trigger

Any inbound message requesting opt-out, deletion, export, correction, unsubscribe, attendee list access, or personal data handling clarification.

## Primary owner

Legal/Compliance Agent.

## Supporting agents

Orchestrator, Commercial, Media/Distribution, Tech/Engineer.

## Steps

1. Log inbound request in `interactions.csv`.
2. Create a compliance task in `tasks.csv` with due date no later than 30 days from request.
3. Identify related contact/account records.
4. If opt-out or unsubscribe, set `contacts.csv` `gdpr_status=opted_out` and `do_not_contact=TRUE` immediately.
5. If deletion/export/correction, create `risks.csv` record with `risk_type=data_privacy` and severity based on scope.
6. Ask Tech/Engineer to identify systems where the data may exist.
7. Prepare response for founder/legal approval if request is complex, broad, or involves attendee data.
8. Complete deletion/export/correction if approved and log outcome.
9. Close task only when the response and CRM update are complete.

## Done state

Request is fulfilled, lawfully rejected with approved rationale, or escalated to founder/external counsel.

## Required data writes

- `interactions.csv`: inbound request and outbound response.
- `contacts.csv`: GDPR status and do-not-contact update.
- `tasks.csv`: compliance task.
- `risks.csv`: data privacy risk if non-routine.
- `technical_items.csv`: system/data-location work if needed.

## Human approval gates

Founder approval required for attendee data release, complex deletion disputes, data breach suspicion, or regulator/legal threat.

## Success metrics

- 100% opt-outs applied immediately.
- 100% GDPR requests resolved or escalated within 30 days.
- 0 outbound messages to `do_not_contact=TRUE` contacts.
