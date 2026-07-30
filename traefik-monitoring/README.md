# Traefik Monitoring

Monitor Traefik ingress traffic, entrypoints, services, latency, TLS certificates, runtime health, access logs, and metric inventory. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Request Rate, 5xx Rate, Success %, Open Connections, Config Reload Success, and Config Reloads, plus related signals.
- **EntryPoints & Traffic:** panels include Request Rate by EntryPoint, Request Bytes by EntryPoint, Response Bytes by EntryPoint, Open Connections by EntryPoint, HTTP Status Mix, and Methods, plus related signals.
- **Services & Latency:** panels include Service Request Rate, Service Errors, EntryPoint Latency Buckets, Service Latency Buckets, and Top Services by Samples.
- **TLS & Certificates:** panels include TLS Requests by Version, TLS Requests by Cipher, Certificates by CN, and Certificate Expiry.
- **Runtime & Process:** panels include CPU Usage, RSS Memory, Go Heap, Goroutines, Open File Descriptors, and FD Usage %.
- **Logs:** panels include Access Logs, 5xx Access Logs, Logs Over Time, Access Logs by Status, Access Logs by Method, and Recent 5xx Access Logs.
- **Inventory:** panels include Traefik Metric Inventory and Traefik Pods.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `azure-prod-cluster-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `azure-prod-pod-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

8 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Metrics Dataset and Logs Dataset
- Scope filters: EntryPoint, Service, HTTP Code, Method, Protocol, and Pod

## Dashboard contents

- **38 tiles** across **7 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](assets/)
- Importable template: [`traefik-monitoring-mixed.json`](traefik-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
