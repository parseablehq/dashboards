# Agent Observability

Prism dashboard template for agent observability.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `agent-observability-sql.json` | Agent Observability | 77 |

## Agent Observability

**File:** `agent-observability-sql.json`

Track GenAI agent invocations, outcomes, latency, tool usage, token consumption, cost, and request-level behavior. Use it to inspect execution paths, failure concentration, and heavy usage patterns.

**Source:** `SQL`

**Tags:** `swe-agent`, `genai`, `sql`, `agent-observability`

**Filter variables:** `log_dataset`, `trace_dataset`

**Panels:**

- Total invocations
- Error rate
- Average agent run duration
- P95 agent run duration
- Agents run over time
- Errors
- Tool latency
- Token consumption by Model
- Tool P95 Latency
- Tool Calls Over Time
- Model Chat Calls
- Top Tools
- Finish Status
- Overall agent latency
- Slowest Invocations
- Tool Failures
- Recent Invocation Detail
- Submission Rate Over Time
- Exit Status Over Time
- Tool Failure Rate by Tool
- Problem Hotspots
- Environment / Version Breakdown
- Provider / Model Health
- Total tokens per invocation
- Recent Trace Summary
- Tool Usage Over Time
- Tool Latency Over Time
- Tool Performance Summary
- Cost Over Time
- Cost Rate of Change
- Cumulative Cost
- Cost per Token Over Time
- Cost by Model
- Cost by Provider and Model
- Total cost over time
- Highest Cost Invocations
- Invocation Cost Distribution
- Cost vs Tokens by Invocation
- Cost by User
- Cost by Agent Name
- Cost by User and Model
- Cost by Agent and Model
- Total tool calls
- Total cost
- Total input tokens
- Average cost per agent run
- P95 Invocation Latency by Agent
- Invocation Latency by Username
- P95 Input/Output Tokens Over Time
- P95 Chat Cost Over Time
- Active Users
- Cache Hit Rate
- Avg Input Tokens / LLM Call
- Avg Output Tokens / LLM Call
- High Retry Loop Runs
- Budget Breaches
- Cost Usage / Minute
- Token Usage / Minute
- Tokens by Type
- Tokens by Model
- Cost per Agent Run
- Cost per User
- Cost per Team
- Cost per Model
- Token Component Share
- Component Cost Split
- Executor Tokens
- Planner Tokens
- Judges/Evals Tokens
- Tool Overhead Tokens
- Output Tokens
- Workspace Rollups
- Cost per Query
- Token Explorer
- High Retry Loop Details
- Budget Burn Alerts
- Cached Tokens
