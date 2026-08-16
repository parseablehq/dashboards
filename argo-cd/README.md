# Argo CD

Monitor Argo CD applications, sync health, controller activity, Kubernetes API behavior, Redis/cache signals, metrics inventory, and Argo CD logs. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Applications, Healthy Apps, Out Of Sync Apps, Connected Clusters, Orphaned Resources, and Kubectl Retries, plus related signals.
- **Applications:** panels include Applications by Health, Applications by Sync Status, Applications by Project, Applications by Destination Namespace, Out Of Sync Applications, and Apps with Orphaned Resources.
- **Sync & Reconciliation:** panels include Sync Rate by Phase, Sync Duration Rate, Reconcile Duration Buckets, Reconcile Count Rate, Resource Events Processed in Batch, and Top Sync Activity by App.
- **Clusters & Kubernetes API:** panels include Cluster Connection Status, Cluster Cache Age, Cluster Events by Kind, API Resource Objects, Kubectl Requests by Code, and Kubectl Requests by Method, plus related signals.
- **Redis & Cache:** panels include Redis Request Rate, Redis Duration Buckets, Redis Requests by Initiator, Redis Failures, Kubectl Transport Cache Entries, and Kubectl Transport Create Calls.
- **Inventory:** panels include Argo CD Metric Inventory and Argo CD Scrape Targets.
- **Logs:** panels include Argo CD Log Events, Argo CD Error Logs, Argo CD Logs Over Time, Argo CD Logs by Component, Argo CD Logs by Severity, and Recent Argo CD Error Logs.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `azure-prod-cluster-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `azure-prod-pod-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

8 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Metrics Dataset and Logs Dataset
- Scope filters: Argo CD Namespace, Project, Application, Sync Status, Health Status, and Pod

## Dashboard contents

- **42 tiles** across **7 collapsible sections**
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/argo-cd/assets)
- Importable template: [`argo-cd-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/argo-cd/argo-cd-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
