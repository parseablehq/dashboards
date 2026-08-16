# Modal Observability

Monitor Modal application logs, traces, function and container capacity, CPU, memory, GPU, input events, latency, errors, and correlated telemetry. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Total Logs, Total Traces, Total Inputs, Avg Input Duration, Running Containers, and Trace Error Rate, plus related signals.
- **Capacity & Utilization:** panels include CPU Utilization, Memory Utilization, Memory Usage MB, Running Containers, Pending Inputs, and Running Inputs, plus related signals.
- **GPU:** panels include GPU Compute Utilization, GPU Memory Utilization, GPU Memory Usage MB, GPU Power Usage, GPU Power Utilization, and GPU Temperature.
- **Input Events:** panels include Input Event Counts, Elapsed Time ms, Queue Time ms, Coldstart Time ms, and Demo Work Duration ms.
- **Traces:** panels include Spans Over Time, Trace Latency, Trace Errors Over Time, Span Performance Summary, and Recent Trace Detail.
- **Logs:** panels include Logs by Level, Logs by Function, Recent Error Logs, and Recent Logs.
- **Inventory:** panels include Core Modal Metric Coverage, Function Metric Series, and Service Inventory.
- **Correlation:** panels include Logs with Trace Context and Function Metric Rollup.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `modal-logs` | SQL | Modal application logs for activity, severity, errors, functions, and recent-event investigation |
| Traces | `modal-traces` | SQL | Spans for function latency, errors, operations, performance, and trace investigation |
| Metrics | `modal-metrics` | PromQL | Modal container, function, input-event, CPU, memory, GPU, and runtime metrics |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry and Modal telemetry conventions. Dataset names can be changed after import through dashboard variables.

## Filters

3 dashboard variables let users select the telemetry sources used by every panel:

- Dataset selectors: Logs Dataset, Traces Dataset, and Metrics Dataset

## Dashboard contents

- **40 tiles** across **8 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/modal-observability/assets)
- Importable template: [`modal-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/modal-observability/modal-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving Modal telemetry.
