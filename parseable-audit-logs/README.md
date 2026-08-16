# Parseable Audit Logs

Review Parseable audit events, user activity, administrative actions, and access patterns from audit log datasets. It uses SQL panels to analyze telemetry directly from the selected Parseable datasets.

## What the dashboard shows

- **Overview:** panels include UI API Calls, UI API Error Calls, UI API Error Rate, UI API Avg Request Size, UI API Distinct Users, and UI API Streams Touched, plus related signals.
- **Request Trends:** panels include UI API Volume Over Time, UI API Error Trend, and UI API Status Class Over Time.
- **Status & Auth:** panels include UI API Status Code Mix, UI API Requests by Method, Auth Methods, Server Mode, and UI API Path Method Status Summary.
- **Users & Streams:** panels include Top UI API Users and Top UI API Streams.
- **API Paths:** panels include Top UI API Paths, Slow APIs, and UI API Call Inventory.
- **Failures:** panels include Top UI API Error Paths, Recent Failed UI API Calls, and UI API Error Details by User.
- **Recent Events:** panels include Recent UI API Calls and User Actions.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Audit logs | `azure-prod-parseable-audit` | SQL | Audit records for users, authentication, API activity, status, and failure investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

2 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Dataset
- Scope filters: Username

## Dashboard contents

- **28 tiles** across **7 collapsible sections**
- SQL panels over Parseable datasets
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/parseable-audit-logs/assets)
- Importable template: [`parseable-audit-logs-sql.json`](https://github.com/parseablehq/dashboards/blob/main/parseable-audit-logs/parseable-audit-logs-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
