## Monitoring > Cloud Monitoring > Release Notes

## June 23, 2026

#### Added Features

* Added detailed metrics for GPU instances
    * Detailed metrics for GPU instances can now be collected through the new Cloud Monitoring Agent.
    * Provides metrics for GPU performance, GPU status, and GPU clock events based on DCGM (Data Center GPU Manager).
    * For installation, see the [New Agent Installation Guide](new-instance-metric.md).

## April 28, 2026

### Added Features

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

## September 23, 2025

### Added Features

* Released new Cloud Monitoring Agent
    * A new Agent for Cloud Monitoring instances has been released.
    * For installation, see the [New Agent Installation Guide](new-instance-metric.md).

## July 29, 2026

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Cloud Functions

## June 24, 2025

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * SMS

## June 10, 2025

### Feature Updates

* Added SMS notification content
    * An item has been added to the SMS content when sending notifications.
    * The Instance Name item has been added when the service that triggered the notification is Instance.

## May 27, 2025

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * VPC
        * Subnet
        * Floating IP

## March 4, 2025

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Direct Connect

## February 11, 2025

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Colocation Gateway
        * Load Balancer

## October 29, 2024

### Added Features

* Added custom webhook support
    * Cloud Monitoring notifications can now be received via webhook using the custom webhook in the notification recipient group.

### Feature Updates

* Applied granular permissions
    * Project service usage roles have been added to Cloud Monitoring.
    * Cloud Monitoring ADMIN: Cloud Monitoring service Create, Read, Update, Delete
    * Cloud Monitoring VIEWER: Cloud Monitoring service Read

## August 27, 2024

### Added Features

* Added services available for metric retrieval
    * Added services for which metrics can be retrieved in Cloud Monitoring.
    * Metrics for the following services can be viewed on the dashboard after configuring collection settings in the metric management screen.
        * Transit Hub
        * Internet Gateway

## July 23, 2024

### Bug Fixes

* [Console] Fixed an issue where pressing the Enter key in the text input field on the widget and notification add/edit page unintentionally attempted to save.

## May 28, 2024

### Added Features

* Released new service
    * Cloud Monitoring is a service that collects and provides resource metrics from NHN Cloud and sends notifications when anomalies occur.
    * Collects and provides system and service metrics for resources within NHN Cloud, including Instance, GPU Instance, and NCS.
    * Flexible dashboard creation and management features allow you to easily monitor resource status.
    * You can configure metric charts of your preferred type on the organization and project dashboard or the monitoring console, and set up notifications to be sent by email, SMS, and more to pre-designated notification recipients when metrics reach a specific threshold.