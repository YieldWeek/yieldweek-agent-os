# 16 — Content Distribution Workflow

## Purpose

Move approved content from Editorial into controlled publication and distribution.

## Trigger

Content is approved by Reality Checker and, where required, Legal/Compliance or founder.

## Primary owner

Media/Distribution Agent.

## Supporting agents

Editorial, Commercial, Legal/Compliance, Reality Checker, Orchestrator.

## Steps

1. Confirm content approval status and source support.
2. Confirm no unresolved `risks.csv` item blocks publication.
3. Select channel: LinkedIn, newsletter, website, press, partner channel, or direct sponsor communication.
4. Use the appropriate template: `linkedin_post.md`, `newsletter_draft.md`, or `press_release.md`.
5. If sponsor/partner is named, confirm founder approval and partner permission.
6. Schedule or publish according to approved cadence.
7. Log publication outcome and any external replies in `interactions.csv` where relevant.
8. Create follow-up tasks for replies, inbound leads, corrections, or repurposing.

## Done state

Content is published/scheduled, logged, and any follow-up task is assigned.

## Required data writes

- `tasks.csv`: publication task status and follow-ups.
- `interactions.csv`: partner/media/external interactions.
- `risks.csv`: post-publication issues or corrections.

## Human approval gates

Founder approval required for public sponsor claims, partner announcements, revenue/traction claims, badge claims, city launch claims, or legal/regulatory claims.

## Success metrics

- 100% content published only after approval.
- Weekly publishing cadence maintained during launch push.
- Corrections logged and resolved if needed.
