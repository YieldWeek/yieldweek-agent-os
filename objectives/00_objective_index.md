# Objective Index

This folder defines the measurable operating objectives for YieldWeek Agent OS.

## Objective files

| File | Purpose |
|---|---|
| `company_objective_function.md` | Company-level validation objective and gates |
| `agent_objective_functions.md` | KPI, target, anti-metric, cadence, and data ownership for each agent |
| `workflow_success_metrics.md` | Trigger, done state, and success metric for each workflow |
| `singapore_smell_test_scorecard.md` | Singapore validation scorecard and go/no-go gates |

## Operating rule

No agent should run as a narrator. Each agent must optimize against a measurable objective, write to an approved data table, and expose blockers through `tasks.csv` or `risks.csv`.

## Minimum standard per objective

Each objective must define:

- owner agent
- metric
- numerical target
- anti-metric
- review cadence
- source data table
- escalation trigger
