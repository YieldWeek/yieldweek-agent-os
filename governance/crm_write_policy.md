# CRM Write Policy

This policy defines which agents may create, update, or close records in `data/crm/`.

## General rules

1. Read access is allowed for all agents unless restricted by privacy policy.
2. Write access is limited by table ownership below.
3. Every write must preserve existing IDs and foreign keys.
4. Do not overwrite another agent's field without logging the reason in notes or `interactions.csv`.
5. Do not create duplicate accounts, contacts, events, or opportunities.
6. GDPR fields override commercial workflow: if `do_not_contact=TRUE`, no outbound may be sent.

## Table ownership

| Table | Create owner | Update owners | Restricted fields |
|---|---|---|---|
| `accounts.csv` | Market Intelligence | Commercial, Franchisee Manager | `account_id`, `source_confidence` |
| `contacts.csv` | Market Intelligence | Commercial, Editorial, Legal/Compliance | `gdpr_status`, `do_not_contact` owned by Legal/Compliance |
| `opportunities.csv` | Commercial | Finance/Treasury, Franchisee Manager | `stage=closed_won` requires payment evidence or finance confirmation |
| `events.csv` | Market Intelligence | Badge Certification, Operations, Product | `badge_status` owned by Badge Certification |
| `interactions.csv` | All agents | Orchestrator | No deletion except founder-approved cleanup |
| `tasks.csv` | Orchestrator | Assigned agent | `status=done` requires output or closed reason |
| `invoices.csv` | Finance/Treasury | Finance/Treasury | Refund/cancel requires founder approval |
| `risks.csv` | Reality Checker, Legal, Finance, Tech | Owning risk agent | `status=accepted` requires founder approval for high/critical |
| `media_partners.csv` | Media/Distribution | Commercial, Orchestrator | Partnership status requires founder approval |
| `franchisees.csv` | Franchisee Manager | Product, Legal/Compliance | Active status requires readiness gate |
| `technical_items.csv` | Tech/Engineer | Operations, Product | Critical severity cannot be deleted |

## Deduplication rules

- Accounts: match by website domain first, then exact account name.
- Contacts: match by email first, then LinkedIn URL, then first name + last name + account_id.
- Opportunities: one open opportunity per account/contact/opportunity_type/edition unless explicitly approved.
- Events: match by event website + event name + city.

## Error correction

If an agent creates a duplicate or wrong record:

1. Do not delete silently.
2. Mark the duplicate record as merged/closed where possible.
3. Add a note referencing the canonical record ID.
4. Create a CRM hygiene task if the issue affects multiple records.
