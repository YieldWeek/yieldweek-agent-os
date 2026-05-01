# YieldWeek Email Alias Map

## Purpose

Define the official YieldWeek email aliases, their intended use, and the agents allowed to operate around them.

## Current aliases

| Address | Role | Primary agent | Human approval posture |
|---|---|---|---|
| `team@yieldweek.org` | Central founder / team mailbox | Founder + Orchestrator | Founder approval by default |
| `hello@yieldweek.org` | General inbound | Orchestrator | Agent may triage; sending usually requires approval |
| `partners@yieldweek.org` | Event organisers, badge partners, media partners, city partners, ecosystem partners | Commercial + Market Intelligence | Batch-approved or controlled autonomous only |
| `sponsors@yieldweek.org` | Sponsor conversations, packages, commercial follow-up | Commercial | Batch-approved or controlled autonomous only |
| `editorial@yieldweek.org` | Speakers, agenda, content, interviews, media, newsletter coordination | Editorial | Low-risk coordination may be controlled autonomous after template approval |
| `ops@yieldweek.org` | Logistics, Luma, venues, suppliers, attendee operations, run-of-show execution | Operations | Operational coordination only; spend and commitments require approval |

## Routing rules

- General inbound goes to `hello@yieldweek.org`.
- Sponsor-related conversations go to `sponsors@yieldweek.org`.
- Organiser, badge, media partner, city partner, and ecosystem partner conversations go to `partners@yieldweek.org`.
- Speaker, agenda, content, interview, and media coordination goes to `editorial@yieldweek.org`.
- Event logistics, venues, suppliers, Luma, attendee operations, and run-of-show execution goes to `ops@yieldweek.org`.
- Sensitive, VIP, Tier A, legal, pricing, and founder-accountable conversations go to `team@yieldweek.org`.

## Gmail label recommendation

- `To: hello@yieldweek.org` -> Label: `General`
- `To: partners@yieldweek.org` -> Label: `Partners`
- `To: sponsors@yieldweek.org` -> Label: `Sponsors`
- `To: editorial@yieldweek.org` -> Label: `Editorial`
- `To: ops@yieldweek.org` -> Label: `Ops`
- `To: team@yieldweek.org` -> Label: `Team`

## Security and autonomy rule

Do not give agents direct mailbox passwords.

Agents should operate through approved workflows, scoped connectors, shared inbox permissions, or reviewed draft/send systems.
