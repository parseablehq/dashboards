# Hermes Agent Observability

Monitor Hermes Agent invocations, model and token usage, tool activity, latency, errors, logs, traces, and native OpenTelemetry metrics in Parseable.

## What the dashboard shows

- **Agent & Trace Overview:** invocation count, error spans, total LLM tokens, P95 agent latency, model calls, tool outcomes, and recent agent traces.
- **Logs & Errors:** log volume by severity and recent warning/error records with trace correlation fields.
- **Metrics & Usage:** metric inventory, token usage by model, and LLM duration by model.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `hermes-traces` | SQL | Agent, LLM, API, tool, and skill spans; latency; outcomes; and token rollups |
| Logs | `hermes-logs` | SQL | Hermes runtime logs, warnings, errors, and trace correlation |
| Metrics | `hermes-metrics` | SQL | Native Hermes and GenAI token, duration, session, model, tool, retry, and error metrics |

## Filters

Three dashboard variables select the telemetry datasets:

- Hermes Traces
- Hermes Logs
- Hermes Metrics

## Dashboard contents

- **12 SQL tiles** across **3 collapsible sections**
- Importable template: [`hermes-agent-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/hermes-agent-observability/hermes-agent-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the three dataset variables to the datasets receiving Hermes telemetry. The defaults are `hermes-traces`, `hermes-logs`, and `hermes-metrics`.

The template matches telemetry emitted by the [`hermes-otel`](https://github.com/briancaffey/hermes-otel) plugin with traces, logs, and metrics enabled.
