# 18 — Post-Event Learning Workflow

## Purpose

Convert each YieldWeek edition into a better operating standard for future cities and franchise readiness.

## Trigger

A city edition closes or a major event milestone completes.

## Primary owner

Product Agent.

## Supporting agents

Operations, Commercial, Editorial, Badge Certification, Media/Distribution, Finance/Treasury, Tech/Engineer, Orchestrator.

## Steps

1. Operations compiles event execution notes, sponsor deliverable status, attendee experience observations, and operational issues.
2. Commercial compiles sponsor and badge revenue outcomes, objections, and conversion lessons.
3. Finance/Treasury compiles invoice, payment, and reconciliation outcomes.
4. Media/Distribution compiles content and media performance.
5. Tech/Engineer compiles infrastructure issues and data lessons.
6. Product compares actual execution against the edition standard.
7. Product updates `edition_playbook_outline.md` or `product_edition_standard_playbook.md`.
8. Orchestrator creates tasks for unresolved improvements.
9. High-risk lessons are logged in `risks.csv`.

## Done state

A post-event learning memo and playbook update are completed within 10 business days.

## Required data writes

- `tasks.csv`: improvement tasks.
- `events.csv`: post-event status and notes.
- `risks.csv`: unresolved or repeated failure modes.
- `technical_items.csv`: technical lessons if relevant.

## Human approval gates

Founder approval required before declaring the edition standard franchise-ready or using lessons in public claims.

## Success metrics

- Playbook update within 10 business days.
- Sponsor deliverable status documented.
- High or critical issues converted into process changes.
