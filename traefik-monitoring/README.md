# Traefik Monitoring

Prism dashboard template for Traefik monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `traefik-monitoring-mixed.json` | Traefik Monitoring | 38 |

## Traefik Monitoring

**File:** `traefik-monitoring-mixed.json`

Monitor Traefik ingress traffic, entrypoints, services, latency, TLS certificates, runtime health, access logs, and metric inventory.

**Source:** `Mixed`

**Tags:** `traefik`, `kubernetes`, `ingress`, `promql`, `logs`

**Filter variables:** `metrics_dataset`, `logs_dataset`, `entrypoint`, `service`, `code`, `method`, `protocol`, `pod`

**Panels:**

- Request Rate
- 5xx Rate
- Success %
- Open Connections
- Config Reload Success
- Config Reloads
- Active Certificates
- Requests by Code
- Request Rate by EntryPoint
- Request Bytes by EntryPoint
- Response Bytes by EntryPoint
- Open Connections by EntryPoint
- HTTP Status Mix
- Methods
- Protocols
- Service Request Rate
- Service Errors
- EntryPoint Latency Buckets
- Service Latency Buckets
- Top Services by Samples
- TLS Requests by Version
- TLS Requests by Cipher
- Certificates by CN
- Certificate Expiry
- CPU Usage
- RSS Memory
- Go Heap
- Goroutines
- Open File Descriptors
- FD Usage %
- Access Logs
- 5xx Access Logs
- Logs Over Time
- Access Logs by Status
- Access Logs by Method
- Recent 5xx Access Logs
- Traefik Metric Inventory
- Traefik Pods
