# GitHub Copilot Observability

Monitor GitHub Copilot traces, sessions, model and token usage, tools, latency, errors, repositories, and recent trace activity. The dashboard uses SQL over OpenTelemetry traces emitted by GitHub Copilot.

## What the dashboard shows

- **Overview:** total traces, spans, sessions, and errors.
- **Trace Activity:** trace volume over time and spans grouped by operation.
- **Models & Tokens:** input and output token totals, calls by model, and token usage by model.
- **Tools:** total tool calls and most-used tools.
- **Latency & Reliability:** average trace duration, model latency, errors by type, and recent errors.
- **Repositories & Sessions:** repository activity and recent trace details.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `copilot-traces` | SQL | Copilot sessions, model calls, tokens, tools, latency, errors, and repository context |

Expected fields follow OpenTelemetry GenAI semantic conventions plus GitHub Copilot attributes. The dataset name can be changed after import through the dashboard variable.

## Filters

1 dashboard variable selects the telemetry source:

- Dataset selector: Traces Dataset

## Dashboard contents

- **18 tiles** across **6 collapsible sections**
- SQL panels over GitHub Copilot OpenTelemetry traces
- Importable template: [`github-copilot-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/github-copilot-observability/github-copilot-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the Traces Dataset variable to the dataset receiving GitHub Copilot traces.
