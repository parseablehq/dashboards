# Baseten Observability

Monitor Baseten Dedicated Inference traffic, latency, concurrency, GPU capacity, pod readiness, logs, errors, and trace hotspots. It combines PromQL metrics with SQL telemetry so model serving behavior can be investigated from one dashboard.

## What the dashboard shows

- **Requests:** panels include incoming inference request rate, model API request rate, request size quantiles, response size quantiles, and request volume by model.
- **Latency & Concurrency:** panels include end-to-end latency, time to first byte, concurrent inference requests, and model API response size quantiles.
- **Capacity & Health:** panels include pod readiness, GPU utilization, GPU memory usage, legacy GPU utilization, scrape samples, and scrape health signals.
- **Trace Hotspots:** panels highlight the most active spans and average span duration from Baseten Truss traces.
- **Logs & Errors Signals:** panels show request volume by model and top log categories from Baseten serving logs.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `baseten-metrics` | PromQL | Baseten deployment metrics for request rate, latency, concurrency, GPU usage, pod readiness, and scrape health |
| Logs | `baseten-logs` | SQL | Baseten serving logs for request volume, model metadata, log categories, and operational events |
| Traces | `baseten-traces` | SQL | Truss built-in spans for request investigation, span hotspots, and latency analysis |

Expected fields, labels, and metric names follow Baseten's OpenTelemetry and Prometheus export conventions. Dataset names can be changed after import through dashboard variables.

## Filters

3 dashboard variables let users select the telemetry sources used by every panel:

- Dataset selectors: Metrics Dataset, Logs Dataset, and Traces Dataset

## Dashboard contents

- **19 tiles** across **5 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/baseten-observability/assets)
- Importable template: [`baseten-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/baseten-observability/baseten-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving Baseten telemetry.
