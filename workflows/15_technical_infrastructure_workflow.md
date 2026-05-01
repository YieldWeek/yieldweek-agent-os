# Technical Infrastructure Workflow

## Purpose

Keep YieldWeek technical infrastructure reliable, owned, and ready for city edition execution.

## Trigger

A website, payment flow, Luma setup, data architecture, or technical incident requires setup, review, or escalation.

## Agents involved

- Primary agent: Tech / Engineer Agent
- Supporting agents: Operations Agent, Finance / Treasury Agent, Product Agent, Legal / Compliance Agent, Orchestrator Agent

## Inputs

- Technical asset or issue
- City edition affected
- Dependency owner
- Deadline
- Data/privacy implications
- Payment implications
- Fallback option

## Steps

1. Define technical requirement
   - Owner: Tech / Engineer Agent
   - Output: technical requirement brief

2. Check event operations dependency
   - Owner: Operations Agent
   - Output: event-day and Luma requirements

3. Check payment/reconciliation dependency
   - Owner: Finance / Treasury Agent
   - Output: Stripe/Airwallex reconciliation requirement

4. Check product/data architecture fit
   - Owner: Product Agent
   - Output: data ownership and format constraints

5. Check legal/privacy constraints
   - Owner: Legal / Compliance Agent
   - Output: GDPR/data/privacy risk notes

6. Test and document
   - Owner: Tech / Engineer Agent
   - Output: tested setup, fallback, and incident notes

7. Escalate if needed
   - Owner: Orchestrator Agent
   - Output: founder decision request

## Human approval points

Founder approval required for paid vendors, public website changes, data architecture decisions, attendee data access changes, and payment infrastructure changes.

## Outputs

- Technical requirement brief
- Infrastructure log update
- Test result
- Fallback plan
- Incident report if relevant

## Success metrics

- singapore.yieldweek.org live and maintained
- payment flows tested
- Luma configuration reviewed before registration opens
- attendee data architecture documented and approved
- no untested critical dependency enters an edition
