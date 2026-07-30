# Parseable Server Logs

Analyze Parseable server logs, error patterns, request activity, status distribution, and runtime log trends. It uses SQL panels to analyze telemetry directly from the selected Parseable datasets.

## What the dashboard shows

- **Overview:** panels include Total Logs, Error Logs, Warning Logs, and Error Rate.
- **Log Trends:** panels include Log Volume Over Time and Error / Warning Trend.
- **Severity & Components:** panels include Logs by Category, Top Components, and Module Severity Matrix.
- **Error Analysis:** panels include CPU Pressure and Repeated Error Messages.
- **Sources:** panels include Logs by Source IP and Logs by Log File.
- **Recent Logs:** panels include Recent Error Logs.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `azure-prod-parseable-server` | SQL | Parseable server logs for severity, components, errors, sources, trends, and recent-event investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

1 dashboard variable lets users select telemetry sources and scope relevant panels:

- Dataset selectors: Dataset

## Dashboard contents

- **14 tiles** across **6 collapsible sections**
- SQL panels over Parseable datasets
- Dashboard screenshot in [`assets/`](assets/)
- Importable template: [`parseable-server-logs-sql.json`](parseable-server-logs-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
