# Windows Server Monitoring

An operations dashboard for monitoring Windows Server hosts from one place. It combines PromQL metrics with SQL-based logs and traces so infrastructure health and workload activity can be investigated together.

## What the dashboard shows

- **Overview:** host availability, host count, CPU, memory, disk, processes, running services, uptime, network traffic, errors, and recent events.
- **CPU & System:** utilization, queue length, interrupts, context switches, process count, and system uptime.
- **Memory:** physical and virtual memory usage, available memory, paging, page faults, and pool usage.
- **Disk & Filesystem:** volume capacity, free space, read/write throughput, latency, IOPS, and queue depth.
- **Network & TCP:** interface throughput, packet rates, drops, errors, TCP connections, retransmissions, and connection failures.
- **Services & Processes:** service state, process inventory, resource usage, and process activity.
- **Windows Events:** event volume, levels, providers, channels, event IDs, messages, and recent critical events.
- **Traces & Workload:** trace volume, latency, errors, services, operations, and recent slow or failed spans.
- **Exporter & Inventory:** exporter scrape health, metric inventory, hosts, operating-system details, and telemetry coverage.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `windows-metrics` | PromQL | Windows host, OS, CPU, memory, disk, network, service, process, and exporter metrics |
| Logs | `windows-logs` | SQL | Windows Event Log records and operational log analysis |
| Traces | `windows-traces` | SQL | Workload spans, service latency, errors, and trace investigation |

Expected telemetry follows OpenTelemetry semantic conventions and Windows exporter-style metric labels. Dataset names can be changed after import through dashboard variables.

## Filters

Eight dashboard variables let users scope every relevant panel:

- Metrics, logs, and traces datasets
- Deployment environment
- Service
- Host
- Volume
- Network interface (NIC)

## Dashboard contents

- **62 tiles** across **9 collapsible sections**
- Metrics, logs, and traces in one mixed-source dashboard
- Overview and section-specific screenshots in [`assets/`](assets/)
- Importable template: [`windows-server-monitoring-mixed.json`](windows-server-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving your Windows telemetry.
