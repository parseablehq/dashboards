# n8n Workflow Observability

Monitor n8n workflow and node executions from OpenTelemetry traces. It uses SQL panels to analyze `workflow.execute` and `node.execute` spans directly from the selected Parseable trace dataset.

## What the dashboard shows

- **Overview:** total workflow executions, success rate, failed executions, and average workflow duration.
- **Executions:** execution volume over time by workflow and status, and workflow breakdown by name and outcome.
- **Nodes:** slowest nodes by average duration, and node execution count by type.
- **Detail:** per-execution summary table (status, mode, duration, last seen), and a recent errors table.

## Data used

| Signal | Default dataset | Query language | Purpose                                                  |
| ------ | --------------- | -------------- | -------------------------------------------------------- |
| Traces | `n8n-traces`    | SQL            | OpenTelemetry spans for n8n workflow and node executions |

The template expects traces produced by n8n's native OpenTelemetry integration (`N8N_OTEL_ENABLED=true`) and exported to Parseable via an OpenTelemetry Collector over OTLP/HTTP. Important fields include:

- `span_name` (`workflow.execute` or `node.execute`)
- `n8n.workflow.id`, `n8n.workflow.name`
- `n8n.node.id`, `n8n.node.name`, `n8n.node.type`
- `n8n.execution.id`, `n8n.execution.status`, `n8n.execution.mode`
- `span_duration_ns`, `span_status_code`, `p_timestamp`

See [Parseable's n8n integration docs](https://www.parseable.com/docs/ingest-data/ai-agents/n8n) for the collector setup. Note: n8n's native OpenTelemetry support currently covers traces only — metrics are still under development and logs require a separate collection path (e.g. a filelog receiver).

## Filters

1 dashboard variable lets users select the telemetry source:

- Dataset selector: n8n Traces Dataset

## Dashboard contents

- **10 tiles** in 1 section
- SQL panels over n8n's OpenTelemetry trace fields
- Importable template: [`n8n-workflow-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/n8n-workflow-observability/n8n-workflow-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map **n8n Traces Dataset** to the dataset receiving n8n OpenTelemetry traces. The default is `n8n-traces`.
