# Website Performance & Visits

Monitor frontend traffic, page activity, API performance, HTTP reliability, external dependencies, request traces, and telemetry health. The dashboard combines PromQL metrics with SQL-based frontend traces.

## What the dashboard shows

- **Overview:** page views, API request rate, average and p95 request duration, success percentage, errors, unique pages, and observed hosts.
- **Traffic & Visits:** request volume, popular pages, referrers, navigation types, page-level traffic, and recent page-view records.
- **API Performance:** request rates by status and endpoint, duration percentiles, latency trends, slow targets, slow hosts, and recent slow requests.
- **Reliability & Errors:** error rate, HTTP status classes, errors by page and host, non-success targets, and 404 URLs.
- **External Dependencies:** request volume, latency, reliability, API rate, and recent requests grouped by external host.
- **Trace Explorer:** trace volume, latency distribution, HTTP methods, recent spans, slow spans, and frontend service inventory.
- **Telemetry & Inventory:** metric families, metric volume, signal freshness, trace attribute coverage, resource inventory, and telemetry volume.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `frontend-metrics` | PromQL / SQL | Page views, API request rate, API duration histograms, traffic dimensions, and metric inventory |
| Traces | `frontend-traces` | SQL | HTTP request latency, status, pages, dependencies, errors, trace exploration, and service inventory |

The metric panels expect `page_views`, `api_calls`, and `api_duration_ms` telemetry. Trace panels use standard OpenTelemetry span fields and frontend HTTP attributes such as `page.path`, `http.host`, `http.method`, and `http.status_code`.

## Filters

10 dashboard variables scope relevant panels:

- Dataset selectors: Trace Dataset and Metrics Dataset
- Frontend filters: Environment, Service, Page, Host, HTTP Status, HTTP Method, Referrer, and Navigation Type

## Dashboard contents

- **44 tiles** across **7 collapsible sections**
- **9 PromQL metric tiles** and **35 SQL trace/metric tiles**
- Screenshot assets directory: [`assets/`](assets/)
- Importable template: [`website-performance-and-visits-mixed.json`](website-performance-and-visits-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving frontend metrics and traces.
