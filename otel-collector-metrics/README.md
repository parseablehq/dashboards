# OTel Collector Metrics

Prism dashboard template for OpenTelemetry Collector monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `otel-collector-metrics-mixed.json` | OTel Collector Metrics | 73 |

## OTel Collector Metrics

**File:** `otel-collector-metrics-mixed.json`

Observe OpenTelemetry Collector throughput, receiver and exporter activity, queue behavior, dropped telemetry, runtime health, signal flow, RPC/HTTP telemetry, and component inventory. Use it to troubleshoot collector pipelines and verify telemetry flow across OTel components.

**Source:** `Mixed`

**Tags:** `otel`, `opentelemetry`, `collector`, `metrics`, `promql`

**Filter variables:** `metrics_dataset`, `receiver`, `processor`, `exporter`, `collector_service`, `service_instance_id`, `transport`

**Panels:**

- Collector Instances
- Receiver Accepted Rate
- Exporter Sent Rate
- Exporter Failure Rate
- CPU Usage %
- RSS Memory %
- Receiver Accepted Spans
- Receiver Accepted Metric Points
- Receiver Accepted Log Records
- Receiver Refused / Failed Items
- Scraped Metric Points
- Scraper Errored Metric Points
- Processor Incoming Items
- Processor Outgoing Items
- Processor Accepted Items
- Avg Processor Internal Duration
- Avg Batch Send Size
- Batch Triggers
- Exporter Sent Spans
- Exporter Sent Metric Points
- Exporter Sent Log Records
- Exporter Send Failures
- Exporter Enqueue Failures
- Exporter Queue Utilization
- Exporter Queue Size
- Exporter Queue Capacity
- Collector CPU by Instance
- Collector RSS Memory
- Runtime Heap Alloc
- Runtime Total Sys Memory
- Runtime Total Alloc
- Collector Uptime
- OTel Collector Metric Inventory
- Active Collector Components
- Receiver Refused Signals
- Receiver Failed Signals
- Exporter Send Failure Signals
- Exporter Enqueue Failure Signals
- Scraper Error Signals
- Queue Saturation Risk
- High CPU Risk
- Receiver Spans Accepted vs Refused
- Receiver Metric Points Accepted vs Refused
- Receiver Log Records Accepted vs Refused
- Processor Spans Incoming vs Outgoing
- Processor Metric Points Incoming vs Outgoing
- Processor Log Records Incoming vs Outgoing
- Processor Spans Accepted / Refused / Dropped
- Processor Metric Points Accepted / Refused / Dropped
- Processor Log Records Accepted / Refused / Dropped
- Batch Send Size Buckets
- Filtered Spans
- Filtered Metric Points
- Filtered Log Records
- Exporter Spans Sent / Failed / Enqueue
- Exporter Metric Points Sent / Failed / Enqueue
- Exporter Log Records Sent / Failed / Enqueue
- CPU Usage Min / Avg / Max
- RSS Memory Min / Avg / Max
- Runtime Sys Memory Min / Avg / Max
- Runtime Heap Memory Min / Avg / Max
- Service Instance Details
- Spans Flow Summary
- Metric Points Flow Summary
- Log Records Flow Summary
- RPC Server Responses by gRPC Status
- RPC Client Responses by gRPC Status
- RPC Server Duration
- RPC Client Duration
- RPC Server Request Size
- RPC Client Request Size
- HTTP Server Request Duration
- HTTP Client Request Duration
