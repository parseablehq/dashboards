# Cloudflare AI Gateway Observability

Monitor Cloudflare AI Gateway request volume, reliability, latency, token usage, cost, models, custom workloads, and individual traces from the gateway's native OpenTelemetry exporter.

## What the dashboard shows

- **Overview:** requests, success rate, errors, tokens, recorded cost, average and P95 latency, active models, and traffic over time.
- **Traffic & Reliability:** volume by model, provider traffic and errors, and workload-level success rates.
- **Performance & Latency:** P50/P95/P99 trends, model and workload latency, and slowest requests.
- **Tokens & Cost:** input/output tokens, per-request averages, trends, and model-level cost efficiency.
- **Models & Workloads:** distributions and comparative model performance.
- **Trace Explorer:** recent requests, recent errors, and grouped trace summaries.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `cf-ai-gateway-traces` | SQL | Native Cloudflare AI Gateway OTLP spans with GenAI semantic-convention attributes |

The dashboard expects Cloudflare fields including `gen_ai.request.model`, `gen_ai.model.provider`, `gen_ai.usage.input_tokens`, `gen_ai.usage.output_tokens`, and `gen_ai.usage.cost`. Custom request metadata such as `workload`, `complexity`, and `source` is optional; unclassified traffic remains visible.

## Filters

- Trace Dataset

## Dashboard contents

- **32 tiles** across **6 collapsible sections**
- SQL-only dashboard backed by native OTLP traces
- Importable template: [`cloudflare-ai-gateway-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/cloudflare-ai-gateway-observability/cloudflare-ai-gateway-observability-sql.json)

## Cloudflare exporter configuration

Configure the AI Gateway OTEL exporter with a Parseable-compatible HTTPS endpoint ending in `/v1/traces`, JSON content type, and these headers:

- `X-API-Key: <parseable-api-key>`
- `X-P-Stream: cf-ai-gateway-traces`
- `X-P-Log-Source: otel-traces`

Do not commit API keys or tunnel URLs to this repository.

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the Trace Dataset variable to the stream receiving Cloudflare AI Gateway traces.
