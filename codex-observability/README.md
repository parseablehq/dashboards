# Codex Observability

Monitor Codex sessions, conversation turns, token and cache usage, estimated cost, latency, tools, MCP activity, approvals, errors, logs, and traces. The dashboard uses SQL across OpenTelemetry logs, traces, and metrics.

## What the dashboard shows

- **Overview:** sessions, turns, tokens, tool calls, cache utilization, tool success, latency, time to first token, and total estimated cost.
- **Adoption & Activity:** session and turn activity, active conversations, model adoption, client version, and terminal inventory.
- **Tokens & Cache:** token composition, model usage, cache trends, and highest-token turns.
- **Cost & FinOps:** total, average, and P95 estimated cost, pricing coverage, cost trends, cumulative cost, model efficiency, and expensive turns.
- **Performance & Latency:** latency percentiles, time to first token, model performance, and slowest turns.
- **Tools & MCP:** tool outcomes, reliability, latency, recent failures, and MCP activity.
- **Safety & Approvals:** approval activity, tool decisions, sandbox policies, and sandbox outcomes.
- **Logs & Errors:** structured events, event distribution, and recent errors.
- **Trace Explorer:** recent turn traces and error spans.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `codex-logs` | SQL | Structured Codex events and error investigation |
| Traces | `codex-traces` | SQL | Sessions, turns, model usage, tools, tokens, cost, and latency |
| Metrics | `codex-metrics` | SQL | Operational telemetry and metric inventory |

Dataset names can be changed after import through dashboard variables.

## Filters

6 dashboard variables provide dataset and scope selection:

- Dataset selectors: Logs Dataset, Traces Dataset, and Metrics Dataset
- Scope filters: Service, Model, and App Version

## Dashboard contents

- **47 tiles** across **9 collapsible sections**
- SQL panels over Parseable datasets
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/codex-observability/assets)
- Importable template: [`codex-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/codex-observability/codex-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving Codex telemetry.
