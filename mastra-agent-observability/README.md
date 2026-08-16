# Mastra Agent Observability

Monitor Mastra agent runs, reliability, model calls, token usage, estimated cost, tool activity, latency, logs, traces, and native metrics. The dashboard combines SQL analysis of OpenTelemetry logs and traces with PromQL panels over Mastra metrics.

## What the dashboard shows

- **Overview:** agent runs, success rate, model and tool calls, tokens, estimated cost, and P95 agent latency.
- **Agent Activity & Reliability:** run volume, agent outcomes, span types, and per-agent performance.
- **Models, Tokens & Cost:** input, output, and reasoning tokens; token trends; model economics; and estimated cost over time.
- **Tools:** tool call volume, outcomes, errors, and latency.
- **Performance & Latency:** agent latency trends, latency by agent and operation, and slowest runs.
- **Logs & Errors:** log volume, severity distribution, error logs, and recent correlated logs.
- **Trace Explorer:** recent spans, trace summaries, and model-call details.
- **Metrics & Telemetry:** native Mastra tool, model, and duration metrics, an optional application workload counter, and metric inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `mastra-traces` | SQL | Agent, model, and tool spans; latency; outcomes; tokens; and estimated cost |
| Logs | `mastra-logs` | SQL | Correlated agent, tool, runtime, and error logs |
| Metrics | `mastra-metrics` | SQL and PromQL | Mastra duration and token metrics, optional workload metrics, and telemetry inventory |

Estimated-cost panels use Parseable's `agent_cost()` UDF with provider and model normalization. Cost results depend on the provider/model combinations supported by the server's pricing catalog.

## Filters

3 dashboard variables select the telemetry sources:

- Mastra Traces Dataset
- Mastra Logs Dataset
- Mastra Metrics Dataset

## Dashboard contents

- **39 tiles** across **8 collapsible sections**
- **35 SQL tiles** and **4 PromQL tiles**
- Dashboard preview images can be placed in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/mastra-agent-observability/assets)
- Importable template: [`mastra-agent-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/mastra-agent-observability/mastra-agent-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the three dataset variables to the datasets receiving Mastra telemetry. The defaults are `mastra-traces`, `mastra-logs`, and `mastra-metrics`.
