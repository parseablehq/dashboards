# Node Metrics Dashboard - PromQL

Prism dashboard template for node-level infrastructure metrics.

Browse all dashboard templates in the [Parseable dashboards repository](../README.md).

## Dashboards

| File | Dashboard | Panels |
| --- | --- | ---: |
| `node-metrics-dashboard-promql.json` | Node Metrics Dashboard - PromQL | 126 |

## Node Metrics Dashboard - PromQL

**File:** `node-metrics-dashboard-promql.json`

Monitor host-level CPU, memory, disk, network, filesystem, and load metrics from node exporter style PromQL data. Use it for infrastructure health checks, capacity review, and node-level troubleshooting.

**Source:** `PromQL`

**Tags:** `node`, `promql`

**Filter variables:** `node`, `job`, `dataset`

**Panels:**

- CPU Pressure
- Memory Pressure
- IO Pressure
- CPU Busy in percent
- Sys Load
- RAM Used
- SWAP Used
- Root FS Used
- CPU Cores
- Root FS Total in TiB
- RAM Total in GB
- SWAP Total in GB
- Uptime in weeks
- CPU Basic
- Memory Basic
- Network Traffic Basic
- Disk Space Used Basic
- CPU Details
- Memory in details
- Disk IOPS
- I/O Usage Read/Write
- Irq Pressure
- Reboot Required
- Network Traffic
- Network Saturation
- Filesystem Space Available
- Filesystem Used
- Disk I/O Utilization
- Pressure Stall Information
- Memory Committed
- Memory Writeback and Dirty
- Memory Slab
- Memory Shared and Mapped
- Memory LRU Active / Inactive (%)
- Memory LRU Active / Inactive Detail
- Memory Kernel / CPU / IO
- Memory Vmalloc
- Memory Anonymous
- Memory Unevictable and MLocked
- Memory DirectMap
- Memory HugePages
- Memory Pages In / Out
- Memory Pages Swap In / Out
- Memory Page Faults
- OOM Killer
- Time Synchronized Drift
- Time PLL Adjust
- Time Synchronized Status
- PPS Frequency / Stability
- PPS Time Accuracy
- PPS Sync Events
- Processes Status
- Processes Detailed States
- Processes Forks
- CPU Saturation per Core
- PIDs Number and Limit
- Threads Number and Limit
- Context Switches / Interrupts
- System Load
- CPU Frequency Scaling
- CPU Schedule Timeslices
- IRQ Detail
- Entropy
- Hardware Temperature Monitor
- Cooling Device Utilization
- Power Supply
- Hardware Fan Speed
- Systemd Units State
- Systemd Sockets Current
- Systemd Sockets Accepted
- Systemd Sockets Refused
- Disk Read/Write IOps
- Disk Read/Write Data
- Disk Average Wait Time
- Average Queue Size
- Disk R/W Merged
- Time Spent Doing I/Os
- Disk Ops Discards / Flush
- Disk Sectors Discarded Successfully
- Instantaneous Queue Size
- File Descriptor
- File Nodes Free
- Filesystem in ReadOnly / Error
- File Nodes Size
- Network Traffic by Packets
- Network Traffic Errors
- Network Traffic Drop
- Network Traffic Compressed
- Network Traffic Multicast
- Network Traffic NoHandler
- Network Traffic Frame
- Network Traffic Fifo
- Network Traffic Collision
- Network Traffic Carrier Errors
- ARP Entries
- NF Conntrack
- Network Operational Status
- Speed
- MTU
- Sockstat TCP
- Sockstat UDP
- Sockstat Used
- Sockstat FRAG / RAW
- TCP/UDP Kernel Buffer Memory Pages
- Sockstat Memory Size
- Softnet Packets
- Softnet Out of Quota
- Softnet RPS
- Netstat IP In / Out Octets
- TCP In / Out
- UDP In / Out
- ICMP In / Out
- TCP Errors
- UDP Errors
- ICMP Errors
- TCP SynCookie
- TCP Connections
- UDP Queue
- TCP Direct Transition
- TCP Stat
- Node Exporter Scrape Time
- Exporter Process CPU Usage
- Exporter Processes Memory
- Exporter File Descriptor Usage
- Node Exporter Scrape - collector
- Node Exporter Scrape - textfile
