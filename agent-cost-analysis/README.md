# Agent Cost Analysis

Prism dashboard template for GenAI agent cost analysis.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `agent-cost-analysis-sql.json` | Agent Cost Analysis | 30 |

## Agent Cost Analysis

**File:** `agent-cost-analysis-sql.json`

Analyze GenAI agent spend, token consumption, and cost distribution across models, users, tools, and sessions. Use it to identify high-cost sessions, expensive model usage, pricing coverage gaps, and agent FinOps trends.

**Source:** `SQL`

**Tags:** `agent-observability`, `cost`

**Filter variables:** `trace_dataset`

**Panels:**

- Total Invocations
- Total Chat Calls
- Total Tool Calls
- Total Cost ($)
- Total Token Usage
- Avg Cost per Invocation
- P95 Cost per Invocation
- Cost Over Time
- Cost Rate of Change
- Cumulative Cost
- Cost per Token Over Time
- RSS Memory
- Cost by Provider and Model
- Model Cost Over Time
- Highest Cost Invocations
- Invocation Cost Distribution
- Cost vs Tokens by Invocation
- Unpriced Events
- Pricing Coverage
- Unpriced Models
- Cached Input Share
- Output / Input Token Ratio (%)
- Cost per Successful Outcome
- Success Rate
- Cost per Agent Job Over Time
- Cost by Outcome
- Cost by User
- Cost by Agent Name
- Cost by User and Model
- Cost by Agent and Model
