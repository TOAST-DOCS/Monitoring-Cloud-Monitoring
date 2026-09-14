<!-- machine_translated: true -->

<!-- pre-align:aligned sig=503aff601f8b -->

<a id="monitoring-cloud-monitoring-console-user-guide"></a>
## Monitoring > Cloud Monitoring > Console User Guide { #monitoring-cloud-monitoring-console-user-guide }

This document explains the basics of using the Cloud Monitoring service.

<a id="dashboard"></a>
## Dashboard { #dashboard }

In **Monitoring > Cloud Monitoring > Dashboard**, you can create chart widgets and configure dashboards to view various metrics collected from resources created by NHN Cloud services.

![Auto-refresh view periods](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-1.png)

The metric data view period for user dashboards defaults to retrieving data up to five minutes prior to the current time. The default auto-refresh interval is 1 minute.

![Customize the view period](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-2.png)

If you set a custom duration, auto-refresh is disabled.

<a id="view-modeedit-mode"></a>
### View Mode/Edit Mode { #view-modeedit-mode }

![Dashboard view mode](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-1.png)

![Dashboard edit mode](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-2.png)

The dashboard has two modes: view mode and edit mode.

![View Mode Header](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-3.png)

Dashboard appears in the view mode by default, and to modify a dashboard or widget, you must click the Edit mode toggle to switch to the edit mode.

![Edit Mode Header](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-4.png)

In the edit mode, you can edit the name or description of a dashboard, or clone or delete a dashboard. You can also edit each widget, or reposition and clone widgets.

![Full save notification modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-5.png)

Any changes you make to the widget, such as adding a widget or modifying its location and size, don't take effect until you click **Save All**. If you don't, you'll see a save notification modal, and any unsaved changes will disappear.

<a id="create-a-dashboard"></a>
### Create a Dashboard { #create-a-dashboard }

![Add Dashboard Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-1.png)

In the view mode, click **+** to the right of the **Dashboard** tab to open the Add dashboard modal.

![Blank dashboard](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-2.png)

If no dashboards have been created, you'll see **+ Create Dashboard**.

![After creating a dashboard](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-3.png)

Enter a **dashboard name** and **dashboard description**. The **dashboard name** is a required value, and can be set to a duplicate name, but we recommend using a unique name whenever possible.
**Dashboard description** is an optional value and you can enter something descriptive of the dashboard.

<a id="create-a-dashboard-dashboard-template"></a>
#### Dashboard Template

Configure a dashboard manually or start with a preconfigured template. Select whether to use the **Dashboard Template** option.

- **Enable**: The template selection area is displayed. Selecting a service displays the list of templates for the service.
- **Disable** (default): An empty dashboard is created without a template.

If you select to use a template, select a service and a template respectively. When a template is selected, the template name is automatically entered in the dashboard name field, and the name can be modified even after it has been automatically entered.

Click the **Preview** button in the template list to open the template preview modal.

In the preview modal, you can preview the widget configuration and layout included in the template. Sample data is displayed in the preview screen, and you can view the actual data after the dashboard is created.

<a id="set-up-a-dashboard"></a>
### Set up a Dashboard { #set-up-a-dashboard }

![Dashboard example](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-1.png)

You can add widgets and groups of widgets to a dashboard. You can add up to 12 widgets per dashboard, and they are added to the bottom of the dashboard when you add them.

![Widget examples](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-2.png)

Widgets are the smallest unit of organization for a dashboard. They can be created by clicking **+ Add Widget** or by selecting **Add Widget**, **Add Widget Template** from the drop-down list of the corresponding button. The size and position of widgets can be freely changed in dashboard edit mode.

![Widget group example](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-3.png)

Widget groups allow you to manage multiple widgets by grouping them together. Widget groups can be collapsed or expanded to hide and show multiple widgets, and the height and width of the widget group automatically adjusts to the size of the widgets within the group.

<a id="set-up-a-dashboard-addedit-a-widget-and-widget-group"></a>
#### Add/Edit a Widget and Widget Group

![Add Widget button area](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a-1.png)

Widgets and widget groups can be added in both view mode and edit modes. However, to modify widgets and widget groups, you must switch to the edit mode.

