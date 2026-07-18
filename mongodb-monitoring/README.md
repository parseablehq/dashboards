# MongoDB Monitoring

Prism dashboard template for MongoDB monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `mongodb-monitoring-mixed.json` | MongoDB Monitoring | 51 |

## MongoDB Monitoring

**File:** `mongodb-monitoring-mixed.json`

Monitor MongoDB connections, operations, storage, collections, WiredTiger cache, replication, logs, traces, and exporter inventory.

**Source:** `Mixed`

**Tags:** `mongodb`, `database`, `metrics`, `logs`, `traces`, `promql`

**Filter variables:** `metrics_dataset`, `logs_dataset`, `traces_dataset`, `server`, `database`, `operation`

**Panels:**

- MongoDB Instances
- Databases
- Current Connections
- Active Connections
- Ops / Sec
- Network Requests / Sec
- Memory Usage
- Replication Lag
- Connections by Type
- Operations by Type
- Operations Over Time
- Document Operations
- Operation Time
- Network IO
- Asserts by Type
- Data Size by Database
- Storage Size by Database
- Collections by Database
- Index Size by Database
- Index Count by Database
- Object Count by Database
- Collection Latency Ops
- WiredTiger Cache Usage %
- WiredTiger Cache Bytes
- Cache Hit / Miss
- WiredTiger Evictions
- Global Lock Time
- Replica Set State
- Replication Lag by State
- Replication Lag Over Time
- Replica Set Members
- Oplog Window
- MongoDB Log Events
- Warnings / Errors
- Logs Over Time
- Logs by Severity
- Logs by Component
- Recent Warning / Error Logs
- Trace Spans
- Error Spans
- Avg Span Duration
- P95 Span Duration
- Spans Over Time
- Spans by DB Operation
- Span Duration by Collection
- Slow MongoDB Trace Queries
- Exporter Scrape Time
- Exporter Goroutines
- Exporter Heap Alloc
- Metric Inventory
- MongoDB Stream Freshness
