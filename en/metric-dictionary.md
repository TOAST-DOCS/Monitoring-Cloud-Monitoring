## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- This is a list of defined metrics for monitoring services on NHN Cloud.
- Metric Dictionary helps you view and understand metrics for the services you monitor.
- You can find and use the metrics you need when configuring widgets. For more information, see the [console user guide](console-guide.md).
- In **Metric List**, you can see a list of metric dictionaries for each service.

### Filter
- You can apply filters to metrics.
- When you apply a filter, you'll only see metrics that match that filter.
  - For example, if you apply KR1 to the region filter, you will only see metrics that fall within the KR1 region among your metrics.
- Common filters are as follows.

| Filter name | Description           | Value                                                                  |
|-----|--------------|--------------------------------------------------------------------|
| Region  | NHN Cloud Region | kr1: Korea (Pangyo), kr2: Korea (Pyeongchon), kr3: Korea (Gwangju), us1: United States (California), jp1: Japan (Tokyo) |

### Legend
- You can apply a legend for metrics.
- When you apply a legend, the metric is applied in legend format.
  - For example, if you apply {{nhncloud_region}} to the legend, each metric appears as the region, such as kr1, kr2.
- Common legends are as follows.

| Filter name             | Description           | Value                                                                  |
|-----------------|--------------|--------------------------------------------------------------------|
| nhncloud_region | NHN Cloud Region | kr1: Korea (Pangyo), kr2: Korea (Pyeongchon), kr3: Korea (Gwangju), us1: United States (California), jp1: Japan (Tokyo) |

## Instance
- A dictionary that defines metrics that can be monitored for the Instance service on NHN Cloud.

### Metric List
| Korean              | Resource Name    | Default legend (Legend)                                                              | Unit         |
|------------------|---------|----------------------------------------------------------------------------|------------------|
| CPU usage          | 3.10     |                                                                            | Percentage (0-100)       |
| CPU usage by core      | 3.10     | {{nhncloud_instance_id}} cpu={{cpu}}                                       | Percentage (0-100)       |
| CPU details (user)     | 3.10     | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |
| CPU details (nice)     | 3.10     | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |
| CPU details (system)   | 3.10     | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |
| CPU details (iowait)   | 3.10     | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |
| CPU average load (1m)    | 3.10     | {{nhncloud_instance_id}}                                                   | Number               |
| CPU average load (5m)    | 3.10     | {{nhncloud_instance_id}}                                                   | Number               |
| CPU average load (15m)   | 3.10     | {{nhncloud_instance_id}}                                                   | Number               |
| Disk usage          | Disk    | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |
| Disk usage by mount     | Disk    | {{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}} | Ratio (0.00 - 1.00)  |
| Read disk           | Disk    | {{nhncloud_instance_id}}                                                   | Bytes per second (bytes/s)  |
| Write to disk           | Disk    | {{nhncloud_instance_id}}                                                   | Bytes per second (bytes/s)  |
| Read disk by device       | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | Bytes per second (bytes/s)  |
| Write to disk by device       | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | Bytes per second (bytes/s)  |
| Memory usage          | Memory  | {{nhncloud_instance_id}}                                                   | Percentage (0-100)       |
| Memory details (used)     | Memory  | {{nhncloud_instance_id}}                                                   | bytes       |
| Memory details (buffered) | Memory  | {{nhncloud_instance_id}}                                                   | bytes       |
| Memory details (cached)   | Memory  | {{nhncloud_instance_id}}                                                   | bytes       |
| Memory details (free)     | Memory  | {{nhncloud_instance_id}}                                                   | bytes       |
| Network data transmission      | Network | {{nhncloud_instance_id}}                                                   | Bytes per second (bytes/s)  |
| Network data reception      | Network | {{nhncloud_instance_id}}                                                   | Bytes per second (bytes/s)  |
| Network data transmission per device  | Network | {{nhncloud_instance_id}} interface={{interface}}                           | Bytes per second (bytes/s)  |
| Network data reception per device  | Network | {{nhncloud_instance_id}} interface={{interface}}                           | Bytes per second (bytes/s)  |
| Network data packet trasmission       | Network | {{nhncloud_instance_id}}                                                   | Packets per second (packets/s) |
| Network packet reception       | Network | {{nhncloud_instance_id}}                                                   | Packets per second (packets/s) |
| Network packet transmission per device   | Network | {{nhncloud_instance_id}} interface={{interface}}                           | Packets per second (packets/s) |
| Network packet reception per device   | Network | {{nhncloud_instance_id}} interface={{interface}}                           | Packets per second (packets/s) |
| Number of processes          | Process | {{nhncloud_instance_id}}                                                   | Number               |
| Swap usage (used)     | Swap    | {{nhncloud_instance_id}}                                                   | bytes       |
| Swap usage (free)     | Swap    | {{nhncloud_instance_id}}                                                   | bytes       |
| Swap usage (total)    | Swap    | {{nhncloud_instance_id}}                                                   | bytes       |
| Swap Usage           | Swap    | {{nhncloud_instance_id}}                                                   | Ratio (0.00 - 1.00)  |

