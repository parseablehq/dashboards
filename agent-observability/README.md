# Agent Observability

Track GenAI agent invocations, outcomes, latency, tools, tokens, cost, and request-level behavior. It uses SQL panels to analyze telemetry directly from the selected Parseable datasets.

## What the dashboard shows

- **Overview:** panels include Total invocations, Error rate, Average agent run duration, P95 agent run duration, Total tool calls, and Total cost, plus related signals.
- **Cost:** panels include Cost by Model, Cost by Provider and Model, Total cost over time, Cost by Service, Cost by Agent Name, and Cost by Service and Model, plus related signals.
- **Performance and latency:** panels include Agents run over time, Errors, Tool latency, Overall agent latency, Slowest Invocations, and Recent Invocation Detail, plus related signals.
- **Tokens:** panels include Token consumption by Model, Model Chat Calls, Provider / Model Health, P95 Input/Output Tokens Over Time, Avg Input Tokens / LLM Call, and Avg Output Tokens / LLM Call, plus related signals.
- **Tools:** panels include Tool P95 Latency, Tool Calls Over Time, Top Tools, Tool Failures, Tool Failure Rate by Tool, and Tool Usage Over Time, plus related signals.
- **Submissions & Outcomes:** panels include Finish Status, Submission Rate Over Time, and Exit Status Over Time.
- **Details:** panels include Problem Hotspots, Environment / Version Breakdown, Service Rollups, Token Explorer, High Retry Loop Details, and Service Cost Rollup.
- **Cost Trends:** panels include Cost Over Time, Cost Rate of Change, Cumulative Cost, Cost per Token Over Time, P95 Chat Cost Over Time, and Cost Usage / Minute.
- **Invocation Cost:** panels include Highest Cost Invocations, Invocation Cost Distribution, Cost vs Tokens by Invocation, Cost per Agent Run, and Cost per Query.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `pydantic-ai-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

1 dashboard variable lets users select telemetry sources and scope relevant panels:

- Dataset selectors: Trace Dataset

## Dashboard contents

- **77 tiles** across **9 collapsible sections**
- SQL panels over Parseable datasets
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/agent-observability/assets)
- Importable template: [`agent-observability-sql.json`](https://github.com/parseablehq/dashboards/blob/main/agent-observability/agent-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
