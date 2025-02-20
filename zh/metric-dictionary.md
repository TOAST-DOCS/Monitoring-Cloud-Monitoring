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
| Metric Name              | Resource Name    | Default legend (Legend)                                                              | Unit         |
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
| Metric Name           | Resource Name | Default legend (Legend)                                                            | Unit        |
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
| Metric Name         | Resource Name | Default legend (Legend) | Unit   |
|-------------|------|---------------|------------|
| GPU usage     | 3.10  | None            | Percentage (0-100) |
| GPU temperature      | 3.10  | None            | Celsius (℃)      |
| GPU memory usage | 3.10  | None            | Percentage (0-100) |
| GPU power usage  | 3.10  | None            | Watts (W)      |

### GPU Filter
- You can apply filters for GPU metrics.
- When you apply a filter, you'll only see metrics that match that filter.


| Filter name  | Description           |
|------|--------------|
| Instance | Name of the instance being used by the GPU service on NHN Cloud. |

### GPU Legend
- You can apply a legend for GPU metrics.
- When you apply a legend, the metric is applied in legend format.

| Filter name                  | Description           |
|----------------------|--------------|
| nhncloud_instance_id | Name of the GPU instance |

## Transit Hub
- A dictionary that defines metrics that can be monitored for the Transit Hub service on NHN Cloud.

### Metric List
| Metric Name                                | Resource Name | Default legend (Legend) | Unit   |
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

| Metric Name                          | Resource Name    | Default legend (Legend)          | Unit         |
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

## Colocation Gateway
- A dictionary that defines metrics that can be monitored for the Colocation Gateway service on NHN Cloud.

### Metric List

| Metric Name                                  | Resource Name      | Default legend (Legend) | Unit                            |
|----------------------------------------------|--------------------|-------------------------|---------------------------------|
| Network transmitted bytes                    | Colocation Gateway | {{id}}                  | 5 min accumulated bytes         |
| Network received bytes                       | Colocation Gateway | {{id}}                  | 5 min accumulated bytes         |
| Network transmitted packets                  | Colocation Gateway | {{id}}                  | 5 min accumulated packets       |
| Network received packets                     | Colocation Gateway | {{id}}                  | 5 min accumulated packets       |
| Network transmitted bits per second (bps)    | Colocation Gateway | {{id}}                  | Bits per second (bits/s)        | 
| Network received bits per second (bps)	      | Colocation Gateway | {{id}}                  | Bits per second (bits/s)        | 
| Network transmitted packets per second (pps) | Colocation Gateway | {{id}}                  | Packets per second (packets/s)  | 
| Network received packets per second	         | Colocation Gateway | {{id}}                  | Packets per second (packets/s)  | 

### Colocation Gateway Filter

| Filter name         | Description                                             |
|---------------------|---------------------------------------------------------|
| Colocation Gateway  | Colocation gateway used by Network service on NHN Cloud |

### Colocation Gateway Legend

| Legend Name | Description             |
|-------------|-------------------------|
| id          | Colocation gateway name |

## Load Balancer
- A dictionary that defines metrics that can be monitored for the Load Balancer service on NHN Cloud.

### Metric List

| Metric Name                                     | Resource Name | Default legend (Legend)                                       | Unit                     |
|-------------------------------------------------|---------------|---------------------------------------------------------------|--------------------------|
| Network Received Byte                           | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated bytes  |
| Network Sent Byte                               | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated bytes  |
| Number of Network Received Bit per Second (bps) | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Bits per second (bit/s)  |
| Number of Network Sent Bit per Second (bps)     | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Bits per second (bit/s)  |
| Number of Requests Pending Processing           | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |
| Number of Sessions in Connection Status         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |
| HTTP 100 Response Count                         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| HTTP 200 Response Count                         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| HTTP 300 Response Count                         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| HTTP 400 Response Count                         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| HTTP 500 Response Count                         | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| Other HTTP Responses Count                      | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5 min accumulated Number |
| Total Number Load balanced with the Member      | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |
| Number of Connections Error                     | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |
| Average Response Time                           | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Millisecond              |
| The Active Status Value of the Member           | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |
| Total Number of Normal HTTP Responses Returned  | Load Balancer | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | Number                   |

### Load Balancer Filter

| Filter name    | Description                                        |
|----------------|----------------------------------------------------|
| Load Balancer  | Load balancer used by Network service on NHN Cloud |

### Load Balancer Legend

| Legend Name     | Description            |
|-----------------|--------------------|
| loadbalancer_id | Load balancer name |
| listener_id     | Listener name      |
| pool_id         | Member group name  |
| member_id       | Member name        |

## Direct Connect
- A dictionary that defines metrics that can be monitored for the Direct Connect service on NHN Cloud.

### Metric List

| Metric Name                               | Resource Name | Default legend (Legend) | Unit                     |
|-------------------------------------------|---------------|-------------------------|--------------------------|
| Connection Status                         | Network       | {{id}}                  | Number                   |
| Number of connection receive errors       | Network       | {{id}}                  | Number                   |
| Number of connection send errors          | Network       | {{id}}                  | Number                   |
| Network transmitted bytes                 | Network       | {{id}}                  | 5 min accumulated bytes  |
| Network received bytes                    | Network       | {{id}}                  | 5 min accumulated bytes  |
| Network transmitted bits per second (bps) | Network       | {{id}}                  | Bits per second (bits/s) |
| Network received bits per second (bps)    | Network       | {{id}}                  | Bits per second (bits/s) |

### Direct Connect Filter

| Filter name | Description                                          |
|-------------|------------------------------------------------------|
| Service ID  | Service apply ID used by Direct Connect on NHN Cloud |

### Direct Connect Legend

| Legend Name | Description      |
|-------------|------------------|
| orderId     | Service apply ID |
