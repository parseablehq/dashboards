# Go Runtime Metrics

Monitor Go services instrumented with OpenTelemetry runtime metrics. The dashboard covers goroutines, processor limits, runtime memory, GC targets, allocation activity, runtime configuration, and telemetry inventory.

## What the dashboard shows

- **Overview:** active Go services, live goroutines, runtime memory, allocation throughput, processor limits, GC heap goals, and GOGC configuration.
- **Concurrency & Scheduling:** goroutines by service, goroutine growth, processor limits, and goroutines per processor.
- **Memory & GC Targets:** runtime memory by service and type, memory growth, stack and other memory, GC heap goals, configured limits, and memory per goroutine.
- **Allocation Activity:** cumulative allocated bytes and allocations, allocation rates, throughput, and average allocation size.
- **Runtime Configuration & Inventory:** GOGC, memory limits, Go versions, executable identity, service inventory, sample volume, freshness, and metric metadata.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `astronomy-shop-metrics` | PromQL and SQL | OpenTelemetry Go runtime measurements and telemetry inventory |

The dashboard expects current OpenTelemetry Go runtime families such as `go.goroutine.count`, `go.memory.used`, `go.memory.allocated`, `go.memory.allocations`, `go.memory.gc.goal`, `go.memory.limit`, `go.processor.limit`, and `go.config.gogc`.

Dataset names can be changed after import through the dashboard variable.

## Filters

5 dashboard variables scope relevant panels:

- Dataset selector: Go Metrics Dataset
- Runtime filters: Service, Service Namespace, Host, and Go Runtime Version

## Dashboard contents

- **34 tiles** across **5 collapsible sections**
- **29 PromQL tiles** and **5 SQL inventory tiles**
- Screenshot assets directory: [`assets/`](assets/)
- Importable template: [`go-runtime-metrics-mixed.json`](go-runtime-metrics-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the metrics dataset variable to the dataset receiving OpenTelemetry Go runtime telemetry.
