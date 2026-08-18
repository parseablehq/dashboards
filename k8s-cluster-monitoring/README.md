# K8s Cluster Monitoring

Monitor Kubernetes cluster health, nodes, pods, containers, workloads, logs, events, capacity, and kubelet/runtime signals. It combines PromQL metrics with SQL telemetry so operational signals can be investigated together.

## What the dashboard shows

- **Overview:** panels include Nodes, Namespaces, Pods Seen, Containers Seen, Pod Log Events, K8s Event Records, Pods by Phase Over Time, and Namespaces by Phase Over Time.
- **Node Metrics:** panels include Node CPU Usage %, Node Memory Working Set %, Node Filesystem Usage, Node Network IO Rate, Node Conditions, and Node Pressure Conditions, plus related signals.
- **Pod and Container Metrics:** panels include Pod CPU by Namespace, Pod Memory by Namespace, Container CPU by Namespace, Container Memory by Namespace, Pod Network IO Rate, and Pod Network Error Rate, plus related signals.
- **Workloads:** panels include Deployment Desired vs Available, Deployment Available, DaemonSet Desired vs Ready, DaemonSet Ready Nodes, StatefulSet Ready vs Desired, and ReplicaSet Available vs Desired, plus related signals.
- **Pod logs:** panels include Pod Logs Over Time, Log Volume by Namespace, and Top Log Pods.
- **Pod Log Errors:** panels include Top Pod Errors, Pod Errors Over Time, Pod Log Errors by Pod Over Time, and Pod Log Errors by Namespace Over Time.
- **K8s Events:** panels include Events Over Time, Warnings Over Time, Events by Type Over Time, Events by Reason Over Time, Events by Namespace Over Time, and Events by Component Over Time, plus related signals.
- **Capacity and Limits:** panels include Node Allocatable CPU, Node Allocatable Memory, Container CPU Requests by Namespace, Container CPU Limits by Namespace, Container Memory Requests by Namespace, and Container Memory Limits by Namespace, plus related signals.
- **Kubelet and Runtime:** panels include Kubelet Runtime Operation Errors and Kubelet HTTP Request Rate.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `azure-prod-cluster-metrics` | PromQL / SQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |
| Logs | `azure-prod-pod-logs` | SQL | Log records for volume, severity, errors, activity, and recent-event investigation |
| Events | `azure-prod-events` | SQL | Kubernetes events for scheduling, lifecycle, warning, and failure analysis |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

7 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Cluster Metrics Dataset, K8s Pod Logs Dataset, and K8s Events Dataset
- Scope filters: Namespace, Node, Pod, and Container

## Dashboard contents

- **74 tiles** across **9 collapsible sections**
- **47 time-series panels** with no pie or donut visualizations
- PromQL metrics and SQL telemetry in one mixed-source dashboard
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/k8s-cluster-monitoring/assets)
- Importable template: [`k8s-cluster-monitoring-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/k8s-cluster-monitoring/k8s-cluster-monitoring-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
