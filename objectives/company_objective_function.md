# Company Objective Function

## Current objective

Validate whether YieldWeek can become a repeatable city-edition business, starting with Singapore and Hong Kong, without creating operational, financial, legal, or brand chaos.

## Singapore validation gates

| Gate | Target | Owner | Source table | Status rule |
|---|---:|---|---|---|
| Paid Type A badge listings | 10 | Commercial + Badge Certification | `opportunities.csv`, `invoices.csv` | Count only `closed_won` with `payment_status=paid` |
| Founding sponsors | 4 | Commercial | `opportunities.csv`, `invoices.csv` | Count only sponsorship deals paid or legally committed |
| Qualified sponsor pipeline | 30 accounts | Market Intelligence + Commercial | `accounts.csv`, `opportunities.csv` | Tier A/B, source-backed, next action dated |
| Credible organiser pipeline | 10 events | Market Intelligence + Badge Certification | `events.csv` | Fit score >=4, source confidence not assumption |
| Finance process live | 100% before first paid close | Finance/Treasury | `invoices.csv` | Invoice, payment, reconciliation fields ready |
| Legal process live | 100% before first contract | Legal/Compliance | `risks.csv`, templates | Contract review workflow available |
| Attendee data process live | 100% before registration opens | Legal + Tech | `technical_items.csv` | Data architecture and privacy handling approved |
| Product learning loop | 1 edition playbook baseline | Product | `tasks.csv` | Edition playbook draft created after first edition |

## Anti-objectives

- Do not optimize for vanity content volume.
- Do not collect attendee data before legal and technical handling rules exist.
- Do not accept sponsor money without invoice and contract workflow readiness.
- Do not scale cities before Singapore has produced reusable operating evidence.

## Weekly review standard

The Orchestrator must produce a weekly review covering revenue, pipeline, risks, product readiness, legal blockers, finance status, technical blockers, and next five actions.
