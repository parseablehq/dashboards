# OTel Collector Metrics

Observe OpenTelemetry Collector throughput, receiver/exporter activity, queue behavior, dropped telemetry, and component inventory. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Collector Instances, Receiver Accepted Rate, Exporter Sent Rate, Exporter Failure Rate, CPU Usage %, and RSS Memory %.
- **Receivers:** panels include Receiver Accepted Spans, Receiver Accepted Metric Points, Receiver Accepted Log Records, Receiver Refused / Failed Items, Scraped Metric Points, and Scraper Errored Metric Points, plus related signals.
- **Processors:** panels include Processor Incoming Items, Processor Outgoing Items, Processor Accepted Items, Avg Processor Internal Duration, Avg Batch Send Size, and Batch Triggers, plus related signals.
- **Filter Processors:** panels include Filtered Spans, Filtered Metric Points, and Filtered Log Records.
- **Exporters:** panels include Exporter Sent Spans, Exporter Sent Metric Points, Exporter Sent Log Records, Exporter Send Failures, Exporter Enqueue Failures, and Exporter Queue Utilization, plus related signals.
- **Runtime:** panels include Collector CPU by Instance, Collector RSS Memory, Runtime Heap Alloc, Runtime Total Sys Memory, Runtime Total Alloc, and Collector Uptime, plus related signals.
- **Signal Flows:** panels include Spans Flow Summary, Metric Points Flow Summary, and Log Records Flow Summary.
- **RPC Server / Client:** panels include RPC Server Responses by gRPC Status, RPC Client Responses by gRPC Status, RPC Server Duration, RPC Client Duration, RPC Server Request Size, and RPC Client Request Size.
- **HTTP Server / Client:** panels include HTTP Server Request Duration and HTTP Client Request Duration.
- **Metric Inventory:** panels include OTel Collector Metric Inventory and Active Collector Components.
- **Alerts & Failure Signals:** panels include Receiver Refused Signals, Receiver Failed Signals, Exporter Send Failure Signals, Exporter Enqueue Failure Signals, Scraper Error Signals, and Queue Saturation Risk, plus related signals.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `astronomy-shop-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

7 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Metrics Dataset
- Scope filters: Receiver, Processor, Exporter, Collector Service, Service Instance, and Transport

## Dashboard contents

- **73 tiles** across **11 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/otel-collector-metrics/assets)
- Importable template: [`otel-collector-metrics-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/otel-collector-metrics/otel-collector-metrics-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
