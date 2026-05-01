# 20 — Badge Quality Alert Workflow

## Purpose

Respond when a badged or listed event may fail YieldWeek quality standards.

## Trigger

A badged event receives a credible complaint, quality concern, cancellation, postponement, misleading claim, sponsor concern, weak execution signal, or post-certification issue.

## Primary owner

Badge Certification Agent.

## Supporting agents

Reality Checker, Operations, Commercial, Legal/Compliance, Media/Distribution, Orchestrator.

## Steps

1. Create `risks.csv` entry with `risk_type=brand` or `operational`.
2. Update `events.csv` badge status if review is required.
3. Collect evidence from source URLs, direct communication, sponsor feedback, attendee feedback, or organiser update.
4. Reality Checker verifies factual basis.
5. Legal/Compliance reviews if public badge use, refund, liability, or misuse is involved.
6. Commercial checks sponsor/client exposure.
7. Badge Certification recommends maintain, condition, suspend, revoke, or escalate.
8. Founder approves any suspension, revocation, refund exposure, or public statement.
9. Media/Distribution updates public surfaces only after approval.

## Done state

Badge status is confirmed, conditioned, suspended, revoked, or escalated with all affected records updated.

## Required data writes

- `events.csv`: badge status and notes.
- `risks.csv`: issue and resolution.
- `tasks.csv`: follow-up actions.
- `interactions.csv`: organiser/sponsor communications.

## Human approval gates

Founder approval required before public badge revocation, refund, sponsor communication about quality failure, or public correction.

## Success metrics

- 100% quality issues logged same business day.
- 100% public badge changes founder-approved.
- No unresolved high-severity badge issue without owner.
