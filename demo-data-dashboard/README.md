# Demo Data Dashboard

Explore sample OpenTelemetry logs, traces, and metrics across application services. The dashboard combines SQL investigations with PromQL runtime and request signals.

## What the dashboard shows

- **Overview:** trace, span, error, latency, log, service, and metric totals.
- **Service Health:** service throughput, errors, latency, health summaries, and instances.
- **HTTP & APIs:** request and error rates, methods, status codes, route latency, throughput, and slow spans.
- **Database & Cache:** database calls, latency, errors, slow spans, cache operations, and hit ratios.
- **Messaging & Dependencies:** dependency calls, latency, errors, messaging operations, DNS, and TLS.
- **Logs & Errors:** service volume, severity, error trends, messages, recent errors, and code locations.
- **Trace Explorer:** span kinds, operations, latency, trace summaries, slow spans, and error spans.
- **Metrics & Runtime:** CPU, memory, requests, queues, database queries, network bytes, threads, pools, and metric inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `otel-demo-logs` | SQL | Service activity, severity, errors, messages, and code locations |
| Traces | `otel-demo-traces` | SQL | Service performance, HTTP, databases, dependencies, messaging, and trace exploration |
| Metrics | `otel-demo-metrics` | PromQL / SQL | Request, runtime, cache, network, and metric inventory signals |

Expected fields and labels follow the dashboard queries and OpenTelemetry semantic conventions.

## Filters

- Logs dataset
- Traces dataset
- Metrics dataset

## Dashboard contents

- **56 tiles** across **8 collapsible sections**
- Importable template: [`demo-data-dashboard-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/demo-data-dashboard/demo-data-dashboard-mixed.json)
- Dashboard assets: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/demo-data-dashboard/assets)

## Import

Download the JSON file and use Parseable's dashboard import flow. Map all three dataset variables to datasets containing compatible demo telemetry.
