# MongoDB Monitoring

Monitor MongoDB connections, operations, storage, collections, WiredTiger cache, replication, logs, traces, and exporter inventory. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include MongoDB Instances, Databases, Current Connections, Active Connections, Ops / Sec, and Network Requests / Sec, plus related signals.
- **Connections & Operations:** panels include Connections by Type, Operations by Type, Operations Over Time, Document Operations, Operation Time, and Network IO, plus related signals.
- **Storage & Collections:** panels include Data Size by Database, Storage Size by Database, Collections by Database, Index Size by Database, Index Count by Database, and Object Count by Database, plus related signals.
- **WiredTiger & Cache:** panels include WiredTiger Cache Usage %, WiredTiger Cache Bytes, Cache Hit / Miss, WiredTiger Evictions, and Global Lock Time.
- **Replication:** panels include Replica Set State, Replication Lag by State, Replication Lag Over Time, Replica Set Members, and Oplog Window.
- **Logs:** panels include MongoDB Log Events, Warnings / Errors, Logs Over Time, Logs by Severity, Logs by Component, and Recent Warning / Error Logs.
- **Traces:** panels include Trace Spans, Error Spans, Avg Span Duration, P95 Span Duration, Spans Over Time, and Spans by DB Operation, plus related signals.
- **Exporter & Inventory:** panels include Exporter Scrape Time, Exporter Goroutines, Exporter Heap Alloc, Metric Inventory, and MongoDB Stream Freshness.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `mongodb-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `mongodb-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `mongodb-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

6 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: MongoDB Metrics Dataset, MongoDB Logs Dataset, and MongoDB Traces Dataset
- Scope filters: Server, Database, and Operation

## Dashboard contents

- **51 tiles** across **8 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/mongodb-monitoring/assets)
- Importable template: [`mongodb-monitoring-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/mongodb-monitoring/mongodb-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
