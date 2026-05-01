# Human Escalation Matrix

This policy defines when agents must stop and escalate to a human decision-maker.

## Default authority

The founder is the default approver for irreversible business, legal, financial, publication, and brand decisions.

If the founder is unavailable, agents must not invent substitute authority. They must use the fallback rules below.

## Escalation levels

| Level | Examples | Required action | Backup rule |
|---|---|---|---|
| P1 Critical | Legal threat, data breach, public false claim, payment fraud, contract signature request | Stop action, log `risks.csv`, create P1 task, notify founder immediately | If founder unavailable, hold decision and prepare options memo |
| P2 High | Sponsor exclusivity, refund request, vendor payment above threshold, attendee data request | Pause action, log risk or task, request approval | If founder unavailable, do not approve; maintain status quo |
| P3 Medium | Content uncertainty, unclear reply, CRM conflict, non-critical vendor issue | Route to owning agent and Orchestrator | Orchestrator may decide only if governance permits |
| P4 Low | Formatting, routine CRM enrichment, standard follow-up | Agent may proceed within policy | No escalation needed |

## Founder-unavailable protocol

When founder approval is required and unavailable:

1. Agent creates `templates/founder_approval_request.md` output.
2. Orchestrator logs a P1/P2 task in `tasks.csv`.
3. No external commitment is made.
4. No payment, refund, publication, contract, attendee-data release, or franchise promise proceeds.
5. Agent may draft non-committal holding response only if allowed by `email_autonomy_policy.md`.

## Mandatory escalation triggers

- Contract terms not already approved.
- Any exclusivity or partnership commitment.
- Any refund, discount outside approved pricing, or changed payment terms.
- Any attendee list or personal-data request.
- Any public claim not source-backed.
- Any suspected data breach.
- Any third-party misuse of YieldWeek brand or badge.
- Any franchisee activation before readiness gate.
