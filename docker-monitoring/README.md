# Docker Monitoring

Monitor Docker containers with cAdvisor and Prometheus metrics sent to Parseable. The dashboard covers availability, resource usage, network and storage activity, container state, and telemetry health.

## What the dashboard shows

- **Overview:** cAdvisor availability, container count, CPU, memory, network, filesystem throughput, OOM events, and active tasks.
- **CPU & Throttling:** per-container CPU usage, user and system time, load averages, CPU shares, D-state load, and pressure.
- **Memory:** working set, usage and limits, working-set ratio, RSS, cache, swap, failures, OOM events, and pressure.
- **Network:** receive and transmit throughput, packet rate, drops, errors, and interface-level traffic.
- **Storage & Filesystem:** filesystem usage and limits, throughput, IOPS, I/O time, inode utilization, and block-device operations.
- **Container State & Inventory:** task and health state, uptime, freshness, service and project distribution, and container metadata.
- **cAdvisor & Metric Inventory:** scrape health, samples, series, machine capacity, cAdvisor version, sample volume, and metric inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `docker-metrics` | PromQL and SQL | cAdvisor container, machine, scrape-health, and metric-inventory data |

Dataset names can be changed after import through the dashboard variable.

## Filters

5 dashboard variables scope relevant panels:

- Dataset selector: Docker Metrics Dataset
- PromQL filters: Node, Project, Service, and Container

## Dashboard contents

- **50 tiles** across **7 collapsible sections**
- **46 PromQL tiles** and **4 SQL inventory tiles**
- Screenshot assets directory: [`assets/`](assets/)
- Importable template: [`docker-monitoring-mixed.json`](docker-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the metrics dataset variable to the dataset receiving cAdvisor telemetry.