##### Add a Widget

![About the Add Widget screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-1.png)

Adding widget allows you to create your own chart widget with the metrics and filters you want.
The widget name, graph type, service, and Metrics settings > Metrics are required values and must be filled in.
A single widget can only represent a single service. However, you can select multiple metric items.

![Select the Add Widget screen metrics item and click](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-2.png)

Each time you select a metric item, elements are added at the bottom of the screen that allow you to set filters and a legend for the metric item.
You can only label one metric filter per type, and all filters are finally applied in the form of an `&` operation. Therefore, when applying multiple filters, the search results for a condition value will only show search results that meet all of the previously set filter criteria. Depending on the operator and condition values of the filters you added earlier, there may be no more condition values to choose from.

The legend is a name to distinguish the metric data viewed by each metric item. When you add a metric item, it automatically populates a suggested name by default.You can add any text before or after the placeholder wrapped in double curly braces syntax `{{ }}`. If you don't enter any text, it will concatenate and expose any label properties the indicator item has.
Select Units to specify the y-axis title and units to be exposed in the chart. The actual value of the metric item is exposed to 15 decimal places (rounded to the 16th place, except when `Percent (0.0-1.0`) is selected, in which case the value is converted to 0-100 and exposed), without support for separate formatting based on units. The Y-axis position setting allows you to choose between **Auto**, **Left**, and **Right** for the Y-axis position of the metric item. When adding a metric item, the Auto value is selected by default. If all metric items are selected Auto, they will be sequentially positioned on the Y-axis as either Left or Right. If a metric exists with a left or right y-axis position, it will be placed in the same y-axis direction. If any metric items have the same unit and y-axis position, they are represented on the same y-axis.

###### Query Settings Block

When a metric item is selected, a metric settings block for that metric is added, and one query settings block is included in the metric settings block by default.

A query settings block is a unit for configuring filters, legends, aggregation, and more for each individual query. Multiple query settings blocks can be added within a single metric settings block, and each query is automatically numbered in alphabetical order (A, B, C, ...).

- **Add**: Click the **+** icon in the metric settings block to add a query settings block at the bottom.
- **Copy**: Click the copy icon in the query settings block to add a query with all filter, legend, and aggregation settings duplicated.
- **Delete**: The delete icon is activated when there are two or more query settings blocks.
- **Collapse/Expand**: When a query settings block is collapsed, key summary information such as filters and aggregation is displayed in the title area.

Filter, aggregation, and other settings values can be duplicated across query settings blocks. Each is treated as an independent query, so even if the settings values are identical, all queries are displayed in the widget.

###### Aggregation Settings

When the query period is extended, the data interval displayed in the chart is automatically adjusted. In this case, individual data points within the data interval may not be reflected in the chart.
Using the aggregation feature allows all data within the data interval to be calculated using aggregation functions such as average, minimum, and maximum, and displayed in the chart.
The aggregation settings area is displayed only for metrics that support aggregation.

- **Disable** (default): Displays the actual data value at each point without processing. Depending on the query period, some data within the data interval may not be reflected in the chart.
- **Enable**: Allows you to select an aggregation item (average, minimum, maximum). Since all data that occurred within the data interval is aggregated and reflected, it is easier to identify the overall flow and trend.

The data intervals by query period are as follows:

| Query period | Data interval |
|---------|----------|
| ~ 5 min     | 15 sec     |
| ~ 30 min    | 30 sec     |
| ~ 1 hr   | 1 min      |
| ~ 6 hr   | 5 min      |
| ~ 12 hr  | 10 min     |
| ~ 24 hr  | 20 min     |
| ~ 2 days    | 30 min     |
| ~ 7 days    | 2 hr    |
| ~ 14 days   | 3 hr    |
| ~ 27 days   | 6 hr    |
| ~ 366 days  | 24 hr   |

For example, if the query period is set to 24 hours, the data interval becomes 20 minutes, and data between intervals is not directly displayed in the chart. Using aggregation allows all data within the 20-minute interval to be reflected.

The following is an example of aggregation applied with a 5-minute data interval. Gray dots represent the original collected data, and red dots represent the values actually displayed in the chart.

