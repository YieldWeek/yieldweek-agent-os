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

If a task does not support paid badge sales, sponsor conversion, category credibility, city edition execution, or risk control, it is out of scope for v1.

## Human approval required

Agents may recommend, draft, classify, summarize, and prepare. They may not independently:

- approve final badge certification
- change pricing
- sign contracts
- confirm partnerships
- publish public claims
- commit spend
- promise attendee access or sponsor exclusivity
- represent YieldWeek legally

See `governance/approval_rules.md`, `governance/email_autonomy_policy.md`, and `governance/external_identity_policy.md` for detailed rules.
