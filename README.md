# Parseable Dashboards

Reusable Parseable dashboard templates in JSON format. Each directory contains one importable dashboard JSON file and a short README with metadata.

## Importing Into Parseable

Use Parseable's dashboard import flow with either a downloaded JSON file or the raw GitHub JSON URL for a template. The JSON files contain the importable dashboard payload: tags, variables, sections, and tiles.

## Available Dashboards

| Dashboard | Description | Source | Tiles | Sections | Variables | File | Raw JSON |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| Agent Cost Analysis | Analyze GenAI agent spend, token consumption, and cost distribution across models, users, tools, and sessions. | SQL | 30 | 6 | 1 | [JSON](agent-cost-analysis/agent-cost-analysis-sql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/agent-cost-analysis/agent-cost-analysis-sql.json) |
| Agent Observability | Track GenAI agent invocations, outcomes, latency, tools, tokens, cost, and request-level behavior. | SQL | 77 | 9 | 2 | [JSON](agent-observability/agent-observability-sql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/agent-observability/agent-observability-sql.json) |
| Claude Code Usage | Monitor Claude Code sessions, model usage, request patterns, token consumption, and PromQL-backed runtime signals. | Mixed | 21 | 7 | 2 | [JSON](claude-code-usage/claude-code-usage-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/claude-code-usage/claude-code-usage-mixed.json) |
| K8s Cluster Monitoring | Monitor Kubernetes cluster health, nodes, pods, containers, workloads, logs, events, capacity, and kubelet/runtime signals. | Mixed | 74 | 9 | 7 | [JSON](k8s-cluster-monitoring/k8s-cluster-monitoring-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/k8s-cluster-monitoring/k8s-cluster-monitoring-mixed.json) |
| Argo CD | Monitor Argo CD applications, sync health, controller activity, Kubernetes API behavior, Redis/cache signals, metrics inventory, and Argo CD logs. | Mixed | 42 | 7 | 8 | [JSON](argo-cd/argo-cd-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/argo-cd/argo-cd-mixed.json) |
| Traefik Monitoring | Monitor Traefik ingress traffic, entrypoints, services, latency, TLS certificates, runtime health, access logs, and metric inventory. | Mixed | 38 | 7 | 8 | [JSON](traefik-monitoring/traefik-monitoring-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/traefik-monitoring/traefik-monitoring-mixed.json) |
| Postgres Monitoring | Monitor PostgreSQL health, connections, locks, database activity, storage, query performance, replication, WAL, logs, traces, and exporter inventory. | Mixed | 57 | 9 | 6 | [JSON](postgres-monitoring/postgres-monitoring-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/postgres-monitoring/postgres-monitoring-mixed.json) |
| MongoDB Monitoring | Monitor MongoDB connections, operations, storage, collections, WiredTiger cache, replication, logs, traces, and exporter inventory. | Mixed | 51 | 8 | 6 | [JSON](mongodb-monitoring/mongodb-monitoring-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/mongodb-monitoring/mongodb-monitoring-mixed.json) |
| Node Metrics Dashboard - PromQL | Monitor host-level CPU, memory, disk, network, filesystem, and load metrics from node exporter style PromQL data. | PromQL | 126 | 16 | 3 | [JSON](node-metrics-dashboard/node-metrics-dashboard-promql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/node-metrics-dashboard/node-metrics-dashboard-promql.json) |
| OTel Collector Metrics | Observe OpenTelemetry Collector throughput, receiver/exporter activity, queue behavior, dropped telemetry, and component inventory. | Mixed | 73 | 11 | 7 | [JSON](otel-collector-metrics/otel-collector-metrics-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/otel-collector-metrics/otel-collector-metrics-mixed.json) |
| OTel Demo Application | Explore application, service, and telemetry behavior for the OpenTelemetry Astronomy Shop demo application. | Mixed | 37 | 8 | 3 | [JSON](otel-demo-application/otel-demo-application-mixed.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/otel-demo-application/otel-demo-application-mixed.json) |
| Parseable Audit Logs | Review Parseable audit events, user activity, administrative actions, and access patterns from audit log datasets. | SQL | 28 | 7 | 2 | [JSON](parseable-audit-logs/parseable-audit-logs-sql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/parseable-audit-logs/parseable-audit-logs-sql.json) |
| Parseable Metrics | Monitor Parseable service metrics including ingestion, query behavior, storage, runtime health, and system-level PromQL signals. | PromQL | 66 | 8 | 2 | [JSON](parseable-metrics/parseable-metrics-promql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/parseable-metrics/parseable-metrics-promql.json) |
| Parseable Server Logs | Analyze Parseable server logs, error patterns, request activity, status distribution, and runtime log trends. | SQL | 14 | 6 | 1 | [JSON](parseable-server-logs/parseable-server-logs-sql.json) | [Raw](https://raw.githubusercontent.com/parseablehq/dashboards/main/parseable-server-logs/parseable-server-logs-sql.json) |

## Structure

Each dashboard follows this layout:

```text
<dashboard-name>/
  README.md
  <dashboard-name>-<source>.json
```

The naming convention is `name-of-dashboard-source.json`, where source is typically `sql`, `promql`, or `mixed`.
