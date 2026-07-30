# Redis Monitoring

Monitor Redis availability, clients, command throughput, memory, keyspace, persistence, replication, network, CPU, logs, traces, and exporter health. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Redis Availability, Redis Instances, Connected Clients, Commands / sec, Memory Usage %, and Keyspace Hits / sec, plus related signals.
- **Clients & Commands:** panels include Clients by Role, Blocked Clients, Connections Received / sec, Rejected Connections / sec by Role, Command Throughput by Role, and Command Failures by Command, plus related signals.
- **Memory & Keyspace:** panels include Memory Used, Memory Peak, Memory RSS, Fragmentation Ratio, Keys by DB, and Expiring Keys by DB, plus related signals.
- **Persistence & Replication:** panels include Connected Replicas, Master Link Up, Replication Offset, RDB Changes Since Last Save, Latest Fork Duration, and RDB Saves / sec, plus related signals.
- **Network & CPU:** panels include Network Input / sec, Network Output / sec, Redis CPU User / sec, Redis CPU Sys / sec, Process RSS Memory, and Process CPU / sec, plus related signals.
- **Logs:** panels include Log Records, Logs by Category, Redis Commands in Logs, Auth and Error-like Logs, and Recent Redis Logs.
- **Traces:** panels include Trace Spans, Error Spans, p95 Span Duration, Spans by Operation, Span Status, and Latency by Operation, plus related signals.
- **Exporter & Inventory:** panels include Exporter Scrape Errors, Exporter Scrapes / sec, Target Up, Scrape Samples, Metric Families by Prefix, and Redis Instances Inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `redis-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `redis-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `redis-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

6 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Redis Metrics Dataset, Redis Logs Dataset, and Redis Traces Dataset
- Scope filters: Release, Redis Role, and Instance

## Dashboard contents

- **57 tiles** across **8 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](assets/)
- Importable template: [`redis-monitoring-mixed.json`](redis-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
