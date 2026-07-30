# LiteLLM Proxy Observability

Monitor LiteLLM proxy traffic, reliability, latency, token usage, spend, model behavior, deployment health, and request traces. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Requests, Trace Error Rate, Total Tokens, Total Spend, Avg Request Latency, and P95 Request Latency, plus related signals.
- **Traffic & Reliability:** panels include Proxy Request Rate by Model & Status, Request vs Failure Rate, Failures by Exception, Deployment State, Trace Errors Over Time, and Request Rate by Route.
- **Latency:** panels include LLM API Latency Percentiles, Total Request Latency Percentiles, Time to First Token Percentiles, Queue Time Percentiles, Trace Request Latency, and Latency by Model.
- **Tokens & Cost:** panels include Input Tokens, Output Tokens, Avg Cost per LLM Call, Avg Tokens per LLM Call, Token Rate by Model, and Spend Rate by Model, plus related signals.
- **Models & Usage:** panels include Model Distribution, Provider Distribution, Finish Reasons, Model Performance & Cost, Service & SDK Inventory, and Streaming vs Non-streaming.
- **Trace Explorer:** panels include Recent Request Traces, Recent LLM Calls, Recent Errors, Slowest Requests, and Recent Span Timeline Data.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `litellm-proxy-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |
| Metrics | `litellm-proxy-metrics` | PromQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

2 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Trace Dataset and Metrics Dataset

## Dashboard contents

- **42 tiles** across **6 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Screenshot assets directory: [`assets/`](assets/)
- Importable template: [`litellm-proxy-observability-mixed.json`](litellm-proxy-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
