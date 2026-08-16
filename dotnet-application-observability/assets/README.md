# .NET Application Observability

Monitor ASP.NET Core application traffic, reliability, latency, .NET runtime health, GC and memory behavior, thread pool activity, exceptions, correlated logs, traces, and telemetry inventory.

## What the dashboard shows

- **Overview:** active services, request volume, error rate, latency, trace services, total traces, log errors, and metric families.
- **Golden Signals:** traffic, latency, errors, and CPU saturation.
- **ASP.NET Requests:** request rate by method, top routes, average request duration, and status code mix.
- **.NET Runtime:** process memory, CPU time, assembly count, and JIT compilation time.
- **GC & Memory:** allocation volume, GC collections, heap/object size, and GC duration.
- **Threading & Exceptions:** thread pool threads, queue length, completed work items, and exception counts.
- **Logs & Errors:** log volume, error rate, errors by service, and recent error logs.
- **Traces & Dependencies:** trace throughput, span latency, span errors, and slow operations.
- **Inventory:** metric inventory, runtime identity, and route inventory from traces.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `dotnet-metrics` | PromQL and SQL | ASP.NET Core, process, and .NET runtime metrics |
| Traces | `dotnet-traces` | SQL | Request, dependency, and custom workload spans |
| Logs | `dotnet-logs` | SQL | ASP.NET Core and application logs |

The dashboard expects OpenTelemetry .NET metrics such as `http.server.request.duration`, `process.memory.usage`, `process.cpu.time`, `process.runtime.dotnet.gc.*`, `process.runtime.dotnet.thread_pool.*`, and `process.runtime.dotnet.exceptions.count`.

Dataset names can be changed after import through dashboard variables.

## Filters

8 dashboard variables scope relevant panels:

- Dataset selectors: .NET Metrics Dataset, .NET Traces Dataset, and .NET Logs Dataset
- Runtime and request filters: Environment, Service, HTTP Route, HTTP Method, and Status Code

## Dashboard contents

- **39 tiles** across **9 collapsible sections**
- **13 PromQL metric tiles** and **26 SQL tiles**
- Importable template: [`dotnet-application-observability-mixed.json`](https://github.com/parseablehq/dashboards/blob/main/dotnet-application-observability/dotnet-application-observability-mixed.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the metrics, traces, and logs dataset variables to the datasets receiving OpenTelemetry .NET telemetry.
