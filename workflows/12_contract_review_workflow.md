# 12 — Contract Review Workflow

## Purpose

Review contracts, agreement templates, risky terms, partnership commitments, sponsorship terms, badge listing terms, vendor terms, and franchise terms before YieldWeek makes a binding commitment.

## Trigger

A contract is received, a contract is requested, or an agent detects legal/commercial commitment risk.

## Primary owner

Legal/Compliance Agent.

## Supporting agents

Commercial, Finance/Treasury, Product, Franchisee Manager, Reality Checker, Orchestrator.

## Inputs

- contract or term sheet
- `templates/contract_request_brief.md`
- related account/contact/opportunity records
- commercial terms and deadline

## Steps

1. Create or update a legal risk record in `risks.csv` if the issue is non-standard.
2. Confirm related `account_id`, `contact_id`, and `opportunity_id` exist where relevant.
3. Complete `contract_request_brief.md` if contract is needed but not yet drafted.
4. Review received terms against approval rules, financial controls, privacy policy, exclusivity, liability, cancellation, and data-sharing risks.
5. Produce `legal_review_memo.md` with issue, clause, severity, recommended edit, and founder action required.
6. Escalate to founder if any term creates commitment, exclusivity, refund exposure, data sharing, franchise rights, or unusual liability.
7. If external counsel is required, log that need in `tasks.csv` and pause execution.
8. Once resolved, update `risks.csv` status and related opportunity notes.

## Done state

Legal review memo is complete and either approved, revised, escalated to counsel, or rejected.

## Required data writes

- `risks.csv`: legal/compliance flags and status.
- `tasks.csv`: review task and approval follow-up.
- `opportunities.csv`: notes where contract affects commercial status.
- `interactions.csv`: external contract communications.

## Human approval gates

Founder approval required before signature, binding commitment, exclusivity, non-standard payment/refund term, attendee data access, or franchise promise.

## Success metrics

- 100% contracts reviewed before signature.
- 0 unreviewed legal commitments.
- High/critical legal risks escalated same day.
