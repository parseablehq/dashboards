# Postgres Monitoring

Monitor PostgreSQL health, connections, locks, database activity, storage, query performance, replication, WAL, logs, traces, and exporter inventory. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Postgres Up, Databases, Active Connections, Connection Utilization %, Cache Hit Ratio, and Database Size, plus related signals.
- **Connections & Locks:** panels include Connections by State, Connections by Application, Used vs Available Connections, Blocked / Waiting Connections, Locks by Mode, and Wait Events.
- **Database Activity:** panels include Transactions by Database, Rows Changed, Rows Returned / Fetched, Temp Files / Bytes, Database Cache Hit Ratio, and Deadlocks and Conflicts by Database.
- **Storage & Tables:** panels include Database Size by DB, Top Table Sizes, Rows by Table State, Table Bloat Ratio, Index Health, and Sequence Usage.
- **Query Performance:** panels include Statement Calls, Mean Execution Time, Total Execution Time, Statement Cache Hit Ratio, Statement Rows, and Statement WAL Bytes.
- **Replication & WAL:** panels include Replication Lag, WAL Bytes Rate, Checkpoint Age, Archiver Failed, WAL Activity, and Checkpoint Writes.
- **Logs:** panels include Postgres Log Events, Errors / Warnings, Logs Over Time, Logs by Severity, Logs by Database, and Recent Error Logs.
- **Traces:** panels include Trace Spans, Error Spans, Avg Span Duration, P95 Span Duration, Spans Over Time, and Span Duration by Operation, plus related signals.
- **Exporter & Inventory:** panels include Exporter Scrape Success %, Exporter CPU %, Exporter RSS Memory, Metric Inventory, and Postgres Settings.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `postgres-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `postgres-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Traces | `postgres-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

6 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Postgres Metrics Dataset, Postgres Logs Dataset, and Postgres Traces Dataset
- Scope filters: Database, Application, and Server

## Dashboard contents

- **57 tiles** across **9 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/postgres-monitoring/assets)
- Importable template: [`postgres-monitoring-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/postgres-monitoring/postgres-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
