# LiteLLM SDK Observability

Monitor LiteLLM SDK calls, reliability, latency, TTFT, token usage, spend, models, providers, correlated logs, traces, and metric health. It uses SQL across OpenTelemetry logs, traces, and metrics so correlated SDK behavior can be investigated in one place.

## What the dashboard shows

- **Overview:** panels include LLM Calls, Success Rate, Errors, Total Tokens, Total Spend, and Average Latency, plus related signals.
- **Traffic & Reliability:** panels include Calls, Successes & Errors, Errors by Type, HTTP Status Codes, Scenario Outcomes, and Provider Reliability.
- **Performance & Latency:** panels include Latency Percentiles, SDK vs Provider Latency (Native Metrics), Streaming TTFT & Time per Output Token, Latency by Model, and Slowest LLM Calls.
- **Tokens & Cost:** panels include Token Consumption, Input vs Output Tokens, Spend by Model Over Time, and Model Economics.
- **Cost & FinOps:** panels include Estimated Cost, Recorded Cost, Average Cost per Request, Pricing Coverage, cost trends, model efficiency, unpriced models, and the most expensive requests.
- **Models & Usage:** panels include Model Distribution, Provider Distribution, Streaming Mix, Scenario Mix, and Service & SDK Inventory.
- **Logs:** panels include Logs by Severity, SDK Log Events, Recent SDK Request/Response Logs, Recent Error Logs, and Logs with Trace Context.
- **Trace Explorer:** panels include Recent LLM Calls, Error Traces, Scenario Trace Roots, and Recent Span Timeline Data.
- **Metrics & Telemetry:** panels include Latest Native Metric Rollup, Metric Export Volume, and Metric & Instrumentation Inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `litellm-sdk-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `litellm-sdk-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |
| Metrics | `litellm-sdk-metrics` | SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

8 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Logs Dataset, Traces Dataset, and Metrics Dataset
- Scope filters: Service, Environment, Request Model, Provider, and Log Level

## Dashboard contents

- **50 tiles** across **9 collapsible sections**
- SQL panels over Parseable datasets
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/litellm-sdk-observability/assets)
- Importable template: [`litellm-sdk-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/litellm-sdk-observability/litellm-sdk-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
