# Codex Observability

Monitor Codex sessions, conversation turns, token and cache usage, estimated cost, latency, tools, MCP activity, approvals, errors, logs, and traces. The dashboard uses SQL across OpenTelemetry logs, traces, and metrics.

## What the dashboard shows

- **Overview:** sessions, turns, tokens, tool calls, cache utilization, tool success, latency, time to first token, and total estimated cost.
- **Usage & Activity:** session and turn activity, active conversations, model adoption, client version, and terminal inventory.
- **Models & Tokens:** token composition, model usage, cache trends, and highest-token turns.
- **Cost:** total, average, and P95 estimated cost, pricing coverage, cost trends, model efficiency, and expensive turns.
- **Tools & Commands:** tool outcomes, MCP activity, approvals, tool decisions, and sandbox policies and outcomes.
- **Performance & Reliability:** latency, structured events, event distribution, and recent errors.
- **Sessions & Users:** recent turn traces and error spans.

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

- **47 tiles** across **7 shared coding-agent sections**
- SQL panels over Parseable datasets
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/codex-observability/assets)
- Importable template: [`codex-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/codex-observability/codex-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving Codex telemetry.
