# Claude Code Usage

Monitor Claude Code sessions, model usage, request patterns, token consumption, and PromQL-backed runtime signals. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Total Cost, API Requests, Sessions, and Errors.
- **Usage & Activity:** API/event activity, active time, lines changed, and code-edit decisions.
- **Models & Tokens:** token trends and breakdowns plus API requests by model.
- **Cost:** cost trends and breakdowns by model and user.
- **Tools & Commands:** panels include Top Tools, Top Hooks, Top Commands, and Plugins.
- **Performance & Reliability:** errors by type and recent errors.
- **Sessions & Users:** recent sessions, session trends, and users.

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

- **24 tiles** across **7 shared coding-agent sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/claude-code-usage/assets)
- Importable template: [`claude-code-usage-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/claude-code-usage/claude-code-usage-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
