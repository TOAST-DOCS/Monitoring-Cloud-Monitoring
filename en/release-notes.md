## Monitoring > Cloud Monitoring > Release Notes

### April 28, 2026

#### Added a dashboard template feature

Added a feature to easily create dashboards by selecting a pre-configured template when creating a dashboard.
Added a feature to select a template by service and preview the widget configuration and layout.

#### Added a dynamic filter feature

Added a feature to filter data across all widgets on a dashboard at once using the dynamic filter at the top of the dashboard.
Added a feature to add or modify filters in the dynamic filter management modal, and configure whether to apply dynamic filters per widget.

#### Added an aggregation feature

Added a feature to automatically calculate and display collected metric data in widgets and alerts using aggregation functions such as average, minimum, and maximum.
Added a feature to aggregate all data within intervals when data intervals are automatically adjusted based on the query period, ensuring no data is missed and the overall trend is captured.
Added a feature to select whether to use aggregation per metric; if aggregation is not used, the original data is displayed as before.

### September 23, 2025

#### Release of a New Cloud Monitoring Agent

Cloud Monitoring Agent for new instances has been released.
* You can install it by referring to the [New Agent Installation Guide](new-instance-metric.md).

### July 29, 2025

#### Added a new service to view metrics

Added a new service for which metrics can be viewed in Cloud Monitoring.
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* Cloud Functions

### June 24, 2025

#### Added a new service to view metrics

Added a new service for which metrics can be viewed in Cloud Monitoring.
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* SMS

### June 10, 2025

#### Added SMS notification content

Added a new item to the SMS content sent upon notification.
When the notification is triggered by a service of type Instance, the Instance Name is included in the message.

### May 27, 2025

#### Added a new service to view metrics

Added a new service for which metrics can be viewed in Cloud Monitoring.
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* VPC
* Subnet
* Floating IP

### May 4, 2025

#### Add New Service to View Metrics

Added a new service for which metrics can be viewed in Cloud Monitoring  
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* Direct Connect

### February 11, 2025

#### Add New Service to View Metrics

Added a new service for which metrics can be viewed in Cloud Monitoring  
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* Colocation Gateway
* Load Balancer

### October 29, 2024

#### Apply Permission Segmentation

Added a role to use project services to Cloud Monitoring.

* Cloud Monitoring ADMIN: Create, Read, Update, and Delete Cloud Monitoring
* Cloud Monitoring VIEWER: Read Cloud Monitoring

#### Support for Custom Webhooks

You can receive Cloud Monitoring notifications as webhooks using custom webhooks in the notification receiver group.

### August 27, 2024

#### Add New Service to View Metrics

Added a new service for which metrics can be viewed in Cloud Monitoring  
Metrics for the services below are available in the dashboard after setting up collection in the Manage Metrics screen.

* Transit Hub
* Internet Gateway

### July 23, 2024

### Bug Fixes

* [Console] Fixed an issue where, when pressing the enter key on the text entry window from the Add/Modify Widgets and Notifications page, an unintended save attempt occurs.

### May 28, 2024

#### Release of a New Service

Cloud Monitoring collects and provides metrics for resources in NHN Cloud and provides notifications about abnormalities. 

* Collects and provides system and service metrics for resources in NHN Cloud, such as Instance, GPU Instance, NCS, etc.
* Creates and manages dashboards flexibly and checks resource health easily.
* You can configure metric charts in the organization and project dashboards and monitoring console in any form you want, and when a metric reaches a certain threshold, notifications can be sent via email, SMS, and more to predetermined notification recipients.
