<!-- pre-align:aligned sig=e480d3f4c60f -->

## Monitoring > Cloud Monitoring > Instance New Metrics Integration Guide

<a id="overview"></a>

## Overview

To collect detailed instance metrics from the Cloud Monitoring service, you must install a new agent.
The new agent operates separately from the existing agent and provides more accurate and detailed instance metrics.

> [Caution]
> Autoscaling may not function properly for instances in an autoscale group.

The overall process is as follows:
1. Install new Agent
2. Delete existing Agent (optional)

<a id="new-agent-installation-guide"></a>

## New Agent Installation Guide

<a id="install-linux-instance-agent"></a>

### Install Linux Instance Agent

<a id="installation-script"></a>

#### Installation Script
```bash
rm -f ./install-nhncloud-telegraf.sh
curl -s -o install-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/install-nhncloud-telegraf.sh'
chmod 755 ./install-nhncloud-telegraf.sh
sudo ./install-nhncloud-telegraf.sh
```

<a id="check-installation"></a>

#### Check Installation
```bash
sudo systemctl status nhncloud-telegraf
```

<a id="install-windows-instance-agent"></a>

### Install Windows Instance Agent
* Run PowerShell as an administrator
   - Search for **PowerShell** in the Start menu.
   - Right-click **Windows PowerShell** and select **Run as administrator**.

<a id="installation-script-2"></a>

#### Installation Script
```powershell
Remove-Item install-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/install-nhncloud-telegraf.ps1' -OutFile 'install-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File install-nhncloud-telegraf.ps1
```

<a id="check-installation-2"></a>

#### Check Installation
```powershell
Get-Service -Name "nhncloud-telegraf"
```

<a id="existing-agent-deletion-guide-optional"></a>

## Existing Agent Deletion Guide (optional)

> [Note]
> You can use both new Agent and existing Agent simultaneously.

It is a guide to delete the existing System Monitoring Agent. New agents and existing agents work without problems even if they are installed at the same time.

<a id="precautions-when-deleting"></a>

### Precautions when Deleting
- You must check that new agents are installed and operated normally before deleting the existing Agent.

<a id="delete-linux-instance-existing-agent"></a>

### Delete Linux Instance Existing Agent

<a id="deletion-script"></a>

#### Deletion Script
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

<a id="check-deletion"></a>

#### Check Deletion
Check existing agent service status. (normal when there is no service)
```bash
sudo systemctl status toast-sysmon
```

<a id="delete-windows-instance-existing-agent"></a>

### Delete Windows Instance Existing Agent
<a id="deletion-script-2"></a>

#### Deletion Script
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

<a id="check-deletion-2"></a>

#### Check Deletion
Check if the existing agent process has been terminated.
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

<a id="delete-new-agent-if-necessary"></a>

### Delete New Agent (if necessary)

<a id="delete-linux-instance-new-agent"></a>

#### Delete Linux Instance New Agent

##### Deletion Script
```bash
rm -f ./uninstall-nhncloud-telegraf.sh
curl -s -o uninstall-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-nhncloud-telegraf.sh'
chmod 755 ./uninstall-nhncloud-telegraf.sh
sudo ./uninstall-nhncloud-telegraf.sh
```

<a id="delete-windows-instance-new-agent"></a>

#### Delete Windows Instance New Agent

##### Deletion Script
```powershell
Remove-Item uninstall-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/uninstall-nhncloud-telegraf.ps1' -OutFile 'uninstall-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File uninstall-nhncloud-telegraf.ps1
```

<a id="metric-dictionary"></a>

## Metric Dictionary

