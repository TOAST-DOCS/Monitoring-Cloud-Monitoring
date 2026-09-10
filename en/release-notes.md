<!-- machine_translated: true -->

<!-- pre-align:aligned sig=31661ef58a0f -->

<a id="monitoring-cloud-monitoring-release-notes"></a>
## Monitoring > Cloud Monitoring > Release Notes { #monitoring-cloud-monitoring-release-notes }

<a id="july-28-2026"></a>
## September 29, 2026

### Added Features

* Added anomaly detection
    * Added an anomaly detection feature that learns historical patterns of metrics collected by Cloud Monitoring and automatically detects abnormalities that deviate from normal behavior.
    * After you select the metrics and resources to monitor and create an anomaly detection item, you can view the metric values, Score, and Score Threshold in the widget chart on the anomaly detection dashboard.
    * You can set notifications for the anomaly detection items you created to receive alerts when abnormalities occur.

<a id="july-28-2026"></a>
## July 28, 2026 { #july-28-2026 }

<a id="feature-updates"></a>
### Feature Updates { #feature-updates }

* Added widget legend area expansion feature
    * When a widget has many legend items, hovering over the legend area displays an expanded legend area.
    * In the expanded area, legend items can be viewed at a glance, and data can be conveniently filtered by selecting the desired items.
* Changed the time zone for notification email occurrence time
    * The occurrence time displayed in notification emails has been changed from UTC to Korea Standard Time (KST).

<a id="june-23-2026"></a>
## June 23, 2026 { #june-23-2026 }

<a id="added-features"></a>
### Added Features { #added-features }

* Added detailed metrics for GPU instances
    * Detailed metrics for GPU instances can now be collected through the new Cloud Monitoring Agent.
    * Provides metrics for GPU performance, GPU status, and GPU clock events based on DCGM (Data Center GPU Manager).
    * For installation, see the [New Agent Installation Guide](new-instance-metric.md).

<a id="april-28-2026"></a>
## April 28, 2026 { #april-28-2026 }

<a id="april-28-2026-added-features"></a>
### Added Features { #april-28-2026-added-features }

* Added dashboard template feature
    * When creating a dashboard, you can select a pre-configured template to create a dashboard quickly.
    * You can select a template by service and check the widget configuration and layout in the preview.
* Added dynamic filter feature
    * The dynamic filter at the top of the dashboard allows you to filter data across all widgets in the dashboard at once.
    * Filters can be added or modified in the dynamic filter management modal, and you can configure whether to apply the dynamic filter for each widget.
* Added aggregation feature
    * Metric data collected in widgets and notifications can be automatically calculated and displayed using aggregation functions such as average, minimum, and maximum.
    * When the data interval is automatically adjusted based on the retrieval period, all data within the interval is aggregated and reflected, allowing you to understand the overall trend without missing any data.
    * You can choose whether to use aggregation for each metric. If aggregation is not used, the raw data is displayed as before.

<a id="september-23-2025"></a>
## September 23, 2025 { #september-23-2025 }

<a id="september-23-2025-added-features"></a>
### Added Features { #september-23-2025-added-features }

* Released new Cloud Monitoring Agent
    * A new Agent for Cloud Monitoring instances has been released.
    * For installation, see the [New Agent Installation Guide](new-instance-metric.md).

<a id="july-29-2026"></a>
## July 29, 2026 { #july-29-2026 }

<a id="july-29-2026-added-features"></a>
### Added Features { #july-29-2026-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Cloud Functions

<a id="june-24-2025"></a>
## June 24, 2025 { #june-24-2025 }

<a id="june-24-2025-added-features"></a>
### Added Features { #june-24-2025-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * SMS

<a id="june-10-2025"></a>
## June 10, 2025 { #june-10-2025 }

<a id="june-10-2025-feature-updates"></a>
### Feature Updates { #june-10-2025-feature-updates }

* Added SMS notification content
    * An item has been added to the SMS content when sending notifications.
    * The Instance Name item has been added when the service that triggered the notification is Instance.

<a id="may-27-2025"></a>
## May 27, 2025 { #may-27-2025 }

<a id="may-27-2025-added-features"></a>
### Added Features { #may-27-2025-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * VPC
        * Subnet
        * Floating IP

<a id="march-4-2025"></a>
## March 4, 2025 { #march-4-2025 }

<a id="march-4-2025-added-features"></a>
### Added Features { #march-4-2025-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Direct Connect

<a id="february-11-2025"></a>
## February 11, 2025 { #february-11-2025 }

<a id="february-11-2025-added-features"></a>
### Added Features { #february-11-2025-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Colocation Gateway
        * Load Balancer

<a id="october-29-2024"></a>
## October 29, 2024 { #october-29-2024 }

<a id="october-29-2024-added-features"></a>
### Added Features { #october-29-2024-added-features }

* Added custom webhook support
    * Cloud Monitoring notifications can now be received via webhook using the custom webhook in the notification recipient group.

<a id="october-29-2024-feature-updates"></a>
### Feature Updates { #october-29-2024-feature-updates }

* Applied granular permissions
    * Project service usage roles have been added to Cloud Monitoring.
    * Cloud Monitoring ADMIN: Cloud Monitoring service Create, Read, Update, Delete
    * Cloud Monitoring VIEWER: Cloud Monitoring service Read

<a id="august-27-2024"></a>
## August 27, 2024 { #august-27-2024 }

<a id="august-27-2024-added-features"></a>
### Added Features { #august-27-2024-added-features }

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Transit Hub
        * Internet Gateway

<a id="july-23-2024"></a>
## July 23, 2024 { #july-23-2024 }

<a id="bug-fixes"></a>
### Bug Fixes { #bug-fixes }

* [Console] Fixed an issue where pressing the Enter key in the text input field on the widget and notification add/edit page unintentionally attempted to save.

<a id="may-28-2024"></a>
## May 28, 2024 { #may-28-2024 }

<a id="may-28-2024-added-features"></a>
### Added Features { #may-28-2024-added-features }

* Released new service
    * Cloud Monitoring is a service that collects and provides resource metrics from NHN Cloud and sends notifications when anomalies occur.
    * Collects and provides system and service metrics for resources within NHN Cloud, including Instance, GPU Instance, and NCS.
    * Flexible dashboard creation and management features allow you to easily monitor resource status.
    * You can configure metric charts of your preferred type on the organization and project dashboard or the monitoring console, and set up notifications to be sent by email, SMS, and more to pre-designated notification recipients when metrics reach a specific threshold.