![Aggregation comparison](https://static.toastoven.net/prod_cloud_monitoring/20260407_aggregation_compare_en.png)

Aggregation Off is the case where aggregation is not used. Only the data at 12:05 and 12:10 are displayed in the chart, and the data collected in between (0.8, 5.0, 1.0) cannot be confirmed in the chart.
Aggregation On is the case where average aggregation is used. Since the average of all data within each interval is calculated and displayed in the chart, data collected between intervals is also reflected in the results.

###### Apply Dynamic Filter

The **Apply Dynamic Filter** toggle allows you to configure whether to apply the dynamic filter conditions selected at the top of the dashboard to the widget. The default value is **Enable**. When dynamic filters are applied, the conditions selected in the dashboard top filter are always applied.

![Widget Add Screen Preview Layer](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-3.png)

After you change the graph type or modify the metric item filters, you can preview how the chart widget will look with your changes. Click the **Preview** toggle in the top-right corner of the screen to open or close the preview layer, where you can see the chart widget in real time with your filters and legend values applied. The preview layer is adjustable for left and right width.

##### Add a Widget Template

![Add Widget Template Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_02-1.png)

Widget templates are a quick and easy way to create widgets using pre-configured widget metric items. After adding the widget, you can edit the widget to add filters to the metric items or change the metric items and names.
Note that some widgets added with widget templates can only be deleted and not edited.

##### Add a Widget Group

![Add Widget Group Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-1.png)

You can add a group of widgets to your dashboard. To add a widget to a widget group, simply drag the title area at the top of the widget in edit mode and move it inside the widget group.

Widget groups can be edited just like widgets, and to edit a widget group, you need to enter edit mode.

![Widget group context menu](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-2.png)

- Click **Edit** to expand the **Edit Widget Group** modal.
- Click **Delete Group** to remove only the group, leaving the widget's location and size information intact.
- Click **Delete Groups and Child Widgets** to delete all widgets within the group.

<a id="set-up-a-dashboard-moveclonedelete-a-widget"></a>
#### Move/Clone/Delete a Widget

![Resizing widgets](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-1.gif)

Once you're in Edit mode, you can resize the widget by dragging the bottom right corner, or reposition it by dragging the top area of the widget.

![Widget context menu](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

- You can delete the widget by clicking **Delete**.
- You can duplicate a widget in a dashboard by clicking **Clone Widget to Other Dashboard**. The cloned widget is added at the bottom.
- You can clone a widget on another dashboard by clicking **Clone Widget to Other Dashboard**. This opens a modal where you can select the dashboard to which you want to add the widget.

![Clone widget to another dashboard modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-2.png)

<a id="set-up-a-dashboard-create-a-notification"></a>
#### Create a Notification

![Widget context menu](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

Clicking **Create Notification** takes you to the **Manage Notifications** > **Create Notification**. You can easily create an notification with the widget's information filled in, including the widget name, service, metric item, and metric item filter information.
You can easily create a notification entering only the notification condition and the recipient of the notification.

![If you accessed the Create widget notification](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_c-1.png)

<a id="dynamic-filter"></a>
### Dynamic filter { #dynamic-filter }

The dynamic filter is a feature that filters data across all widgets at once from the common filter area at the top of the dashboard, without modifying individual widgets one by one.

Dynamic filters are grouped and arranged by service. They are automatically arranged from left to right according to internally defined priorities based on the dependencies between filter items.

When a dynamic filter item is changed, it is immediately reflected in the widgets on the dashboard. When the selected value of a left filter is changed, the items in the right filter are updated to match the changed conditions, and the selection state of the right filter is reset.

The dynamic filter is displayed as follows depending on the selection state:

| Selection state | Display format | Example |
|---------|---------|------|
| All selected (default) | `All` | All |
| 1 item selected | Selected filter value | Korea (Pangyo) |
| 2 or more items selected | `{filter value} and N more` | Korea (Pangyo) and 2 more |
| No items selected | `No items selected` | No items selected |
| No items available | `No items available` | No items available |

> Note: Dynamic filters are applied only to widgets with the **Apply Dynamic Filter** toggle enabled in the widget add/edit screen.

<a id="dynamic-filter-management"></a>
#### Dynamic Filter Management

Click the **Dynamic Filter Management** button in view mode to open the dynamic filter management modal. The Dynamic Filter Management button is not displayed in edit mode.

Dynamic filters are managed independently for each dashboard. The name of the dashboard to which the dynamic filter currently being configured applies is displayed at the top of the modal.

- **Add**: Click the **Add** button to add a new row at the bottom of the dynamic filter list. Enter the following items:
  - **Filter name**: Enter the name of the filter to be displayed at the top of the dashboard.
  - **Service**: Select the service to apply the dynamic filter to. (e.g., Instance, Load Balancer)
  - **Label**: Select the label available for the selected service. (e.g., when Instance service is selected, region, instance, etc.)
- **Edit**: Click the **Edit** button of an existing dynamic filter to modify the filter name, service, and label.
- **Delete**: Click the **Delete** button to delete the dynamic filter.

The same combination of service and label cannot be added as a duplicate.

!!! tip "Note"
    When selecting an instance in the dynamic filter for the Instance service, both instances with existing agents and instances with new agents installed are displayed.
    Since the supported metrics differ depending on the agent type, metrics that do not correspond to the agent type of the selected instance may not display data.
    For metrics supported by the new agent, refer to the [New Agent Installation Guide](new-instance-metric.md).

<a id="manage-a-dashboard"></a>
### Manage a Dashboard { #manage-a-dashboard }

![View Mode Header](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-1.png)

![Dashboard Management Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-2.png)

Click **Manage Dashboards** to display the Manage dashboards modal. You can view or edit the dashboard's name, description, creation date, and whether the project dashboard is visible or not.

![Manage Dashboards Modal > Edit Mode](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-3.png)

You can click the **Edit** or Delete icon in each dashboard's **Edit** column to edit the name and description of that dashboard or delete the dashboard.
You can click the**Project Dashboard Visibility Settings** toggle to set the visibility of that dashboard on the Project custom dashboards screen. Even if you turn off the visibility setting, it is always visible in the Cloud Monitoring service.

<a id="download-widget-data"></a>
### Download Widget Data { #download-widget-data }

![Download Widget Data menu](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_05-1.png)

You can download all the widget data for a dashboard as a .png, .csv, or .xlsx file. The files are saved with the dashboard name, and in the case of .csv files, they are downloaded as a .zip file compressed with the dashboard name. Inside it contains individual .csv files with the name of each widget.
For .csv and .xlsx files, you can only download up to 3 months of data based on the start date. If the view period is less than one month, data is provided in 5-minute intervals, and if it is more than one month, data is provided in 1-day intervals.
The longer the view period you specify or the more metric data the widget and the widget contains, the longer the download might take.

<a id="manage-notifications"></a>
## Manage Notifications { #manage-notifications }

In **Monitoring > Cloud Monitoring > Notification Settings**, you can add notifications to your NHN Cloud resources and check the history of notification occurrences.

![Notification settings list screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01-1.png)

<a id="notification-settings"></a>
### Notification Settings { #notification-settings }

![Notification Settings List Screen - Created](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-4.png)

The Notification settings screen displays a table where you can view information about the notifications you've created, and you can sort the table by notification name, whether the notification is enabled, and when it was created.
- You can enable or disable notifications by clicking the **Enable Notifications** toggle.
- Click **View** in the **View Notification Details** column to display the **Notification Details** modal.
- Click **Edit** in the **Edit** column to go to the **Edit Notification** screen.
- Clicking on each row of notifications takes you to the **Notification Occurred History** tab, where the notifications are automatically looked up and displayed.

<a id="notification-settings-createedit-notifications"></a>
#### Create/Edit Notifications

![Create/Edit Notifications Screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-1.png)

The name of the notification's basic information, the service and metric items in the service and notification settings, the notification conditions, and the recipients of the notification are required values and must be entered.
You can only select a single service for the notification, but you can select multiple metric items.

![Create/Edit Notification Screen - Metrics Selected](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-2.png)

When a metric item is selected, a metric settings block for that metric is added, and one query settings block is included in the metric settings block by default. A query settings block is a unit for configuring filters, aggregation, conditions, and more for each individual query, and multiple query settings blocks can be added within a single metric settings block.
For metrics that support aggregation, the aggregation settings area is displayed within the query settings block. Selecting **Enable** allows you to select an aggregation item (average, minimum, maximum), and selecting **Disable** (default) evaluates alerts based on the original data.

You don't need to enter a filter for the metric entry, but you must enter at least one condition. Set the conditions you want to be notified on with a combination of comparison method, threshold, and duration.

![Notification Settings List Screen - Notification Recipients](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-3.png)

You must select at least one notification recipient. Only notification recipient types are supported for notification recipient groups, which can be managed on the **Project Management > Notification Receiver Group Management** screen. [[Go to User Guide]](/nhncloud/en/console-guide/#notification-receiver-group-management)

You can receive notifications as custom webhooks in the Notification Receiver Group.

- List of parameters to provide as custom webhook request data
  
| Value | Description | Type | Remarks |
| --- | --- | --- | --- |
| orgName | Organization name | String |  |
| projectName | Project name | String |  |
| tenantType | Service type | String | `organization`(custom dashboard)<br>`project`(Cloud Monitoring) |
| referenceKey | Organization or project ID | String |  |
| serviceName | Service name | String |  |
| alertName | Notification name | String |  |
| alertId | Notification ID | String |  |
| eventsCount | Number of events occurring | Integer |  |
| events | Notification event | List<Object\> | See the events parameter list |

- events parameter list

| Value | Description | Type | Remarks |
| --- | --- | --- | --- |
| events[].resourceTypeName | Resource type name (En) | String | |
| events[].enMetricName | Metric name (En) | String | |
| events[].threshold | Threshold | String | String as Double |
| events[].operator | Comparison Method | String | Enum`(EQUAL`, `NOT_EQUAL`, `GREATER_THAN`, `LESS_THAN`, `GREATER_THAN_OR_EQUAL`, `LESS_THAN_OR_EQUAL`) |
| events[].duration | Duration | String | The value set in the condition |
| events[].result | Detected value | String | String as Double |
| events[].startAt | Event Occurred at | String | ex) `2024-10-29T08:44:22Z` |
| events[].endAt | Event Ended at | String | ex) `2024-10-29T08:44:22Z` |
| events[].contMinutes | Event duration (minutes) | Integer | The difference between the time the event occurred and the current time (minutes) |
| events[].labels | Where event occurred | Map<String, String\> | |


<a id="notification-settings-view-notification-details-modal"></a>
#### View Notification Details Modal

![View Notification Details Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_b-1.png)

In the alert details modal, you can view the detailed information of the configured alert. You can view the alert name, description, service, metric item filters and alert conditions, aggregation settings, and alert recipients. For metrics that support aggregation, the configured aggregation value (disable/average/maximum/minimum) is displayed, and for metrics that do not support aggregation, - is displayed.

<a id="notification-history"></a>
### Notification History { #notification-history }

![Notification occurrence history view screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)

You can use search filters and tables to view the history of notifications that have occurred, and tables to view the information of notifications that have occurred.
You can view the alert name, occurrence time, end time, service, resource, metric item, aggregation, result value, and duration. For metrics that support aggregation, the configured aggregation value is displayed, and for metrics that do not support aggregation, - is displayed. You can change the table sort order by occurrence time or end time.

> Notes: Duration refers to the time from when the notification occurs to when the notification ends.
If you disable a notification before it ends while it is still occurring, the duration can continue to increase because the notification was not explicitly ended.

<a id="notification-history-view-the-history-of-notification-occurrences"></a>
#### View the history of notification occurrences

![Notification history search filters](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_a-1.png)

You can use the notification name, notification status, Metric item, and Occurrence time filters to view the history of notification occurrences. Click **Initialize** to initialize the search filters.

<a id="notification-history-view-notification-send-history-modal"></a>
#### View Notification Send History Modal

![View notification sending history screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)
For each notification, click **View** in the **View Notification Send History** column to open the **View Notification Send History** modal.

![View Notification Send History Modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_b-1.png)

In the history modal, you can view detailed information on notification settings such as **Occurred Date**, ** Duration**, **Metric Item**, **집계**, **Result**, **Notification Conditions**, and **Occurred Location**.

The actual history of sending notifications is also provided in a table. You can see the notification sending date, notification method, recipient, and notification result for each notification sending history.
You can change the table sorting by notification date, notification method, and notification time.

<a id="manage-metrics"></a>
## Manage Metrics { #manage-metrics }

In **Monitoring > Cloud Monitoring > Manage Metrics**, you can set whether to collect service-specific metrics for NHN Cloud resources.

<a id="set-up-metric-collection"></a>
### Set up Metric Collection { #set-up-metric-collection }

![Manage metrics screen](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-1.png)

A table displays where you can set up metric collection by service.
For each service, you can see the **category**, **service**, **whether the service is enabled**, and **metric collection settings**, and you can click the **Metric Collection Settings** toggle to set whether metrics are collected.

![Confirmation to start collecting metrics modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-2.png)

![Metric collection stop confirmation modal](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-3.png)

When you start/stop collecting metrics, a confirmation modal opens.

![Example of a broken metric widget](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-4.png)

![Example of the widget when metrics are being collected](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-5.png)

If you stop collecting metrics, the metrics are no longer displayed in widgets that you've created using metrics from that service, and the metrics' legends are disabled.

<a id="anomaly-detection"></a>
## Anomaly Detection { #anomaly-detection }

**Monitoring > Cloud Monitoring > Anomaly Detection** learns the metric patterns collected by Cloud Monitoring and automatically detects abnormalities that differ from normal behavior.

Unlike regular notifications where you must set thresholds manually, anomaly detection automatically calculates a Score and a Score Threshold at each point in time based on historical metric patterns. Both the Score and the Score Threshold are values in the range from 0 to 100, and when the Score exceeds the Score Threshold, the state is determined to be anomalous.

Use anomaly detection in the following order:

1. Create an anomaly detection item by selecting the metrics and resources to monitor for anomalies.
2. Check the Score and Score Threshold in the widget chart to identify the periods when anomalies occur.
3. Set up anomaly detection notifications to receive alerts when an anomaly occurs.

!!! tip "Note"
    Anomaly detection items are evaluated at 1-minute intervals.

<a id="create-anomaly-detection"></a>
### Create Anomaly Detection { #create-anomaly-detection }

Click **Create Anomaly Detection** to go to the anomaly detection creation screen. You can create an anomaly detection by selecting a service and targets.

- **Service**: Only NHN Cloud services that support anomaly detection are displayed, and only a single selection is allowed.
- **Target**: Configure the following items in order:
  - **Type**: Select the metric type for the service.
  - **Metric Item**: Metric items belonging to the selected type are displayed, and you can select multiple items. The number of selected resources is shown for each metric item.
  - **Resource**: Resources belonging to the selected type/metric item among the resources created in NHN Cloud are displayed, and you can select multiple resources.

One anomaly detection item is created for each combination of the selected metric item and resource, and the anomaly detection name is automatically generated based on the selected metric item and resource.

You cannot create additional items using a combination that has already been created. In such cases, the combination is displayed as **Already Created**.

You can preview the name, metric, and resource of the anomaly detection items to be created in a table using **Creation Item Preview**.
When **Create** is complete, the items shown in the preview are each created as individual anomaly detection items. At that point, you can choose whether to navigate immediately to the notification settings screen for those items.

!!! danger "Caution"
    Creation is processed as either a complete success or a complete failure.
    If even one of the selected items cannot be created, none of the items are created.

Immediately after creation, the anomaly detection status is **Active - Waiting**. Once the training and inference for anomaly detection are complete, the status changes to **Active - Normal**. Until the status changes to Active - Normal, the Score and Score threshold may not be displayed in the chart.
For more information, see the anomaly detection statuses below.

<a id="anomaly-detection-list"></a>
### Anomaly Detection List { #anomaly-detection-list }

The Anomaly Detection screen consists of a list area on the left and a dashboard area on the right. Each anomaly detection item in the list is displayed as a separate widget on the right dashboard.

For each item in the list, you can view the anomaly detection name, service, creation date and time, and status information. The check box for each item is used when processing multiple items at once, such as for deletion.

- Filters, sorting, and search are applied simultaneously to both the left list and the right dashboard area.
- **Filter**: You can filter items displayed in the list and dashboard by using the service and target filters. Filters are configured based on the anomaly detection items that have been created. For example, if there are only items for the Instance service, only Instance is displayed in the service filter.
- **Sort**: You can sort items in descending order by latest or oldest.
- **Search**: You can search by anomaly detection name.


<a id="anomaly-detection-dashboard"></a>
### Anomaly Detection Dashboard { #anomaly-detection-dashboard }

All anomaly detection items that have been created are automatically configured as individual widgets on the anomaly detection dashboard.

- If you select **View active (normal) status only**, only widgets with **Active-Normal** status are displayed.
- In **Download Widget Data**, you can download the widget data displayed on the dashboard as a .csv or .xlsx file.

!!! tip "Note"
    You can add anomaly detection widgets not only to the anomaly detection dashboard, but also to dashboards that you configured yourself on the Dashboard tab.

<a id="anomaly-detection-dashboard-anomaly-detection-widget-chart"></a>
#### Anomaly Detection Widget Chart

The widget chart displays the following elements together.

- **Metric value**: The actual collected value of the metric selected as the anomaly detection target. Displayed based on the left Y axis.
- **Score**: A value from 0 to 100 that indicates how much the current data deviates from historical patterns. A value closer to 100 indicates greater Abnormalities from the usual pattern. Displayed based on the right Y axis.
- **Score threshold**: If the Score exceeds the threshold, the data is determined to be anomalous. Displayed based on the same right Y axis as the Score.

The interval where the Score exceeds the Score threshold is the interval that is determined to be in an anomalous state.

<a id="anomaly-detection-dashboard-delete-anomaly-detection"></a>
#### Delete Anomaly Detection

You can delete a selected item from the anomaly detection list.

- If you create a new item with the same metric item and resource combination as the deleted item, it is automatically re-linked to the widgets and notifications that were previously linked to the deleted item (however, the data collection process may start again).

!!! danger "Caution"
    Deleting an anomaly detection item does not automatically delete the widgets or notifications that use that item.
    Widgets that use the deleted item will no longer display anomaly detection data, and notifications will no longer occur, so you must manually clean them up if they are no longer needed.

<a id="anomaly-detection-dashboard-set-up-anomaly-detection-activation"></a>
#### Anomaly detection activation settings

You can change the activation status of a selected item in the anomaly detection list.

- **Enable**: When you create an anomaly detection, it is automatically set to enabled by default. If you switch from disabled to enabled, data collection may resume.
- **Disable**: Anomaly detection for the selected item stops immediately. Anomaly detection data is no longer displayed in widgets created from that anomaly detection, and notifications are no longer generated.

<a id="anomaly-detection-dashboard-set-up-anomaly-detection-notifications"></a>
#### Set Up Anomaly Detection Notifications

You can set up notifications for the item selected in the anomaly detection list.

- You are taken to the notification creation screen with the selected item already configured. Since each notification can only be created with the metric items of a single service, this is only available when you select anomaly detection items from the same service.


<a id="anomaly-detection-status"></a>
### Anomaly detection status { #anomaly-detection-status }

| Status | Description | 
| --- | --- |
| Enabled - Normal | - Anomaly detection is enabled and operating normally. <br> - Anomaly detection data is displayed in the widget and notifications occur.  |
| Enabled - Pending | - Anomaly detection is enabled and data collection is in progress. <br> - Collecting the data required for anomaly detection training and inference may take up to about 6 hours. Anomaly detection data is displayed and notifications occur once data collection is complete. | 
| Enabled - Insufficient Data | - Anomaly detection is not operating due to insufficient collected metric data for the anomaly detection target. <br> - This can occur due to service failures or resource deletion. Check the resource status in each service console. <br>(If the resource has been deleted, delete the corresponding anomaly detection configuration. If this status persists despite no issues, contact customer support.) | 
| Enabled - Suspended | - Anomaly detection has been temporarily suspended due to a transient issue. <br> - The system recovers automatically, and an additional data collection process for analysis may proceed after recovery is complete. <br> (If this status persists for an extended period, contact the customer support center.) |
| Disabled |  - Anomaly detection is disabled and not operating. <br> - You can reactivate anomaly detection by enabling the setting. <br>(Note that when enabled, additional time is required to collect data, and anomaly detection data will be displayed and notifications will occur only after data collection is complete.) | 

!!! tip "Note"
    For all statuses other than Enabled - Normal, no anomaly detection data is generated, and therefore no notifications occur.



<a id="use-anomaly-detection"></a>
### Use Anomaly Detection { #use-anomaly-detection }

<a id="use-anomaly-detection-add-anomaly-detection-widget"></a>
#### Add an anomaly detection widget

You can freely add an anomaly detection widget to any dashboard that you have created.

- On the Add Widget screen, select **Anomaly Detection** for **Target Type**.
- **Graph Type** is fixed to `Anomaly Detection`.
- When you select a service, a list of anomaly detections created for that service is displayed. If the anomaly detection item you want is not in the list, you must create it first on the Anomaly Detection tab.
- One Metric Setting Block is added for each anomaly detection item that you select.
- The Query Setting Block automatically places three legends: the metric value, Score, and Score threshold. Widgets created with anomaly detection always display these three pieces of data together (however, they may not be displayed depending on the status). The legend name, unit, and Y-axis position of Score and Score threshold are fixed values.
- For metrics that support aggregation, you can use the aggregation settings, and the configured aggregation applies to the metric value, Score, and Score threshold.

!!! danger "Caution"
    If the anomaly detection item used in a widget is deleted, you can still view and save the widget, but you cannot change the query settings of the deleted item.

##### Specify threshold manually

Anomaly detection determines the threshold for each data point on its own, so the reference value varies depending on the point in time. To use a fixed reference, select **Specify Threshold Manually** and enter a value.

- The threshold value must be a number between 0 and 100.
- When you specify a threshold manually, anomalies are determined based on the value that you entered, regardless of the data point.
- If you deselect this option, the chart displays data according to the threshold determined by anomaly detection.

<a id="use-anomaly-detection-anomaly-detection-notifications"></a>
#### Anomaly detection notifications

To receive notifications when an anomaly is detected, create an anomaly detection notification. You can create anomaly detection notifications on the **Notification Management** tab > **Create Notification** screen, just like regular metric notifications.

##### Set threshold

Anomaly detection automatically determines the threshold for each data point, so the reference value varies by time. To use a fixed reference, select **Specify Directly** for each condition and enter a value.

- Only numbers between 0 and 100 (inclusive) can be entered for the threshold.
- If you select Specify Directly, anomalies are evaluated against the value you entered, regardless of data points, and a notification is fired.
- If deselected, a notification is fired when the anomaly detection determines that the threshold-exceeded state has persisted for 5 minutes.

##### View anomaly detection notifications

- Anomaly detection notifications can be viewed on the Notification Settings tab and the Notification History tab, just like regular metric notifications. Anomaly detection notifications are displayed with a separate badge to distinguish them.
- In the Notification History, you can use the **Target Type** filter to view only anomaly detection notifications.

!!! danger "Caution"
    Notifications are only fired when the anomaly detection item is in an **Active-Normal** state. Notification conditions are not evaluated when the status is collecting data, disabled, insufficient data, or suspended. You can check the status of items on the **Anomaly Detection** screen.
    If an anomaly detection item used in a notification is deleted, you can still view and save the notification, but you cannot change the notification conditions for the deleted item.


<a id="use-anomaly-detection-notes"></a>
#### Notes

- Immediately after creating an item, the Score and Score Threshold may not be displayed until the training and inference for anomaly detection are complete.
- If the source metric used by anomaly detection is not collected for 30 consecutive minutes, the status changes to a data-insufficient state, and the Score and Score Threshold are no longer generated. When metric collection resumes, the status is restored to "Active - Waiting" or "Active - Normal".

<a id="example-screen"></a>
## Example Screen { #example-screen }

![Dashboard example](https://static.toastoven.net/prod_cloud_monitoring/Overview.png)
