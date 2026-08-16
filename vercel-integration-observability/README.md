# Vercel Integration Observability

Monitor everything delivered by the Parseable Vercel integration: request logs, distributed traces, Core Web Vitals from Speed Insights, and pageview events from Web Analytics — in one dashboard.

## What the dashboard shows

- **Overview:** total log events, total spans, total Speed Insights events, total pageviews, and the current error log rate.
- **Logs:** recent log lines, recent error logs, log volume by level, and requests by HTTP status code.
- **Traces:** recent spans, slowest spans (>1s), average span duration, and spans grouped by route.
- **Speed Insights (Web Vitals):** average LCP, CLS, and INP, events grouped by rating (good/needs-improvement/poor), and per-route web vitals breakdown.
- **Web Analytics:** recent pageviews, and events grouped by path, event type, and origin.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Logs | `vercel_logs` | SQL | Request/runtime logs delivered via the `logs` drain (`schema=log`, delivery=`http`, path `/api/v1/ingest`) |
| Traces | `vercel_traces` | SQL | Request spans delivered via the `traces` drain (`schema=trace`, delivery=`otlphttp`, path `/v1/traces`) |
| Speed Insights | `vercel_speed_insights` | SQL | Core Web Vitals delivered via the `speed_insights` drain |
| Web Analytics | `vercel_analytics` | SQL | Pageview events delivered via the `analytics` drain |

Queries match the live Vercel drain schemas: traces use `span_name` and `span_duration_ns`, Speed Insights uses `metricType`, `value`, and `path`, and Web Analytics uses `eventType`, `path`, and `origin`.

## Filters

4 dashboard variables scope the dashboard to your datasets:

- Logs Dataset, Traces Dataset, Speed Insights Dataset, Web Analytics Dataset

## Dashboard contents

- **22 tiles** across **5 collapsible sections**
- All tiles are SQL-based
- Icon asset: [`assets/icon.svg`](https://github.com/parseablehq/dashboards/blob/main/vercel-integration-observability/assets/icon.svg)
- Importable template: [`vercel-integration-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/vercel-integration-observability/vercel-integration-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the four dataset variables to the datasets receiving each Vercel drain's data.
