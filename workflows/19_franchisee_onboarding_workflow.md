# 19 — Franchisee Onboarding Workflow

## Purpose

Onboard qualified franchise operators only after YieldWeek has a documented edition standard and founder-approved readiness gate.

## Trigger

A franchisee agreement is signed or founder explicitly approves onboarding preparation.

## Primary owner

Franchisee Manager Agent.

## Supporting agents

Product, Legal/Compliance, Finance/Treasury, Commercial, Operations, Orchestrator.

## Readiness prerequisite

No active franchisee onboarding may begin until Product confirms franchise readiness and founder approves the gate.

## Steps

1. Confirm `franchise_readiness_playbook.md` gate status.
2. Confirm signed agreement or founder-approved preparation mandate.
3. Create or update record in `franchisees.csv`.
4. Create onboarding tasks in `tasks.csv` for Product, Operations, Legal/Compliance, Finance/Treasury, and Tech/Engineer as needed.
5. Provide edition playbook, brand rules, reporting requirements, approval rules, and data handling rules.
6. Confirm territory, city, operator role, sponsor/badge process, and escalation chain.
7. Legal/Compliance reviews any local commitments or deviations.
8. Finance/Treasury confirms fee/payment handling if applicable.
9. Product runs readiness review before the franchisee operates publicly under YieldWeek brand.

## Done state

Franchisee is onboarded, paused, or rejected with status and reason logged.

## Required data writes

- `franchisees.csv`: status, fit score, readiness gate, territory, notes.
- `tasks.csv`: onboarding tasks and blockers.
- `risks.csv`: legal, brand, or operational issues.
- `interactions.csv`: external franchisee communication.

## Human approval gates

Founder approval required for any franchise sale, territory grant, brand use, local partnership, or public announcement.

## Success metrics

- 0 franchisee activation before readiness gate.
- 100% franchisees have fit memo and signed/approved terms.
- 100% deviations escalated before external commitment.