### Instance Filter
- You can apply filters to the Instance metric.
- When you apply a filter, you'll only see metrics that match that filter.

| Filter name  | Description                                      |
|------|-----------------------------------------|
| Instance | Name of the instance being used by the Instance service on NHN Cloud. |

### Instance Legend
- You can apply a legend for the Instance metric.
- When you apply a legend, the metric is applied in legend format.

| Legend Name                  | Description                  |
|----------------------|---------------------|
| nhncloud_instance_id | Instance name            |
| cpu                  | CPU number of the instance        |
| device               | Disk device in the instance        |
| fstype               | File system type of the instance     |
| path                 | Disk mount path to the instance    |
| interface            | Name of the instance's network interface |

## NHN Container Service(NCS)
- A dictionary that defines metrics that can be monitored for NCS services on NHN Cloud.

### Metric List
| Korean           | Resource Name | Default legend (Legend)                                                            | Unit        |
|---------------|------|--------------------------------------------------------------------------|-----------------|
| CPU usage       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}} container={{container}} | Percentage (0-100)      |
| CPUs assigned to the workload | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Number              |
| Memory usage       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Percentage (0-100)      |
| Memory allocated to the workload | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Megabytes (MiB)      |
| GPU usage       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Percentage (0-100)      |
| GPU memory usage   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Percentage (0-100)      |
| GPU power usage    | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Megawatts (mW)        |
| GPU temperature        | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Celsius (℃)           |
| GPUs assigned to the workload | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Number              |
| Network data reception   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Bytes per second (bytes/s) |
| Network data transmission   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Bytes per second (bytes/s) |
| Disk usage       | NCS  | {{workload_id}} {{type}}                                                 | Percentage (0-100)      |
| Number of tasks by activation status  | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Number              |
| Number of processes in a container  | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | Number              |

### NCS Filter
- You can apply filters to NCS metrics.
- When you apply a filter, you'll only see metrics that match that filter.

| Filter name  | Description                               |
|------|----------------------------------|
| Workload | Name of the workload being used by the NCS service on NHN Cloud  |
| Type   | Storage type                          |


### NCS Legend
- You can apply a legend for NCS metrics.
- When you apply a legend, the metric is applied in legend format.

| Legend Name                                          | Description                             |
|----------------------------------------------|--------------------------------|
| label_ncs_container_nhncloud_com_workload_id | Name of the workload being used by the NCS service on NHN Cloud |
| workload_id                                  | Name of the workload being used by the NCS service on NHN Cloud |
| String                                         | Storage type                        |
| container                                    | Container Name                       |

## 3.10
- A dictionary that defines metrics that can be monitored for GPU services on NHN Cloud.

### Metric List
| Korean         | Resource Name | Default legend (Legend) | Unit   |
|-------------|------|---------------|------------|
| GPU Usage     | 3.10  | None            | Percentage (0-100) |
| GPU Temperature      | 3.10  | None            | Celsius (℃)      |
| GPU Memory Usage | 3.10  | None            | Percentage (0-100) |
| GPU Power Usage  | 3.10  | None            | Watts (W)      |

### GPU Filter
- You can apply filters for GPU metrics.
- When you apply a filter, you'll only see metrics that match that filter.

| Filter name  | Description                                  |
|------|-------------------------------------|
| Instance | The name of the instance being used by the GPU service on NHN Cloud. |

### GPU Legend
- You can apply a legend for GPU metrics.
- When you apply a legend, the metric is applied in legend format.

| Filter name                  | Description           |
|----------------------|--------------|
| nhncloud_instance_id | Name of the GPU instance |

## Transit Hub
- A dictionary that defines metrics that can be monitored for the Transit Hub service on NHN Cloud.

