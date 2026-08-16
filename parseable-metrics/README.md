# Parseable Metrics

Monitor Parseable service metrics including ingestion, query behavior, storage, runtime health, and system-level PromQL signals. It uses PromQL panels for time-series monitoring, breakdowns, and operational inventory.

## What the dashboard shows

- **Overview:** panels include Total Storage, Lifetime Events, Lifetime Ingested, Staging Files, Request Rate (All), and Error Rate (All), plus related signals.
- **HTTP Requests:** panels include Request Rate by Status (All), Response Code Rate (All), Request Rate ($node_type), Request Rate by Status ($node_type), Response Code Rate ($node_type), and Top Endpoint Request Rate ($node_type).
- **Storage & Ingestion:** panels include Storage by Stream, Storage Trend, Ingested Events by Stream, Ingested Size by Stream, Deleted Events by Stream, and Storage ($node_type), plus related signals.
- **Object Store:** panels include Object Store Calls by Method (All), Object Store Bytes Scanned, Object Store Calls by Method ($node_type), Object Store Bytes Scanned ($node_type), Files Scanned in Object Store ($node_type), and Partial Object Store Scans.
- **Process Resources:** panels include Process Memory (All), Virtual Memory (All), Open File Descriptors (All), Process Threads (All), CPU Seconds Rate (All), and RSS Memory ($node_type), plus related signals.
- **Query & Cache:** panels include PromQL Cache Operations (All), Query Calls ($node_type), Bytes Scanned in Query ($node_type), PromQL Cache Operations ($node_type), Cache Hit Metrics, and Query Scan Metrics ($node_type).
- **Latency & Histograms:** panels include Latency p95 Histograms (All), Latency p95 Histograms ($node_type), Latency Histogram Counts ($node_type), Latency Histogram Sums ($node_type), and Request p95 Latency by Endpoint.
- **Tenants:** panels include Top Tenants by Storage and Top Tenants by Ingested Events.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `parseable-metrics` | PromQL | Parseable service, ingestion, storage, query, cache, latency, process, and tenant metrics |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

2 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Dataset
- Scope filters: Node Type

## Dashboard contents

- **66 tiles** across **8 collapsible sections**
- PromQL panels over metric datasets
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/parseable-metrics/assets)
- Importable template: [`parseable-metrics-promql.json`](https://github.com/parseablehq/dashboards/blob/main/parseable-metrics/parseable-metrics-promql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
