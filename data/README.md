# Data Model

The `data/` folder is the source-of-truth operating layer for YieldWeek Agent OS.

## Structure

- `target_cities.csv`: launch-city pipeline and edition planning.
- `crm/`: normalized CRM and operating tables used by agents.
- `legacy/`: deprecated flat CSVs retained for migration history only.

## Operating rules

1. Every CRM record must have a unique ID in `YW-XXX-XXXX` format.
2. Agents must write to approved tables only, as defined in `governance/crm_write_policy.md`.
3. Every external-facing record must include `source`, `source_url` where available, and `source_confidence`.
4. Agents must not create duplicate accounts, contacts, events, or opportunities.
5. Every external email sent or received must create an `interactions.csv` entry.
6. Any high-risk issue must create or update a `risks.csv` entry.

## Canonical IDs

| Object | Prefix | Example |
|---|---|---|
| Account | YW-ACC | YW-ACC-0001 |
| Contact | YW-CON | YW-CON-0001 |
| Opportunity | YW-OPP | YW-OPP-0001 |
| Event | YW-EVT | YW-EVT-0001 |
| Interaction | YW-INT | YW-INT-0001 |
| Task | YW-TSK | YW-TSK-0001 |
| Invoice | YW-INV | YW-INV-0001 |
| Risk | YW-RSK | YW-RSK-0001 |
| Media partner | YW-MED | YW-MED-0001 |
| Franchisee | YW-FRA | YW-FRA-0001 |
| Technical item | YW-TEC | YW-TEC-0001 |

## Confidence levels

- `confirmed`: directly verified from primary source or direct communication.
- `inferred`: reasonable inference from available evidence.
- `assumption`: unverified working assumption; cannot support public claims or irreversible decisions.
