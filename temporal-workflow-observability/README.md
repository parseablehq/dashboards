# Temporal Workflow Observability

Monitor Temporal workflow executions, activities, task queues, failures, traces, logs, workers, service requests, persistence, and runtime health. The dashboard combines SQL analysis of OpenTelemetry logs and traces with PromQL panels over Temporal metrics.

## What the dashboard shows

- **Overview:** workflow and activity executions, completion and failure counts, success rate, workflow types, and task queues.
- **Workflows & Reliability:** workflow volume, outcomes, execution summaries, failures, retries, duration, and state transitions.
- **Activities:** activity volume, outcomes, summaries, and event details.
- **Task Queues & Runtime:** task-queue and namespace activity, service/SDK inventory, and queue inventory.
- **Event Performance & Traces:** span volume, duration trends, operation performance, status, and recent spans.
- **Logs & Errors:** log volume, severity, workflow errors, event distribution, and recent log details.
- **Temporal Metrics Overview:** scrape health, completed workflows, successful activities, workflow latency, worker slots, backlog, and poll timeouts.
- **Workers, Task Queues & Server Metrics:** worker capacity, pollers, polling rates, queue backlog, service latency, persistence, heap memory, goroutines, and metric inventory.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `temporal-traces` | SQL | Workflow, activity, event, operation, latency, status, and trace investigation |
| Logs | `temporal-logs` | SQL | Workflow state changes, Temporal events, errors, and runtime logs |
| Metrics | `temporal-metrics` | PromQL and SQL | Workflow, activity, worker, task-queue, service, persistence, and runtime metrics |

## Filters

3 dashboard variables select the telemetry datasets:

- Temporal Traces Dataset
- Temporal Logs Dataset
- Temporal Metrics Dataset

## Dashboard contents

- **57 tiles** across **8 collapsible sections**
- **35 SQL tiles** and **22 PromQL tiles**
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/temporal-workflow-observability/assets)
- Importable template: [`temporal-workflow-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/temporal-workflow-observability/temporal-workflow-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the three dataset variables to the datasets receiving Temporal traces, logs, and metrics.
