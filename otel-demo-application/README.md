# OTel Demo Application

Explore application, service, and telemetry behavior for the OpenTelemetry Astronomy Shop demo application. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Logs Overview:** panels include Total Logs, Error Logs, and Most Errored Service.
- **Traces Overview:** panels include Total Traces, Total Spans, Trace Services, Error Spans, Longest Span From Service, and Trace With Highest Number Of Spans, plus related signals.
- **Metrics Overview:** panels include Total Metric Points and Total Unique Metrics.
- **Trace Performance:** panels include Span Volume by Service, Latency p95 by Service, Top Services by Span Count, Top Operations, and Slowest Spans.
- **Logs & Errors:** panels include Trace Errors Over Time, Log Volume by Severity, Recent Error Logs, Log Volume by Service, Log Error Rate Over Time, and Exception Types, plus related signals.
- **HTTP:** panels include HTTP Server p95 Latency (PromQL), HTTP Status Mix, and Top HTTP Routes.
- **Business Metrics:** panels include Orders, Total Revenue, Payment Card Types, and Orders Over Time.
- **Runtime Metrics:** panels include Process CPU Rate (PromQL), Process Memory by Service (PromQL), Metric Samples by Family, JVM Memory Used by Service, HTTP Metric Status Mix, and Runtime Concurrency.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `astronomy-shop-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `astronomy-shop-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |
| Metrics | `astronomy-shop-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

3 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Logs Dataset, Traces Dataset, and Metrics Dataset

## Dashboard contents

- **37 tiles** across **8 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/otel-demo-application/assets)
- Importable template: [`otel-demo-application-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/otel-demo-application/otel-demo-application-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
