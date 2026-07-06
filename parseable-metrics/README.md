# Parseable Metrics

Prism dashboard template for Parseable service metrics.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `parseable-metrics-promql.json` | Parseable Metrics | 66 |

## Parseable Metrics

**File:** `parseable-metrics-promql.json`

Monitor Parseable service metrics including ingestion, query behavior, storage, runtime health, and system-level PromQL signals. Use it to understand Parseable cluster health and service performance from metrics data.

**Source:** `PromQL`

**Tags:** `metrics`, `parseable`, `promql`

**Filter variables:** `node_type`, `dataset`

**Panels:**

- Total Storage
- Lifetime Events
- Lifetime Ingested
- Staging Files
- Request Rate (All)
- Error Rate (All)
- Request Rate by Status (All)
- Response Code Rate (All)
- Top Endpoint Request Rate (All)
- Object Store Calls by Method (All)
- Storage by Stream
- Storage Trend
- Ingested Events by Stream
- Ingested Size by Stream
- Staging Files by Stream
- Deleted Events by Stream
- Object Store Bytes Scanned
- Storage Requests Inflight (All)
- Process Memory (All)
- Virtual Memory (All)
- Open File Descriptors (All)
- Process Threads (All)
- CPU Seconds Rate (All)
- PromQL Cache Operations (All)
- Request Rate ($node_type)
- Error Rate ($node_type)
- Storage ($node_type)
- Staging Files ($node_type)
- RSS Memory ($node_type)
- CPU Rate ($node_type)
- Request Rate by Status ($node_type)
- Response Code Rate ($node_type)
- Top Endpoint Request Rate ($node_type)
- Storage by Stream ($node_type)
- Events Ingested by Stream ($node_type)
- Events Ingested Size by Stream ($node_type)
- Object Store Calls by Method ($node_type)
- Object Store Bytes Scanned ($node_type)
- Storage Requests Inflight ($node_type)
- Process Memory ($node_type)
- Open FDs / Threads ($node_type)
- CPU Seconds Rate ($node_type)
- Query Calls ($node_type)
- Bytes Scanned in Query ($node_type)
- PromQL Cache Operations ($node_type)
- Files Scanned in Object Store ($node_type)
- Cache Hit Metrics
- Partial Object Store Scans
- Process Limit Metrics ($node_type)
- Process Start Metrics ($node_type)
- Latency p95 Histograms (All)
- Deleted Size Metrics by Stream (All)
- Lifetime Storage Metrics by Stream (All)
- Event Date Metrics - Counts (All)
- Event Date Metrics - Size (All)
- Collection Count Metrics ($node_type)
- Collection Size Metrics ($node_type)
- Parquet Metrics ($node_type)
- Query Scan Metrics ($node_type)
- Latency p95 Histograms ($node_type)
- Latency Histogram Counts ($node_type)
- Latency Histogram Sums ($node_type)
- Top Tenants by Storage
- Top Tenants by Ingested Events
- Request p95 Latency by Endpoint
- File Descriptor Usage Percent
