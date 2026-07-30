# LiteLLM SDK Observability

Prism dashboard template for LiteLLM SDK OpenTelemetry logs, traces, and metrics.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `litellm-sdk-observability-sql.json` | LiteLLM SDK Observability | 40 |

## LiteLLM SDK Observability

**File:** `litellm-sdk-observability-sql.json`

Monitor LiteLLM SDK calls, reliability, latency, time to first token, token usage, spend, model and provider behavior, correlated logs, traces, and OpenTelemetry metric health.

**Source:** `SQL`

**Tags:** `litellm`, `sdk`, `llm`, `genai`, `opentelemetry`, `logs`, `traces`, `metrics`, `observability`

**Filter variables:** `logs_dataset`, `traces_dataset`, `metrics_dataset`, `service`, `environment`, `model`, `provider`, `severity`

**Panels:**

- LLM Calls
- Success Rate
- Errors
- Total Tokens
- Total Spend
- Average Latency
- P95 Latency
- Average TTFT
- LLM Calls by Model & Outcome
- Calls, Successes & Errors
- Errors by Type
- HTTP Status Codes
- Scenario Outcomes
- Provider Reliability
- Latency Percentiles
- SDK vs Provider Latency (Native Metrics)
- Streaming TTFT & Time per Output Token
- Latency by Model
- Slowest LLM Calls
- Token Consumption
- Input vs Output Tokens
- Spend by Model Over Time
- Model Economics
- Model Distribution
- Provider Distribution
- Streaming Mix
- Scenario Mix
- Service & SDK Inventory
- Logs by Severity
- SDK Log Events
- Recent SDK Request/Response Logs
- Recent Error Logs
- Logs with Trace Context
- Recent LLM Calls
- Error Traces
- Scenario Trace Roots
- Recent Span Timeline Data
- Latest Native Metric Rollup
- Metric Export Volume
- Metric & Instrumentation Inventory
