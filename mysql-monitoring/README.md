# MySQL Monitoring

Monitor MySQL availability, connections, query throughput, InnoDB storage, locks, table and index I/O, query performance, logs, traces, and telemetry health. The dashboard combines PromQL metrics with SQL-based logs and traces.

## What the dashboard shows

- **Overview:** availability, uptime, connected and running threads, query rate, buffer pool usage, trace latency, and trace errors.
- **Connections & Threads:** thread states, connection attempts, maximum used connections, connection errors, and client network traffic.
- **Query Throughput & Commands:** query rates, command types, handler operations, joins, sorts, and temporary resources.
- **InnoDB Buffer Pool & Storage:** buffer pool capacity, pages, operations, page flushes, log activity, and doublewrites.
- **Locks & Row Operations:** MySQL locks, row locks, row operations, InnoDB operations, and table lock waits.
- **Table & Index I/O:** largest tables, row counts, table I/O, index I/O, and wait time.
- **Query Performance:** statement event rates, top statements by executions and wait time, slow-query volume, and recent slow queries.
- **Logs & Errors:** log volume by source, errors, warnings, and recent MySQL error log records.
- **Traces & Workload:** database span volume, latency percentiles, errors, operation latency, and recent slow spans.
- **Telemetry & Inventory:** active metrics, receiver identity, metric sample rate, and freshness.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `mysql-metrics` | PromQL | MySQL server, InnoDB, connection, query, lock, table, index, and receiver metrics |
| Logs | `mysql-logs` | SQL | Error logs, slow-query logs, query samples, and statement summaries |
| Traces | `mysql-trcaes` | SQL | Instrumented database client spans, latency, errors, and query investigation |

Dataset names can be changed after import through dashboard variables. The default trace dataset keeps the source deployment's `mysql-trcaes` spelling.

## Filters

6 dashboard variables scope relevant panels:

- Dataset selectors: MySQL Metrics Dataset, MySQL Logs Dataset, and MySQL Traces Dataset
- PromQL filters: MySQL Instance, Environment, and Database

## Dashboard contents

- **60 tiles** across **10 collapsible sections**
- **44 PromQL metric tiles** and **16 SQL log/trace tiles**
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/mysql-monitoring/assets)
- Importable template: [`mysql-monitoring-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/mysql-monitoring/mysql-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving MySQL telemetry.
