# K8s Cluster Monitoring

Prism dashboard template for Kubernetes cluster monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `k8s-cluster-monitoring-mixed.json` | K8s Cluster Monitoring | 58 |

## K8s Cluster Monitoring

**File:** `k8s-cluster-monitoring-mixed.json`

Monitor Kubernetes cluster health, nodes, pods, containers, workloads, pod logs, Kubernetes events, capacity, and kubelet/runtime signals. Use it to troubleshoot cluster behavior across metrics, logs, and events.

**Source:** `Mixed`

**Tags:** `kubernetes`, `k8s`, `cluster`, `metrics`, `logs`

**Filter variables:** `cluster_metrics_dataset`, `pod_logs_dataset`, `events_dataset`, `namespace`, `node`, `pod`, `container`

**Panels:**

- Nodes
- Namespaces
- Pods Seen
- Containers Seen
- Pod Log Events
- Node CPU Usage %
- Node Memory Working Set %
- Node Filesystem Usage
- Node Network IO Rate
- Pod CPU by Namespace
- Pod Memory by Namespace
- Container CPU by Namespace
- Container Memory by Namespace
- Pod Network IO Rate
- Pod Network Error Rate
- Pod Phase by Namespace
- Node Conditions
- Deployment Desired vs Available
- Deployment Available
- DaemonSet Desired vs Ready
- DaemonSet Ready Nodes
- Pod Logs Over Time
- Top Log Namespaces
- Top Log Pods
- Container Restarts
- Top Pod CPU
- Top Pod Memory
- K8s Event Records
- Warning Events
- Event Occurrences
- Warning Occurrences
- Events Over Time
- Warnings Over Time
- Events by Type
- Top Event Reasons
- Top Event Namespaces
- Events by Component
- High Occurrence Warnings
- Recent Warning Events
- Top Pod Errors
- Pod Errors Over Time
- Pod Log Errors by Pod
- Pod Log Errors by Namespace
- Node Allocatable CPU
- Node Allocatable Memory
- Node Pressure Conditions
- Container Ready by Namespace
- Container CPU Requests by Namespace
- Container CPU Limits by Namespace
- Container Memory Requests by Namespace
- Container Memory Limits by Namespace
- Pod Filesystem Usage by Namespace
- Pod Filesystem Available by Namespace
- Kubelet Runtime Operation Errors
- Kubelet HTTP Request Rate
- Running Containers by State
- StatefulSet Ready vs Desired
- ReplicaSet Available vs Desired
