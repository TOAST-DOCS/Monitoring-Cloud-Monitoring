## Monitoring > Cloud Monitoring > Instance New Metrics Integration Guide

## Overview

To collect detailed instance metrics from the Cloud Monitoring service, you must install a new agent.
The new agent operates separately from the existing agent and provides more accurate and detailed instance metrics.

> [Caution]
> Autoscaling may not function properly for instances in an autoscale group.

The overall process is as follows:
1. Install new Agent
2. Delete old Agent (optional)

## New Agent Installation Guide

### Install Linux Instance Agent

#### Installation Script
```bash
rm -f ./install-nhncloud-telegraf.sh
curl -s -o install-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/install-nhncloud-telegraf.sh'
chmod 755 ./install-nhncloud-telegraf.sh
sudo ./install-nhncloud-telegraf.sh
```

#### Check Installation
```bash
sudo systemctl status nhncloud-telegraf
```

### Install Windows Instance Agent
* Run PowerShell as an administrator
   - Search for **PowerShell** in the Start menu.
   - Right-click **Windows PowerShell** and select **Run as administrator**.

#### Installation Script
```powershell
Remove-Item install-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/install-nhncloud-telegraf.ps1' -OutFile 'install-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File install-nhncloud-telegraf.ps1
```

#### Check Installation
```powershell
Get-Service -Name "nhncloud-telegraf"
```

## Old Agent Deletion Guide (optional)

> [Note]
> You can use both new Agent and old Agent simultaneously.

It is a deletion guide for removing the existing System Monitoring Agent. New agents and old agents work without problems even if they are installed at the same time.

### Precautions when Deleting
- **Required confirmation before deletion **: check that new agents are installed and operated normally

### Delete Linux Instance Old Agent

#### Deletion Script
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

#### Check Deletion
* Check old agent service status (normal when there is no service)
```bash
sudo systemctl status toast-sysmon
```

### Delete Windows Instance Old Agent
#### Deletion Script
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

#### Check Deletion
* Check old agent process termination
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

### Delete New Agent (if necessary)

#### Delete Linux Instance New Agent

##### Deletion Script
```bash
rm -f ./uninstall-nhncloud-telegraf.sh
curl -s -o uninstall-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-nhncloud-telegraf.sh'
chmod 755 ./uninstall-nhncloud-telegraf.sh
sudo ./uninstall-nhncloud-telegraf.sh
```

#### Delete Windows Instance New Agent

##### Deletion Script
```powershell
Remove-Item uninstall-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/uninstall-nhncloud-telegraf.ps1' -OutFile 'uninstall-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File uninstall-nhncloud-telegraf.ps1
```

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
