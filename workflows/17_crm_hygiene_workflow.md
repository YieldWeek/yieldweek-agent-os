# 17 — CRM Hygiene Workflow

## Purpose

Keep YieldWeek CRM usable as multiple agents create and update records.

## Trigger

Weekly cadence, bulk import, duplicate detection, or broken foreign-key reference.

## Primary owner

Orchestrator Agent.

## Supporting agents

Market Intelligence, Commercial, Legal/Compliance, Finance/Treasury, Franchisee Manager.

## Steps

1. Review new records created during the period.
2. Check duplicate accounts by website domain and exact account name.
3. Check duplicate contacts by email, LinkedIn URL, or name + account ID.
4. Check opportunities for missing account/contact IDs, invalid stage, missing next action, or stale next action date.
5. Check GDPR fields before outbound campaigns.
6. Check invoices for missing opportunity/account/contact IDs.
7. Check risks and tasks for stale open P1/P2 items.
8. Create correction tasks for owning agents.
9. Mark duplicate records as merged/closed through notes rather than silent deletion.

## Done state

Known duplicates, invalid statuses, missing required fields, and stale P1/P2 blockers are either corrected or assigned.

## Required data writes

- `tasks.csv`: correction tasks.
- affected CRM tables: corrected IDs, statuses, notes.
- `risks.csv`: high-impact data quality risks.

## Human approval gates

Founder approval required before deleting records, changing financial status, or overriding GDPR fields.

## Success metrics

- 0 known duplicate accounts after review.
- 0 open opportunities without next action.
- 0 outbound campaign records with `do_not_contact=TRUE`.
