# YieldWeek Agent OS

YieldWeek Agent OS is the internal operating system for building, coordinating, and governing the agent-assisted workflows behind YieldWeek.

The system is intentionally narrow. It is not a generic AI agency. It exists to help validate and operate YieldWeek through disciplined agent roles, workflows, playbooks, templates, data tables, and governance rules.

## Current business objective

Validate the first YieldWeek launch markets, starting with Singapore and Hong Kong.

Primary validation gates:

- 10 paid Type A badge listings
- 4 founding sponsors
- credible event organiser pipeline
- first city edition calendar
- repeatable badge certification process
- invoice and reconciliation process live before first payment
- badge and sponsor agreement templates ready before first close
- Singapore edition format documented as the v1 playbook baseline
- technical stack and attendee data handling approved before registration opens

## Agent roster

### Core validation agents

- `00_orchestrator.md` — routes work, manages priorities, escalates decisions
- `01_market_intelligence.md` — maps cities, events, sponsors, organisers, speakers, and source-backed targets
- `02_badge_certification.md` — protects badge quality and scores Type A event candidates
- `03_commercial.md` — drives sponsor and badge sales pipeline
- `04_editorial.md` — creates category narrative, agenda themes, and speaker/content drafts
- `05_operations.md` — executes event operations, run-of-show, Luma, venues, and logistics
- `06_reality_checker.md` — verifies claims and blocks unsupported or risky outputs

### Operating layer agents

- `07_finance_treasury.md` — invoices, reconciles payments, tracks cash and expenses
- `08_legal_compliance.md` — flags legal/compliance risk, templates agreements, tracks entity and data gates
- `09_media_distribution.md` — distributes approved content and manages media/channel cadence
- `10_product.md` — owns edition format, attendee experience, and playbook standard
- `11_tech_engineer.md` — maintains websites, payment integrations, Luma technical setup, and data architecture
- `12_franchisee_manager.md` — monitors and later develops franchisee opportunities after playbook readiness

## Repository model

```text
yieldweek-agent-os/
  agents/      = who does the work
  workflows/   = how work moves across agents
  playbooks/   = business strategy and operating rules
  templates/   = reusable output formats
  data/        = source-of-truth tables
  governance/  = approval, risk, identity, and escalation policies
```

## Core operating principle

If a task does not support paid badge sales, sponsor conversion, category credibility, city edition execution, financial control, legal/compliance safety, product replicability, technical reliability, or risk control, it is out of scope for v1.

## Human approval required

Agents may recommend, draft, classify, summarize, and prepare. They may not independently:

- approve final badge certification
- change pricing
- sign contracts
- confirm partnerships
- publish public claims
- commit spend
- issue refunds
- modify invoice or payment terms
- promise attendee access or sponsor exclusivity
- represent YieldWeek legally
- approve franchise terms
- change public-facing website content without the required content/product review
- access or share attendee data outside the approved data handling policy

See `governance/approval_rules.md`, `governance/email_autonomy_policy.md`, `governance/external_identity_policy.md`, and `governance/legal_escalation_rules.md` for detailed rules.
