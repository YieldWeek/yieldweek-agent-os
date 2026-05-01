# YieldWeek Workflow Index

This folder defines how YieldWeek agents work together.

Agents define roles.
Playbooks define business logic.
Workflows define execution sequences.
Governance defines approval and risk constraints.
Objectives define success metrics and done states.
Data tables define the operating source of truth.

## Core workflows

| # | Workflow file | Purpose | Primary Agent | Supporting Agents |
|---:|---|---|---|---|
| 01 | `01_city_market_map_workflow.md` | Map a city edition opportunity | Market Intelligence | Editorial, Product, Reality Checker |
| 02 | `02_type_a_badge_sales_workflow.md` | Convert event organisers into paid badge partners | Commercial | Market Intelligence, Badge Certification, Legal / Compliance, Finance / Treasury, Reality Checker, Orchestrator |
| 03 | `03_sponsor_sales_workflow.md` | Convert sponsors into paid edition sponsors | Commercial | Market Intelligence, Editorial, Media / Distribution, Legal / Compliance, Finance / Treasury, Reality Checker, Orchestrator |
| 04 | `04_editorial_content_workflow.md` | Produce category-building content | Editorial | Market Intelligence, Media / Distribution, Legal / Compliance, Reality Checker |
| 05 | `05_speaker_invitation_workflow.md` | Identify and invite speakers | Editorial | Market Intelligence, Commercial, Legal / Compliance, Reality Checker, Operations |
| 06 | `06_event_operations_workflow.md` | Execute a city edition | Operations | Product, Commercial, Editorial, Tech / Engineer, Finance / Treasury, Legal / Compliance, Reality Checker |
| 07 | `07_weekly_ceo_review_workflow.md` | Review pipeline and priorities | Orchestrator | All agents |
| 08 | `08_reality_check_workflow.md` | Verify claims and reduce risk | Reality Checker | Any requesting agent; Legal / Compliance when legal exposure exists |
| 09 | `09_inbound_email_triage_workflow.md` | Classify and route inbound messages | Orchestrator | Commercial, Editorial, Operations, Media / Distribution, Franchisee Manager, Legal / Compliance |
| 10 | `10_outbound_campaign_workflow.md` | Run controlled outbound at scale | Commercial | Market Intelligence, Media / Distribution, Legal / Compliance, Reality Checker, Orchestrator |
| 11 | `11_payment_invoice_workflow.md` | Invoice confirmed deals and reconcile payments | Finance / Treasury | Commercial, Legal / Compliance, Orchestrator |
| 12 | `12_contract_review_workflow.md` | Draft and review agreement templates and risky terms | Legal / Compliance | Commercial, Finance / Treasury, Product, Franchisee Manager, Reality Checker |
| 13 | `13_gdpr_data_request_workflow.md` | Handle opt-out, deletion, export, and privacy requests | Legal / Compliance | Orchestrator, Commercial, Media / Distribution, Tech / Engineer |
| 14 | `14_payment_dispute_workflow.md` | Resolve disputed invoices, refunds, and unmatched payments | Finance / Treasury | Commercial, Legal / Compliance, Orchestrator |
| 15 | `15_technical_incident_workflow.md` | Handle website, payment, Luma, CRM, data, and infrastructure failures | Tech / Engineer | Operations, Finance / Treasury, Product, Legal / Compliance, Orchestrator |
| 16 | `16_content_distribution_workflow.md` | Distribute approved content and manage media cadence | Media / Distribution | Editorial, Commercial, Legal / Compliance, Reality Checker |
| 17 | `17_crm_hygiene_workflow.md` | Keep CRM clean across agents and cities | Orchestrator | Market Intelligence, Commercial, Legal / Compliance, Finance / Treasury, Franchisee Manager |
| 18 | `18_post_event_learning_workflow.md` | Convert edition execution into playbook improvements | Product | Operations, Commercial, Editorial, Badge Certification, Media / Distribution, Finance / Treasury, Tech / Engineer |
| 19 | `19_franchisee_onboarding_workflow.md` | Onboard franchise operators after readiness gate | Franchisee Manager | Product, Legal / Compliance, Finance / Treasury, Commercial, Operations |
| 20 | `20_badge_quality_alert_workflow.md` | Respond to quality issues in badged/listed events | Badge Certification | Reality Checker, Operations, Commercial, Legal / Compliance, Media / Distribution, Orchestrator |

## Standard workflow file structure

Each workflow should include:

1. Purpose
2. Trigger
3. Primary owner and supporting agents
4. Inputs
5. Steps
6. Required data writes
7. Human approval gates
8. Done state
9. Success metrics

## Required integration rule

Every workflow must write to at least one source-of-truth table in `data/crm/` or explain why no data write is needed.
