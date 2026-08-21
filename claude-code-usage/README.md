# Claude Code Usage

Monitor Claude Code sessions, model usage, request patterns, token consumption, and PromQL-backed runtime signals. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Total Cost, API Requests, Sessions, and Errors.
- **Cost & Tokens:** panels include Cost and API Requests Over Time, Tokens Over Time, Token Usage by Type, and Cost by Model.
- **Models & Requests:** panels include API Requests by Model and Events by Type.
- **Tools & Commands:** panels include Top Tools, Top Hooks, Top Commands, and Plugins.
- **Activity & Code Changes:** panels include Active Time Over Time, Lines Changed Over Time, and Code Edit Decisions.
- **Errors:** panels include Errors by Type and Recent Errors.
- **Sessions:** panels include Recent Sessions, Session Count Over Time, and Users.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `claudecode-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Metrics | `claudecode-metrics` | PromQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

2 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Logs Dataset and Metrics Dataset

## Dashboard contents

- **22 tiles** across **7 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/claude-code-usage/assets)
- Importable template: [`claude-code-usage-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/claude-code-usage/claude-code-usage-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
