## Monitoring > Cloud Monitoring > Overview
**Monitoring > Cloud Monitoring** collects and provides system/service metrics for resources including instance servers in NHN Cloud.
You can configure metric charts in the organization and project dashboards and monitoring console in any form you want.
When a metric reaches a certain threshold, you can specify who you want to be notified and set up notifications via email, SMS, and more.

## Main Features
### Compute > Instance Server Monitoring
For instance servers, Cloud Monitoring collects system metrics with Cloud Monitoring Agent installed on each instance server.
System metrics are automatically collected when the instance is running because the agent is included in the instance image by default.

### Metric Dashboard
You can understand the status of each server with charts for various system metrics of server instances created in ** Compute > Instance** and resources in NHN Cloud.
You can select a metric widget and place it on the dashboard, and create multiple dashboards to manage according to your purpose.

Metrics are collected every minute and kept for up to 52 weeks.

### Notification Conditions
You can set thresholds for the collected metrics to monitor your NHN Cloud resources at all times and identify abnormalities.
For example, if the CPU usage of an instance server exceeds 90%, or if the usage of a specific NIC exceeds 1000 pps, various monitoring items to understand the status of your server are provided.

### Notification Methods: Email, SMS
You can choose how you want to be notified when something happens that meets the notification conditions you set.
You can be notified by email or SMS.

## Glossary
| Term       | Description                                                                                                 |
|----------|----------------------------------------------------------------------------------------------------|
| Metric       | Metric for each resource, which is collected by Cloud Monitoring. For instance servers, metrics for CPU usage, load average 1m, and memory usage are collected. | 
| Dashboard     | A bundle of metric widgets. You can arrange the widgets the way you want, and you can create multiple dashboards to manage them for different purposes.                        |                     
| Notification Receiver Group | A list of users who will be notified when events occur.                                                                      |                                                                       
| Notification Group    | Set thresholds and specify which instances to monitor, and which notification receiver groups to send notifications to when events occur.                                     |                                      
| Notification Condition Settings | Detailed settings for each metric threshold.                                                                                |                                                                                 
