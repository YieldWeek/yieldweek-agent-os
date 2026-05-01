# Type A Badge Sales Workflow

## Purpose

Convert relevant third-party event organisers into paid YieldWeek Type A badge partners.

## Trigger

A candidate event is identified as potentially relevant to a YieldWeek city edition.

## Agents involved

- Primary agent: Commercial Agent
- Supporting agents: Market Intelligence Agent, Badge Certification Agent, Reality Checker Agent, Orchestrator Agent

## Inputs

- Candidate event name
- Event URL
- City
- Date
- Organiser name
- Audience profile
- Sponsor profile
- Known contact path
- Current YieldWeek edition strategy

## Steps

1. Target identification
   - Owner: Market Intelligence Agent
   - Action: Identify candidate event and collect verified source links.
   - Output: Candidate event record in `data/event_pipeline.csv`.

2. Badge fit assessment
   - Owner: Badge Certification Agent
   - Action: Score the event against YieldWeek badge criteria.
   - Output: Badge qualification memo using `templates/badge_qualification_memo.md`.

3. Commercial angle
   - Owner: Commercial Agent
   - Action: Define buyer pain, value proposition, pricing hypothesis, and outreach angle.
   - Output: Outreach brief and draft email.

4. Claim review
   - Owner: Reality Checker Agent
   - Action: Verify all factual claims, remove unsupported statements, flag risk.
   - Output: Approved or flagged outbound draft.

5. Approval
   - Owner: Orchestrator Agent
   - Action: Determine whether founder approval is required.
   - Output: Send approval request or autonomous send decision.

6. Outreach
   - Owner: Commercial Agent
   - Action: Send or queue outreach from approved address.
   - Output: Email sent, CRM updated.

7. Reply handling
   - Owner: Commercial Agent
   - Action: Classify reply as positive, neutral, objection, negative, unsubscribe, or escalation.
   - Output: Next action recommendation.

8. Close path
   - Owner: Commercial Agent
   - Action: Prepare call brief, pricing recommendation, and close checklist.
   - Output: Founder-ready call pack.

## Human approval points

Founder approval is required for:

- Tier A targets
- pricing changes
- discounts
- legal terms
- claims of official partnership
- use of founder name
- sponsor or attendee access promises
- badge approval for high-profile events

## Outputs

- Updated event pipeline
- Badge qualification memo
- Outreach email
- Reply classification
- Deal status
- Next action

## Escalation rules

Escalate if:

- organiser asks for exclusivity
- organiser asks about revenue share
- organiser challenges YieldWeek legitimacy
- organiser requests attendee data
- organiser asks for contract terms
- negative reputational feedback appears
- event quality is questionable but commercially attractive

## Success metrics

- qualified organiser calls booked
- paid badge listings closed
- conversion rate by event type
- average badge fee
- time from target identification to first response
