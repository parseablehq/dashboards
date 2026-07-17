# Argo CD

Prism dashboard template for Argo CD monitoring.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `argo-cd-mixed.json` | Argo CD | 42 |

## Argo CD

**File:** `argo-cd-mixed.json`

Monitor Argo CD applications, sync health, controller activity, Kubernetes API behavior, Redis/cache signals, metrics inventory, and Argo CD logs.

**Source:** `Mixed`

**Tags:** `argocd`, `gitops`, `kubernetes`, `promql`, `logs`

**Filter variables:** `metrics_dataset`, `logs_dataset`, `namespace`, `project`, `application`, `sync_status`, `health_status`, `pod`

**Panels:**

- Applications
- Healthy Apps
- Out Of Sync Apps
- Connected Clusters
- Orphaned Resources
- Kubectl Retries
- App Health %
- App Sync %
- Applications by Health
- Applications by Sync Status
- Applications by Project
- Applications by Destination Namespace
- Out Of Sync Applications
- Apps with Orphaned Resources
- Sync Rate by Phase
- Sync Duration Rate
- Reconcile Duration Buckets
- Reconcile Count Rate
- Resource Events Processed in Batch
- Top Sync Activity by App
- Cluster Connection Status
- Cluster Cache Age
- Cluster Events by Kind
- API Resource Objects
- Kubectl Requests by Code
- Kubectl Requests by Method
- Kubectl Duration Buckets
- Kubectl Exec Pending
- Redis Request Rate
- Redis Duration Buckets
- Redis Requests by Initiator
- Redis Failures
- Kubectl Transport Cache Entries
- Kubectl Transport Create Calls
- Argo CD Metric Inventory
- Argo CD Scrape Targets
- Argo CD Log Events
- Argo CD Error Logs
- Argo CD Logs Over Time
- Argo CD Logs by Component
- Argo CD Logs by Severity
- Recent Argo CD Error Logs
