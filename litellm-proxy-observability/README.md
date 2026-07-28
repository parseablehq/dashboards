# LiteLLM Proxy Observability

Prism dashboard template for LiteLLM proxy traces and metrics.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `litellm-proxy-observability-mixed.json` | LiteLLM Proxy Observability | 42 |

## LiteLLM Proxy Observability

**File:** `litellm-proxy-observability-mixed.json`

Monitor LiteLLM proxy traffic, reliability, latency, token usage, spend, model behavior, deployment health, and request traces using OpenTelemetry traces and PromQL metrics.

**Source:** `Mixed`

**Tags:** `litellm`, `llm`, `genai`, `metrics`, `traces`, `promql`, `observability`

**Filter variables:** `trace_dataset`, `metrics_dataset`

**Panels:**

- Requests
- Trace Error Rate
- Total Tokens
- Total Spend
- Avg Request Latency
- P95 Request Latency
- P95 Time to First Token
- In-flight Requests
- Request Volume by Model
- Proxy Request Rate by Model & Status
- Request vs Failure Rate
- Failures by Exception
- Deployment State
- Trace Errors Over Time
- Request Rate by Route
- LLM API Latency Percentiles
- Total Request Latency Percentiles
- Time to First Token Percentiles
- Queue Time Percentiles
- Trace Request Latency
- Latency by Model
- Input Tokens
- Output Tokens
- Avg Cost per LLM Call
- Avg Tokens per LLM Call
- Token Rate by Model
- Spend Rate by Model
- Token Consumption Over Time
- Cost by Model Over Time
- Cost by Model
- Spend by User
- Model Distribution
- Provider Distribution
- Finish Reasons
- Model Performance & Cost
- Service & SDK Inventory
- Streaming vs Non-streaming
- Recent Request Traces
- Recent LLM Calls
- Recent Errors
- Slowest Requests
- Recent Span Timeline Data