### Metric List
| Korean                                | Resource Name | Default legend (Legend) | Unit   |
|------------------------------------|------|---------------|------------|
| Network transmitted bytes                        | Transit Hub  | {{id}} | 5 min accumulated bytes |
| Network received bytes                        | Transit Hub  | {{id}} | 5 min accumulated bytes |
| Network transmitted packets                         | Transit Hub  | {{id}} | 5 min accumulated packets  |
| Network received packets                         | Transit Hub  | {{id}} | 5 min accumulated packets  |
| Network packets deleted due to route mismatch            | Transit Hub  | {{id}} | 5 min accumulated packets  |
| Network bytes deleted due to route mismatch           | Transit Hub  | {{id}} | 5 min accumulated bytes |
| Network packets deleted due to blackhole route match           | Transit Hub  | {{id}} | 5 min accumulated packets  |
| Network bytes deleted due to blackhole route match          | Transit Hub  | {{id}} | 5 min accumulated bytes |
| Network transmitted bytes                        | Attachment  | {{id}} | 5 min accumulated bytes |
| Network received bytes                        | Attachment  | {{id}} | 5 min accumulated bytes |
| Network transmitted packets                         | Attachment  | {{id}} | 5 min accumulated packets  |
| Network received packets                         | Attachment  | {{id}} | 5 min accumulated packets  |
| Network packets deleted due to route mismatch            | Attachment  | {{id}} | 5 min accumulated packets  |
| Network bytes deleted due to route mismatch           | Attachment  | {{id}} | 5 min accumulated bytes |
| Network packets deleted due to blackhole route match           | Attachment  | {{id}} | 5 min accumulated packets  |
| Network bytes deleted due to blackhole route match          | Attachment  | {{id}} | 5 min accumulated bytes |
| Network transmitted bits per second (bps)               | Transit Hub  | {{id}} |  Bits per second (bits/s)  |
| Network received bits per second (bps)               | Transit Hub  | {{id}} |  Bits per second (bits/s)  |
| Network transmitted packets per second (pps)               | Transit Hub  | {{id}} |  Packets per second (packets/s)  |
| Network received packets per second               | Transit Hub  | {{id}} |  Packets per second (packets/s)  |
| Network packets per second (pps) due to route mismatch  | Transit Hub  | {{id}} |  Packets per second (packets/s)  |
| Network bits per second (bps) due to route mismatch  | Transit Hub  | {{id}} |  Bits per second (bits/s)  |
| Network packets per second (pps) deleted due to blackhole route match | Transit Hub  | {{id}} |  Packets per second (packets/s)  |
| Network bits per second (bps) deleted due to blackhole route match | Transit Hub  | {{id}} |  Bits per second (bits/s)  |
| Network transmitted bits per second (bps)               | Attachment  | {{id}} |  Bits per second (bits/s)  |
| Network received bits per second (bps)               | Attachment  | {{id}} | Bits per second (bits/s)  |
| Network transmitted packets per second (pps)               | Attachment  | {{id}} |  Packets per second (packets/s)  |
| Network received packets per second               | Attachment  | {{id}} |  Packets per second (packets/s)  |
| Network packets per second (pps) due to route mismatch  | Attachment  | {{id}} |  Packets per second (packets/s)  |
| Network bits per second (bps) due to route mismatch  | Attachment  | {{id}} |  Bits per second (bits/s)  |
| Network packets per second (pps) deleted due to blackhole route match | Attachment  | {{id}} |  Packets per second (packets/s)  |
| Network bits per second (bps) deleted due to blackhole route match | Attachment  | {{id}} |  Bits per second (bits/s)  |


### Transit Hub Filter
- You can apply filters to Transit Hub metrics.
- When you apply a filter, only metrics that meet the criteria of that filter are displayed.

#### Resource Type > Applicable Filters for Transit Hub

| Filter name | Description |
| --- | --- |
| Transit Hub | Transit hub used by the Network service on NHN Cloud |

#### Resource Type > Applicable filters for Attachment

| Filter name | Description                                      |
| --- |-----------------------------------------|
| Transit Hub | Transit hub related to attachment |
| Attachment | Connect the transit hub used by Network services on NHN Cloud |

### Transit Hub Legend
- You can apply a legend for Transit Hub metrics.
- When you apply a legend, the metric is applied in legend format.

| Legend Name            | Description                         |
|----------------|----------------------------|
| id             | Transit hub or attachment name            |
| transit_hub_id | Transit hub name (if the resource is `attachment`) |

## Internet Gateway
- A dictionary that defines metrics that can be monitored for the Internet Gateway service on NHN Cloud.

### Metric List

| Korean                          | Resource Name    | Default legend (Legend)          | Unit         |
|------------------------------|---------|------------------------|------------------|
| Network transmitted bytes                 | Routing Table | {{id}} | 5 min accumulated bytes        |
| Network received bytes                 | Routing Table | {{id}} | 5 min accumulated bytes        |
| Network transmitted packets                  | Routing Table | {{id}} | 5 min accumulated packets         |
| Network received packets                  | Routing Table | {{id}} | 5 min accumulated packets         |
| Network transmitted bits per second (bps)        | Routing Table | {{id}} | Bits per second (bits/s)    | 
| Network received bits per second (bps)	    | Routing Table | {{id}} | Bits per second (bits/s)    | 
| Network transmitted packets per second (pps)	    | Routing Table | {{id}} | Packets per second (packets/s) | 
| Network received packets per second	    | Routing Table | {{id}} | Packets per second (packets/s) | 

### Internet Gateway Filter
- You can apply filters to the Internet Gateway metrics.
- When you apply a filter, only metrics that meet the criteria of that filter are displayed.

| Filter name | Description |
| --- | --- |
| Routing Table | Routing table used by Network service on NHN Cloud |

### Internet Gateway Legend
- You can apply a legend for the Internet Gateway metrics.
- When you apply a legend, the metric is applied in legend format.

| Legend Name            | Description                                     |
|----------------|----------------------------------------|
| id             | Routing table name  |
