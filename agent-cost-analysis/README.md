# Agent Cost Analysis

Analyze GenAI agent spend, token consumption, and cost distribution across models, services, tools, and sessions. It uses SQL panels to analyze telemetry directly from the selected Parseable datasets.

## What the dashboard shows

- **Overview:** panels include Total Invocations, Total Chat Calls, Total Tool Calls, Total Cost ($), Total Token Usage, and Avg Cost per Invocation, plus related signals.
- **Cost Trends:** panels include Cost Over Time, Cost Rate of Change, Cumulative Cost, and Cost per Token Over Time.
- **Model Cost:** panels include Cost Per Model, Cost by Provider and Model, Model Cost Over Time, Cost by Service, Cost by Agent Name, and Cost by Service and Model, plus related signals.
- **Invocation Cost:** panels include Highest Cost Invocations, Invocation Cost Distribution, and Cost vs Tokens by Invocation.
- **Pricing Coverage:** panels include Unpriced Events, Pricing Coverage, and Unpriced Models.
- **AI FinOps KPIs:** panels include Cached Input Share, Output / Input Token Ratio (%), Cost per Successful Outcome, Success Rate, Cost per Agent Job Over Time, and Cost by Outcome.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Traces | `pydantic-ai-traces` | SQL | Spans for latency, errors, operations, request behavior, and trace investigation |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

1 dashboard variable lets users select telemetry sources and scope relevant panels:

- Dataset selectors: Trace Dataset

## Dashboard contents

- **30 tiles** across **6 collapsible sections**
- SQL panels over Parseable datasets
- Dashboard screenshot in [`assets/`](https://github.com/parseablehq/dashboards/tree/main/agent-cost-analysis/assets)
- Importable template: [`agent-cost-analysis-sql.json`](https://github.com/parseablehq/dashboards/blob/main/agent-cost-analysis/agent-cost-analysis-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
