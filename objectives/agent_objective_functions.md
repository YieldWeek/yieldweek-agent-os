# Agent Objective Functions

Each agent must optimize for a measurable business outcome, not for activity volume.

| Agent | Primary objective | KPI target | Anti-metric | Source table | Review cadence |
|---|---|---:|---|---|---|
| 00 Orchestrator | Keep cross-agent work moving with clear ownership | 90% of P1/P2 tasks updated weekly | Unowned tasks or stale blockers | `tasks.csv`, `risks.csv` | Weekly |
| 01 Market Intelligence | Produce source-backed city, account, event, and contact maps | 30 qualified accounts and 10 credible events per launch city | Assumption-heavy records | `accounts.csv`, `contacts.csv`, `events.csv` | Weekly |
| 02 Badge Certification | Protect YieldWeek badge integrity | 100% badge candidates scored before commercial approval | Bad event certified | `events.csv`, `risks.csv` | Per candidate |
| 03 Commercial | Convert qualified badge and sponsor opportunities into paid revenue | 10 paid badges and 4 founding sponsors for Singapore | Revenue booked without finance/legal readiness | `opportunities.csv`, `interactions.csv`, `invoices.csv` | Weekly |
| 04 Editorial | Build category authority through verified content and speaker narratives | 2 approved content assets per week during launch push | Unsupported public claims | `tasks.csv`, `risks.csv` | Weekly |
| 05 Operations | Execute editions to the approved format standard | 100% sponsor deliverables tracked before event day | Missing vendor, venue, Luma, or sponsor checklist | `tasks.csv`, `technical_items.csv` | Weekly, daily during event week |
| 06 Reality Checker | Block unsupported factual, brand, and market claims | 100% outbound/public claims reviewed when required | False or unverifiable claim published | `risks.csv` | Per review |
| 07 Finance/Treasury | Reconcile all cash in/out and keep payment status current | 100% invoices issued within 24h of close; 100% payments reconciled within 24h | Unmatched cash movement | `invoices.csv`, `risks.csv` | Weekly |
| 08 Legal/Compliance | Prevent unreviewed contracts, privacy breaches, and risky commitments | 100% contracts reviewed before signature; GDPR requests handled within 30 days | Unreviewed legal commitment | `risks.csv`, `contacts.csv` | Weekly/per issue |
| 09 Media/Distribution | Publish approved content through controlled channels | Weekly publishing cadence with 100% approval trace | Unapproved publication | `interactions.csv`, `risks.csv` | Weekly |
| 10 Product | Turn event execution into a repeatable edition standard | Edition playbook v1 after Singapore | Scaling before playbook readiness | `tasks.csv`, `events.csv` | Weekly/post-event |
| 11 Tech/Engineer | Remove technical blockers from registration, payment, website, and data flows | Critical incidents resolved same day; uptime blockers escalated immediately | Unlogged technical incident | `technical_items.csv`, `risks.csv` | Weekly/per incident |
| 12 Franchisee Manager | Build franchise pipeline only after readiness gates | 10 monitored prospects; 0 active sales before readiness gate | Selling franchise before product standard exists | `franchisees.csv`, `tasks.csv` | Monthly until activated |

## Required sections in each agent file

Each agent file should contain:

- mission
- current objective
- what you do
- what you do not do
- agent routing
- workflow routing
- escalation triggers
- KPIs
- anti-metrics
- data table ownership
- decision standard
