# NVIDIA GPU Monitoring

Monitor NVIDIA GPUs using metrics collected from NVIDIA DCGM Exporter. Dashboard covers utilization, framebuffer memory, temperatures, power, execution engines, clocks, PCIe traffic, energy consumption, and hardware reliability.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `nvidia-gpu-metrics` | PromQL | NVIDIA DCGM GPU telemetry |

Dashboard expects metrics from NVIDIA DCGM Exporter ingested into Parseable through an OpenTelemetry Collector. Dataset can be changed after import using dashboard variable.

## Filters

- Metrics dataset
- Host
- GPU

## Dashboard contents

- **16 tiles** across **4 collapsible sections**
- Overview, GPU telemetry, execution and I/O, energy and reliability
- Importable template: `nvidia-gpu-monitoring-promql.json`

## Import

Download JSON file and use Parseable dashboard import flow. Map metrics dataset variable to dataset receiving DCGM Exporter telemetry.

## Icon

NVIDIA logo sourced from [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:NVIDIA_logo.svg). NVIDIA and its logo are trademarks of NVIDIA Corporation.
