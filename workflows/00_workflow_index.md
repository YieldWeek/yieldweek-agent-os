# YieldWeek Workflow Index

This folder defines how YieldWeek agents work together.

Agents define roles.
Playbooks define business logic.
Workflows define execution sequences.
Governance defines approval and risk constraints.

## Core workflows

| Workflow | Purpose | Primary Agent | Supporting Agents |
|---|---|---|---|
| City Market Map | Map a city edition opportunity | Market Intelligence | Editorial, Reality Checker |
| Type A Badge Sales | Convert event organisers into paid badge partners | Commercial | Market Intelligence, Badge Certification, Reality Checker, Orchestrator |
| Sponsor Sales | Convert sponsors into paid edition sponsors | Commercial | Market Intelligence, Editorial, Reality Checker, Orchestrator |
| Editorial Content | Produce category-building content | Editorial | Market Intelligence, Reality Checker |
| Speaker Invitation | Identify and invite speakers | Editorial | Market Intelligence, Commercial, Reality Checker |
| Event Operations | Execute a city edition | Operations | Commercial, Editorial, Reality Checker |
| Weekly CEO Review | Review pipeline and priorities | Orchestrator | All agents |
| Reality Check | Verify claims and reduce risk | Reality Checker | Any requesting agent |
| Inbound Email Triage | Classify and route inbound messages | Orchestrator | Commercial, Editorial, Operations |
| Outbound Campaign | Run controlled outbound at scale | Commercial | Market Intelligence, Reality Checker, Orchestrator |

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
