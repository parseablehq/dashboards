# Mac Host Metrics Dashboard

Monitor macOS host metrics collected through the OpenTelemetry Collector. The dashboard combines PromQL time series with SQL-based telemetry coverage and inventory panels.

## What the dashboard shows

- **Overview:** uptime, load, host count, CPU utilization, and metric value coverage.
- **CPU & Load:** CPU time by state, load averages, and utilization trends.
- **Storage & Filesystem:** disk busy time, operation time, and disk telemetry inventory.
- **Collector & Metric Inventory:** metric families, active series, samples, reporting hosts, and collector metadata.
- **Telemetry Coverage:** value availability, component samples, missing-value families, memory states, network interfaces, and filesystem labels.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `dataset-leog53o6` | PromQL / SQL | macOS host performance, inventory, collector health, and telemetry coverage |

Expected fields follow OpenTelemetry host metrics conventions, including `metric_name`, `data_point_value`, `host.name`, `state`, `device`, and `mountpoint`.

## Filters

- Metrics dataset
- Host

## Dashboard contents

- **25 tiles** across **5 collapsible sections**
- Importable template: [`mac-host-metrics-dashboard-mixed.json`](mac-host-metrics-dashboard-mixed.json)
- Dashboard assets: [`assets/`](assets/)

## Import

Download the JSON file and use Parseable's dashboard import flow. Map the metrics dataset variable to the dataset receiving macOS host metrics.
