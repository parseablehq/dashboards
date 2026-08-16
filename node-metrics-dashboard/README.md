# Node Metrics Dashboard - PromQL

Monitor host-level CPU, memory, disk, network, filesystem, and load metrics from node exporter style PromQL data. It uses PromQL panels for time-series monitoring, breakdowns, and operational inventory.

## What the dashboard shows

- **Quick CPU / Mem / Disk:** panels include CPU Pressure, Memory Pressure, IO Pressure, CPU Busy in percent, Sys Load, and RAM Used, plus related signals.
- **Basic CPU / Mem / Net / Disk:** panels include CPU Basic, Memory Basic, Network Traffic Basic, and Disk Space Used Basic.
- **CPU / Memory / Net / Disk:** panels include CPU Details, Memory in details, Disk IOPS, I/O Usage Read/Write, Network Traffic, and Network Saturation, plus related signals.
- **Memory Meminfo:** panels include Memory Committed, Memory Writeback and Dirty, Memory Slab, Memory Shared and Mapped, Memory LRU Active / Inactive (%), and Memory LRU Active / Inactive Detail, plus related signals.
- **Memory Vmstat:** panels include Memory Pages In / Out, Memory Pages Swap In / Out, Memory Page Faults, and OOM Killer.
- **System Timesync:** panels include Time Synchronized Drift, Time PLL Adjust, Time Synchronized Status, PPS Frequency / Stability, PPS Time Accuracy, and PPS Sync Events, plus related signals.
- **System Processes:** panels include Processes Status, Processes Detailed States, Processes Forks, PIDs Number and Limit, and Threads Number and Limit.
- **System Misc:** panels include Irq Pressure, Reboot Required, CPU Saturation per Core, Context Switches / Interrupts, System Load, and CPU Frequency Scaling, plus related signals.
- **Hardware Misc:** panels include Hardware Temperature Monitor, Cooling Device Utilization, Power Supply, and Hardware Fan Speed.
- **Systemd:** panels include Systemd Units State, Systemd Sockets Current, Systemd Sockets Accepted, and Systemd Sockets Refused.
- **Storage Disk:** panels include Disk Read/Write IOps, Disk Read/Write Data, Disk Average Wait Time, Average Queue Size, Disk R/W Merged, and Disk Ops Discards / Flush, plus related signals.
- **Storage Filesystem:** panels include File Descriptor, File Nodes Free, Filesystem in ReadOnly / Error, and File Nodes Size.
- **Network Traffic:** panels include Network Traffic by Packets, Network Traffic Errors, Network Traffic Drop, Network Traffic Compressed, Network Traffic Multicast, and Network Traffic NoHandler, plus related signals.
- **Network Sockstat:** panels include Sockstat TCP, Sockstat UDP, Sockstat Used, Sockstat FRAG / RAW, TCP/UDP Kernel Buffer Memory Pages, and Sockstat Memory Size, plus related signals.
- **Network Netstat:** panels include Netstat IP In / Out Octets, TCP In / Out, UDP In / Out, ICMP In / Out, TCP Errors, and UDP Errors, plus related signals.
- **Node Exporter:** panels include Node Exporter Scrape Time, Exporter Process CPU Usage, Exporter Processes Memory, Exporter File Descriptor Usage, Node Exporter Scrape - collector, and Node Exporter Scrape - textfile.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Metrics | `box3-node-metrics` | PromQL | Operational metrics for availability, throughput, saturation, latency, resource use, and inventory |

Expected fields and labels follow the panel queries and the relevant OpenTelemetry or exporter conventions. Dataset names can be changed after import through dashboard variables.

## Filters

3 dashboard variables let users select telemetry sources and scope relevant panels:

- Dataset selectors: Dataset
- Scope filters: node and Job

## Dashboard contents

- **126 tiles** across **16 collapsible sections**
- PromQL panels over metric datasets
- Screenshot assets directory: [`assets/`](https://github.com/parseablehq/dashboards/tree/main/node-metrics-dashboard/assets)
- Importable template: [`node-metrics-dashboard-promql.json`](https://github.com/parseablehq/dashboards/blob/main/node-metrics-dashboard/node-metrics-dashboard-promql.json)

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variables to the datasets receiving this telemetry.
