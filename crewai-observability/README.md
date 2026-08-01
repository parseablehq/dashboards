# CrewAI Observability

Monitor CrewAI crews, flows, agents, tasks, LLM calls, token usage, tools, latency, and errors from OpenInference traces. It uses SQL panels to analyze OpenTelemetry spans directly from the selected Parseable trace dataset.

## What the dashboard shows

- **Overview:** total traces, crew runs, crew success rate, error spans, average and P95 crew duration, LLM calls, and tool calls.
- **Runs & Performance:** scenario throughput, workload mix, latency by scenario, and recent tagged runs.
- **Agents & Tasks:** agent execution counts, outcomes, error rate, P95 duration, and per-agent performance.
- **LLM & Tokens:** input, output, and total token consumption; model usage; LLM latency; and LLM outcomes.
- **Tools:** tool error rate, latency, failures, usage by name, performance, and call volume over time.
- **Errors & Trace Detail:** span error rate, failed traces, errors by span kind, recent errors, and trace-level summaries.

## Data used

| Signal | Default dataset | Query language | Purpose                                                                                            |
| ------ | --------------- | -------------- | -------------------------------------------------------------------------------------------------- |
| Traces | `crewai-traces` | SQL            | OpenInference spans for CrewAI flows, crews, agents, tools, LLM calls, latency, tokens, and errors |

The template expects traces produced by `openinference-instrumentation-crewai` and exported to Parseable through OTLP/HTTP. Important fields include:

- `openinference.span.kind`
- `crew_id`, `task_id`, `task_name`, and `flow_id`
- `llm.model_name` and `llm.token_count.*`
- `tool.name`
- `span_trace_id`, `span_parent_span_id`, `span_duration_ns`, and `span_status_code`

Scenario-specific panels use the optional `load_test.*` attributes from the accompanying fixture workload. Core CrewAI, agent, LLM, tool, token, latency, and error panels work without those attributes.

## Filters

1 dashboard variable lets users select the telemetry source:

- Dataset selector: Trace Dataset

## Dashboard contents

- **38 tiles** across **6 collapsible sections**
- SQL panels over OpenInference and OpenTelemetry trace fields
- Dashboard preview images in [`assets/`](assets/)
- Importable template: [`crewai-observability-sql.json`](crewai-observability-sql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map **Trace Dataset** to the dataset receiving CrewAI OpenInference spans. The default is `crewai-traces`.
