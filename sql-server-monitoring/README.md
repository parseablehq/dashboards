# SQL Server Monitoring

Monitor Microsoft SQL Server availability, batch requests, buffer cache, memory, database I/O, TempDB, locks, waits, deadlocks, query logs, traces, and metric inventory. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Batch Requests / sec, Buffer Cache Hit Ratio, Deadlocks / sec, Logins / sec, SQL Compilations / sec, and SQL Recompilations / sec, plus related signals.
- **Connections & Workload:** panels include Batch Request Trend, Login vs Logout Rate, Full Scan Rate, Index Search Rate, Page Lookup Rate, and Queries by Command.
- **Memory & Buffer Cache:** panels include Memory Usage, Buffer Cache Hit Ratio Trend, TempDB Version Store Size, Page Lookup / sec, Compilations / sec, and Recompilations / sec, plus related signals.
- **Database I/O & TempDB:** panels include Database Latency by DB, Resource Pool Disk Operations, Disk Throttled Writes, Replica Data Rate, Transaction Delay, and Mirror Write Rate.
- **Locks, Waits & Deadlocks:** panels include Deadlock Rate, Lock Wait Rate, Lock Timeout Rate, OS Wait Duration, Top Wait Types, and Blocking Sessions, plus related signals.
- **Queries & Logs:** panels include Query Log Records, p95 Query Elapsed, p95 Query CPU, Queries by Database, Queries by User, and Top Query Hashes by Elapsed Time, plus related signals.
- **Traces:** panels include Trace Spans, p95 Span Duration, Spans by Operation, Spans by Query Summary, Trace Latency Trend, and Slowest Spans, plus related signals.
- **Collector & Inventory:** panels include Metric Families, Live SQL Server Metrics, Metric Families by Prefix, Databases Seen, and Metrics Inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `sqlserver-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `sqlserver-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `sqlserver-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

6 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: SQL Server Metrics Dataset, SQL Server Logs Dataset, and SQL Server Traces Dataset
- Scope filters: Environment, Service, and Database

## Dashboard contents

- **53 tiles** across **8 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](assets/)
- Importable template: [`sql-server-monitoring-mixed.json`](sql-server-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
