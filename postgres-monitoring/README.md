# Postgres Monitoring

Prism dashboard template for PostgreSQL monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `postgres-monitoring-mixed.json` | Postgres Monitoring | 57 |

## Postgres Monitoring

**File:** `postgres-monitoring-mixed.json`

Monitor PostgreSQL health, connections, locks, database activity, storage, query performance, replication, WAL, logs, traces, and exporter inventory.

**Source:** `Mixed`

**Tags:** `postgres`, `postgresql`, `database`, `metrics`, `logs`, `traces`, `promql`

**Filter variables:** `metrics_dataset`, `logs_dataset`, `traces_dataset`, `database`, `application`, `server`

**Panels:**

- Postgres Up
- Databases
- Active Connections
- Connection Utilization %
- Cache Hit Ratio
- Database Size
- QPS
- Deadlocks + Conflicts
- Connections by State
- Connections by Application
- Used vs Available Connections
- Blocked / Waiting Connections
- Locks by Mode
- Wait Events
- Transactions by Database
- Rows Changed
- Rows Returned / Fetched
- Temp Files / Bytes
- Database Cache Hit Ratio
- Deadlocks and Conflicts by Database
- Database Size by DB
- Top Table Sizes
- Rows by Table State
- Table Bloat Ratio
- Index Health
- Sequence Usage
- Statement Calls
- Mean Execution Time
- Total Execution Time
- Statement Cache Hit Ratio
- Statement Rows
- Statement WAL Bytes
- Replication Lag
- WAL Bytes Rate
- Checkpoint Age
- Archiver Failed
- WAL Activity
- Checkpoint Writes
- Postgres Log Events
- Errors / Warnings
- Logs Over Time
- Logs by Severity
- Logs by Database
- Recent Error Logs
- Trace Spans
- Error Spans
- Avg Span Duration
- P95 Span Duration
- Spans Over Time
- Span Duration by Operation
- Spans by DB Operation
- Slow Trace Queries
- Exporter Scrape Success %
- Exporter CPU %
- Exporter RSS Memory
- Metric Inventory
- Postgres Settings