|Metrics name|Resource name|Legend| Unit|
|-------|-------|------|------|
|CPU usage (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|No. of CPU cores|CPU (New)|{{nhncloud_instance_id}}|Number|
|CPU utilization by core (%)|CPU (New)|{{nhncloud_instance_id}} cpu={{cpu}}|Percentage (0-100)|
|CPU average load (1m)|CPU (New)|{{nhncloud_instance_id}} - 1m|Number|
|CPU average load (5m)|CPU (New)|{{nhncloud_instance_id}} - 5m|Number|
|CPU average load (15m)|CPU (New)|{{nhncloud_instance_id}} - 15m|Number|
|CPU details (user) (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|CPU details (nice) (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|CPU details (system) (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|CPU details (iowait) (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|CPU details (steal) (%)|CPU (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|Memory usage (%)|Memory (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|Memory details (used) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|Bytes|
|Memory details (available) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|Bytes|
|Memory details (free) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|Bytes|
|Memory details (cached) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|Bytes|
|Memory details (buffered) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|Bytes|
|Disk usage (%)|Disk (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|Disk usage by device (%)|Disk (New)|{{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}}|Percentage (0-100)|
|Disk read (B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|Byte per second (bytes/s)|
|Disk write (B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|Byte per second (bytes/s)|
|Disk read by device (B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|Byte per second (bytes/s)|
|Disk write by device (B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|Byte per second (bytes/s)|
|No. of tasks being processed by device|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|Number|
|IO usage by device (%)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|Percentage (0-100)|
|Network data reception (B/s)|Network (New)|{{nhncloud_instance_id}}|Byte per second (bytes/s)|
|Network data transmission (B/s)|Network (New)|{{nhncloud_instance_id}}|Byte per second (bytes/s)|
|Network data reception by device (B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Byte per second (bytes/s)|
|Network data transmission by device (B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Byte per second (bytes/s)|
|Network data reception (bps)|Network (New)|{{nhncloud_instance_id}}|Bit per second (bit/s)|
|Network data transmission (bps)|Network (New)|{{nhncloud_instance_id}}|Bit per second (bit/s)|
|Network data reception by device (bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Bit per second (bit/s)|
|Network data transmission by device (bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Bit per second (bit/s)|
|Network packet reception (pps)|Network (New)|{{nhncloud_instance_id}}|Packet per second (packets/s)|
|Network packet transmission (pps)|Network (New)|{{nhncloud_instance_id}}|Packet per second (packets/s)|
|Network packet reception by device (pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Packet per second (packets/s)|
|Network packet transmission by device (pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|Packet per second (packets/s)|
|Operating time (s)|System (New)|{{nhncloud_instance_id}}|Time (second)|
|Swap utilization (%)|Swap (New)|{{nhncloud_instance_id}}|Percentage (0-100)|
|Swap utilization (used) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|Bytes|
|Swap usage (free) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|Bytes|
|Swap usage (total) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|Bytes|

<a id="gpu-instance-metric-dictionary"></a>

## GPU Instance Metric Dictionary

> [Note]
> GPU metrics are collected from GPU instances based on DCGM (Data Center GPU Manager) and can only be retrieved from GPU instances with the new Cloud Monitoring Agent installed.
> Some metrics may not be collected depending on the GPU model (V100/A100/T4) and driver version.

| Metric Name | Resource Name | Default Legend | Unit |
|-------|-------|------|------|
| GPU utilization (%) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Percentage (0–100) |
| GPU memory utilization (%) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Percentage (0–100) |
| GPU memory bandwidth utilization (%) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Percentage (0–100) |
| GPU power usage (W) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Watts (W) |
| GPU temperature (°C) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Celsius (°C) |
| GPU memory temperature (°C) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Celsius (°C) |
| SM clock (MHz) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Megahertz (MHz) |
| Memory clock (MHz) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Megahertz (MHz) |
| Encoder utilization (%) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Percentage (0–100) |
| Decoder utilization (%) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Percentage (0–100) |
| GPU free memory (MiB) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Mebibytes (MiB) |
| GPU reserved memory (MiB) | GPU performance | {{nhncloud_instance_id}} - gpu={{gpu}} | Mebibytes (MiB) |
| PCIe retransmit rate (count/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Count per second (count/s) |
| XID errors | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| ECC single-bit errors - cumulative (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| ECC single-bit errors - volatile (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| ECC double-bit errors - cumulative (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| ECC double-bit errors - volatile (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Retired pages - SBE (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Retired pages - DBE (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Pending retired pages (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Remapped rows - correctable (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Remapped rows - uncorrectable (count) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| Remapping failure status | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Number |
| NVLink CRC flit error rate (count/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Count per second (count/s) |
| NVLink CRC data error rate (count/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Count per second (count/s) |
| NVLink replay error rate (count/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Count per second (count/s) |
| NVLink recovery error rate (count/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Count per second (count/s) |
| NVLink bandwidth - Total (KiB/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Kibibytes per second (KiB/s) |
| NVLink bandwidth - L0 (B/s) | GPU status | {{nhncloud_instance_id}} - gpu={{gpu}} | Bytes per second (bytes/s) |
| Power throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |
| Thermal throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |
| Board limit throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |
| Low utilization throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |
| Sync boost throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |
| Reliability throttling rate (µs/s) | GPU clock events | {{nhncloud_instance_id}} - gpu={{gpu}} | Microseconds per second (µs/s) |

<a id="gpu-instance-filter"></a>

### GPU Instance Filter

| Filter Name | Description |
|------|------|
| Region | Region where the GPU instance is located |
| Instance | Name of the GPU instance |
| GPU | GPU device number within the instance |

<a id="gpu-instance-legend"></a>

### GPU Instance Legend

| Legend Name | Description |
|------|------|
| nhncloud_instance_id | Name of the GPU instance |
| gpu | GPU device number within the instance |