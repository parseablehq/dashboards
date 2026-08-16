# OpenRouter Observability

Monitor OpenRouter requests, routing, reliability, provider attempts, retries, latency, tokens, cache usage, cost, models, and traces using SQL over OpenTelemetry trace data.

## What the dashboard shows

- **Overview:** request volume, final success, failed provider attempts, retries, tokens, total cost, latency, and cache utilization.
- **Traffic & Reliability:** request outcomes, model traffic, finish reasons, provider attempts, and reliability by model.
- **Performance & Latency:** request and provider latency, model latency, and slowest requests.
- **Tokens & Cost:** token consumption, cost trends, model cost, token composition, and cache utilization.
- **Cost & FinOps:** estimated and recorded cost, average request cost, pricing coverage, cost trends, model efficiency, unpriced models, and expensive requests.
- **Models & Routing:** model adoption, provider routing, and model/provider pricing inventory.
- **Trace Explorer:** recent requests, failed provider attempts, expensive requests, and retry traces.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `openrouter-traces` | SQL | Requests, provider attempts, retries, latency, tokens, costs, routing, and trace investigation |

The dataset name can be changed after import through the dashboard variable.

## Filters

5 dashboard variables provide dataset and scope selection:

- Dataset selector: Traces Dataset
- Scope filters: Model, Provider, API Key, and Finish Reason

## Dashboard contents

- **40 tiles** across **7 collapsible sections**
- SQL panels over OpenTelemetry traces
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/openrouter-observability/assets)
- Importable template: [`openrouter-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/openrouter-observability/openrouter-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the trace dataset variable to the dataset receiving OpenRouter telemetry.
