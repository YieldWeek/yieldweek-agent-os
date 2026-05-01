# YieldWeek Workflow Index

This folder defines how YieldWeek agents work together.

Agents define roles.
Playbooks define business logic.
Workflows define execution sequences.
Governance defines approval and risk constraints.

## Core workflows

| Workflow | Purpose | Primary Agent | Supporting Agents |
|---|---|---|---|
| City Market Map | Map a city edition opportunity | Market Intelligence | Editorial, Product, Reality Checker |
| Type A Badge Sales | Convert event organisers into paid badge partners | Commercial | Market Intelligence, Badge Certification, Legal / Compliance, Finance / Treasury, Reality Checker, Orchestrator |
| Sponsor Sales | Convert sponsors into paid edition sponsors | Commercial | Market Intelligence, Editorial, Media / Distribution, Legal / Compliance, Finance / Treasury, Reality Checker, Orchestrator |
| Editorial Content | Produce category-building content | Editorial | Market Intelligence, Media / Distribution, Legal / Compliance, Reality Checker |
| Speaker Invitation | Identify and invite speakers | Editorial | Market Intelligence, Commercial, Legal / Compliance, Reality Checker, Operations |
| Event Operations | Execute a city edition | Operations | Product, Commercial, Editorial, Tech / Engineer, Finance / Treasury, Legal / Compliance, Reality Checker |
| Weekly CEO Review | Review pipeline and priorities | Orchestrator | All agents |
| Reality Check | Verify claims and reduce risk | Reality Checker | Any requesting agent; Legal / Compliance when legal exposure exists |
| Inbound Email Triage | Classify and route inbound messages | Orchestrator | Commercial, Editorial, Operations, Media / Distribution, Franchisee Manager, Legal / Compliance |
| Outbound Campaign | Run controlled outbound at scale | Commercial | Market Intelligence, Media / Distribution, Legal / Compliance, Reality Checker, Orchestrator |
| Invoice Reconciliation | Invoice confirmed deals and reconcile payments | Finance / Treasury | Commercial, Operations, Legal / Compliance, Orchestrator |
| Contract Legal Review | Draft and review agreement templates and risky terms | Legal / Compliance | Commercial, Finance / Treasury, Product, Franchisee Manager, Reality Checker |
| Media Distribution | Distribute approved content and manage media cadence | Media / Distribution | Editorial, Commercial, Legal / Compliance, Reality Checker |
| Edition Playbook | Define and update the YieldWeek edition standard | Product | Operations, Editorial, Commercial, Badge Certification, Franchisee Manager, Orchestrator |
| Technical Infrastructure | Maintain websites, payments, Luma, and data architecture | Tech / Engineer | Operations, Finance / Treasury, Product, Legal / Compliance, Orchestrator |
| Franchisee Qualification | Monitor and qualify franchisee opportunities | Franchisee Manager | Product, Legal / Compliance, Commercial, Reality Checker, Orchestrator |

## Standard workflow file structure

Each workflow should include:

1. Purpose
2. Trigger
3. Agents involved
4. Inputs
5. Steps
6. Human approval points
7. Outputs
8. Escalation rules
9. Success metrics
