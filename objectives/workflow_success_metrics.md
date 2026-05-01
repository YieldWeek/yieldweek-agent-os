# Workflow Success Metrics

Every workflow must have a trigger, a done state, required data writes, and a success metric.

| # | Workflow | Trigger | Done state | Required data writes | Success metric |
|---:|---|---|---|---|---|
| 01 | City Market Map | City set to active in `target_cities.csv` | Top targets created in CRM with source confidence | `accounts.csv`, `contacts.csv`, `events.csv`, `opportunities.csv` | 10 qualified targets, 0 duplicate accounts |
| 02 | Type A Badge Sales | Badge opportunity opened | Payment confirmed or closed lost reason logged | `events.csv`, `opportunities.csv`, `interactions.csv`, `invoices.csv` | 10 paid badge listings |
| 03 | Sponsor Sales | Sponsor opportunity opened | Payment confirmed or closed lost reason logged | `accounts.csv`, `contacts.csv`, `opportunities.csv`, `interactions.csv`, `invoices.csv` | 4 founding sponsors |
| 04 | Editorial Content | Content task created | Approved content handed to Media/Distribution | `tasks.csv`, `risks.csv`, `interactions.csv` where external | 2 approved assets/week |
| 05 | Speaker Invitation | Speaker target approved | Speaker confirmed/declined/cancelled and logged | `contacts.csv`, `interactions.csv`, `tasks.csv` | Confirmed speaker status updated within 24h |
| 06 | Event Operations | Edition status moves to planning | Event operating brief complete and open risks logged | `tasks.csv`, `technical_items.csv`, `risks.csv` | 100% critical checklists complete before event |
| 07 | Weekly CEO Review | Weekly cadence | Memo issued; tasks and risks updated | `tasks.csv`, `risks.csv` | No stale P1 blockers |
| 08 | Reality Check | Review requested or approval gate reached | Approved, corrected, blocked, or escalated | `risks.csv`, `tasks.csv` | 100% high-risk claims resolved before publish/send |
| 09 | Inbound Email Triage | Inbound email received | Routed, replied, or escalated with CRM log | `interactions.csv`, `tasks.csv`, `risks.csv` if needed | 100% legal/VIP routed correctly |
| 10 | Outbound Campaign | Campaign brief approved | Sends logged; replies classified; suppressions applied | `interactions.csv`, `contacts.csv`, `tasks.csv` | No outreach to do-not-contact contacts |
| 11 | Payment Invoice | Opportunity reaches invoice-ready state | Invoice sent and reconciled or exception logged | `invoices.csv`, `opportunities.csv`, `risks.csv` | Invoice issued within 24h |
| 12 | Contract Review | Contract needed or received | Founder-ready legal review memo complete | `risks.csv`, `tasks.csv` | 100% contract commitments reviewed |
| 13 | GDPR Data Request | Deletion/export/opt-out request received | Request completed or escalated within SLA | `contacts.csv`, `interactions.csv`, `risks.csv` | 30-day completion SLA |
| 14 | Payment Dispute | Invoice marked disputed/refund requested | Resolution logged and approved | `invoices.csv`, `risks.csv`, `tasks.csv` | No unresolved critical finance issue |
| 15 | Technical Incident | Technical failure or risk flagged | Incident resolved or workaround approved | `technical_items.csv`, `risks.csv` | Critical incidents escalated immediately |
| 16 | Content Distribution | Content approved | Publication/schedule logged | `interactions.csv`, `tasks.csv`, `risks.csv` | 100% approved-only publication |
| 17 | CRM Hygiene | Weekly cadence or import event | Duplicates merged; required fields checked | All CRM tables | 0 known duplicates after review |
| 18 | Post-Event Learning | Edition closes | Learnings converted to playbook updates | `tasks.csv`, `events.csv`, `risks.csv` | Playbook update within 10 business days |
| 19 | Franchisee Onboarding | Franchise agreement signed | Onboarding complete and quality gates accepted | `franchisees.csv`, `tasks.csv`, `risks.csv` | No onboarding before readiness gate |
| 20 | Badge Quality Alert | Badged event underperforms or risk emerges | Badge status reviewed and corrective action logged | `events.csv`, `risks.csv`, `tasks.csv` | 100% quality failures reviewed |
