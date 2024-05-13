## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- This is a list of defined metrics for monitoring services in NHN Cloud.
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
- A dictionary of instance server metrics provided by NHN Cloud.

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
| Instance | Name of the instance in use by the NHN Cloud Instance service |

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
- A dictionary for metrics in NCS.

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
| Workload | Name of the workload in use by NHN Cloud NCS |
| Type   | Storage type                          |


### NCS Legend
- You can apply a legend for NCS metrics.
- When you apply a legend, the metric is applied in legend format.

| Legend Name                                          | Description                             |
|----------------------------------------------|--------------------------------|
| label_ncs_container_nhncloud_com_workload_id | Name of the workload in use by NHN Cloud NCS |
| workload_id                                  | Name of the workload in use by NHN Cloud NCS |
| String                                         | Storage type                        |
| container                                    | Container Name                       |

## 3.10
- A dictionary of metrics for GPU services provided by NHN Cloud.

### Metric List
| Korean         | Resource Name | Default legend (Legend) | Unit   |
|-------------|------|---------------|------------|
| GPU usage     | 3.10  | None            | Percentage (0-100) |
| GPU yemperature      | 3.10  | None            | Celsius (℃)      |
| GPU memory usage | 3.10  | None            | Percentage (0-100) |
| GPU power usage  | 3.10  | None            | Watts (W)      |

### GPU Filter
- You can apply filters for GPU metrics.
- When you apply a filter, you'll only see metrics that match that filter.

| Filter name  | Description           |
|------|--------------|
| Instance | Name of the GPU instance |

### GPU Legend
- You can apply a legend for GPU metrics.
- When you apply a legend, the metric is applied in legend format.

| Filter name                  | Description           |
|----------------------|--------------|
| nhncloud_instance_id | Name of the GPU instance |
