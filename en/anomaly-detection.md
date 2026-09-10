<!-- machine_translated: true -->

<!-- pre-align:aligned sig=efabe69d34b4 -->

## Anomaly Detection

**Monitoring > Cloud Monitoring > Anomaly Detection** learns the metric patterns collected by Cloud Monitoring and automatically detects abnormalities that deviate from normal behavior.

Unlike standard notifications where you define thresholds manually, anomaly detection automatically calculates a **Score** and a **Score threshold** at each point in time based on the historical pattern of the metric. Both the Score and the Score threshold are values in the range of 0 to 100. When the Score exceeds the Score threshold, the state is determined to be anomalous.

Use anomaly detection in the following order:

1. Create anomaly detection items by selecting the metrics and resources to monitor for anomalies.
2. Check the Score and Score threshold in the widget chart to identify anomalous intervals.
3. Configure anomaly detection notifications to receive alerts when an anomaly occurs.

!!! tip "Note"
    Created anomaly detection items are evaluated every minute.

### Create anomaly detection

Click **Create Anomaly Detection** to navigate to the anomaly detection creation screen. You can create items by selecting the service and target for anomaly detection.

- **Service**: Only NHN Cloud services that support anomaly detection are displayed, and only a single selection is allowed.
- **Target**: Configure in the following order:
  - **Type**: Select the metric type for the service.
  - **Metric items**: Metric items belonging to the selected type are displayed, and you can select multiple items. The number of selected resources is displayed alongside each metric item.
  - **Resource**: Resources belonging to the corresponding type/metric item among resources created in NHN Cloud are displayed, and you can select multiple resources.

One anomaly detection item is created for each combination of the selected metric item and resource, and the anomaly detection name is automatically generated based on the selected metric item and resource.

You cannot create additional items using combinations that already exist. Such cases are displayed as **Already created**.

You can preview the names, metrics, and resources of the anomaly detection items to be created in **Creation item preview**.
When **creation** is complete, the items shown in the preview are each created as individual anomaly detection items. At that point, you can choose whether to immediately navigate to the notification settings screen for those items.

!!! danger "Caution"
    Creation is processed as either fully successful or fully failed.
    If even one of the selected items cannot be created, no items are created.

The status immediately after creating an anomaly detection item is **Enabled - Pending**, and it changes to **Enabled - Normal** when learning and inference for anomaly detection are complete. The Score and Score threshold may not be displayed in the chart until the status changes to Enabled - Normal.
For more information, see **Anomaly detection status** below.

### Anomaly detection list

The anomaly detection screen consists of a list area on the left and a dashboard area on the right. Each anomaly detection item in the list is displayed as a single widget in the dashboard on the right.

Each item in the list shows the anomaly detection name, service, creation date and time, and status information. The checkboxes next to items are used when processing multiple items at once, such as for deletion.

- Filters, sorting, and search are applied simultaneously to both the left list and the right dashboard area.
- **Filter**: You can filter the items displayed in the list and dashboard using service and target filters. Filters are configured based on the created anomaly detection items. For example, if there are only items for the Instance service, only Instance is displayed in the service filter.
- **Sort**: You can sort items from newest to oldest or oldest to newest.
- **Search**: You can search by anomaly detection name.


### Anomaly detection dashboard

The anomaly detection dashboard automatically organizes all created anomaly detection items as individual widgets.

- Selecting **View enabled (normal) status only** displays only the widgets for items in the **Enabled - Normal** status.
- In **Download widget data**, you can download the widget data displayed in the dashboard as a .csv or .xlsx file.

!!! tip "Note"
    You can add anomaly detection widgets not only to the anomaly detection dashboard but also to dashboards that you have configured directly in the Dashboard tab.

#### Anomaly detection widget chart

The widget chart displays the following elements together:

- **Metric value**: The actual collected value of the metric selected as the anomaly detection target. Displayed based on the left Y-axis.
- **Score**: A value from 0 to 100 that represents the degree to which the current data deviates from past patterns. The closer to 100, the more it indicates abnormalities that differ from normal patterns. Displayed based on the right Y-axis.
- **Score threshold**: If the Score exceeds the threshold, the state is determined to be anomalous. Displayed based on the same right Y-axis as the Score.

The interval where the Score exceeds the Score threshold is the interval determined to be in an anomalous state.

#### Delete anomaly detection

You can delete selected items from the anomaly detection list.

- If you recreate an item using the same metric item and resource combination as a deleted item, the widgets and notifications that were previously linked to the deleted item are automatically linked again. (However, the data acquisition process may restart.)

!!! danger "Caution"
    Deleting an anomaly detection item does not automatically delete the widgets or notifications that use that item.
    Widgets that use a deleted item will not display anomaly detection data, and notifications will no longer be generated. If they are no longer needed, you must clean them up manually.

#### Configure anomaly detection activation

You can change the activation status of selected items in the anomaly detection list.

- **Enable**: When an anomaly detection item is created, it is automatically enabled by default. If you switch from disabled to enabled, the data acquisition process may restart.
- **Disable**: Anomaly detection for the item stops immediately, anomaly detection data is no longer displayed in widgets created with that anomaly detection item, and notifications are no longer generated.

#### Configure anomaly detection notifications

You can configure notifications for selected items in the anomaly detection list.

- The screen navigates to the notification creation screen with the selected items pre-configured. Since one notification can be created with the service metrics of a single service, this is only possible when anomaly detection items belonging to the same service are selected.


### Anomaly detection status

| Status | Description | 
| --- | --- |
| Enabled - Normal | - Anomaly detection is enabled and operating normally. <br> - Anomaly detection data is displayed in widgets, and notifications are generated. |
| Enabled - Pending | - Anomaly detection is enabled and data acquisition is in progress. <br> - It may take approximately 6 hours to acquire the data required for anomaly detection learning and inference. Anomaly detection data is displayed and notifications are generated from the point when data acquisition is complete. | 
| Enabled - Insufficient data | - Anomaly detection is not operating due to insufficient collected metric data for the anomaly detection target. <br> - This may be caused by a service failure or resource deletion. Check the resource status in each service console. <br>(If the resource has been deleted, delete the corresponding anomaly detection configuration. If this status persists without any apparent issue, contact customer support.) | 
| Enabled - Temporarily suspended | - Anomaly detection has been temporarily paused due to a temporary issue. <br> - The system automatically recovers, and after recovery, an additional data acquisition process may take place to support analysis. <br>(If this status persists for a long time, contact customer support.) |
| Disabled | - Anomaly detection is disabled and not operating. <br> - You can restart anomaly detection by enabling it. <br>(However, additional time is required to acquire data upon enabling, and anomaly detection data is displayed and notifications are generated after data acquisition is complete.) | 

!!! tip "Note"
    All statuses except Enabled - Normal do not generate anomaly detection data, and therefore notifications are not generated either.



## Using anomaly detection

### Add anomaly detection widget

You can freely add anomaly detection widgets to dashboards that you have created directly.

- In the Add Widget screen, select **Anomaly Detection** for **Target type**.
- **Graph type** is fixed to `Anomaly Detection`.
- When you select a service, the list of anomaly detection items created for that service is displayed. If the anomaly detection item you want is not in the list, you must create it first in the Anomaly Detection tab.
- One Metric Setting Block is added for each selected anomaly detection item.
- The Query Setting Block automatically includes three legends: metric value, Score, and Score threshold. Widgets created with anomaly detection always display these three data types together. (However, they may not be displayed depending on the status.) The legend names, units, and Y-axis positions of the Score and Score threshold are fixed values.
- For metrics that support aggregation, you can use aggregation settings, and the configured aggregation is applied to the metric value, Score, and Score threshold.

!!! danger "Caution"
    If an anomaly detection item in use by a widget is deleted, the widget can still be viewed and saved, but the query settings for the deleted item cannot be changed.

#### Specify threshold manually

Since anomaly detection determines the threshold independently for each data point, the baseline value varies by point in time. To use a fixed baseline, select **Specify threshold manually** and enter a value.

- Only numbers between 0 and 100 (inclusive) can be entered for the threshold.
- When specified manually, anomalies are determined based on the entered value regardless of the data point.
- If deselected, the chart displays the threshold as determined by anomaly detection.

### Anomaly detection notifications

To receive notifications when an anomaly is detected, create anomaly detection notifications. Anomaly detection notifications can also be created in the same way as standard metric notifications, in the Notification Management tab > Create Notification screen.

#### Threshold settings

Since anomaly detection determines the threshold independently for each data point, the baseline value varies by point in time. To use a fixed baseline, select **Specify** for each condition and enter a value.

- Only numbers between 0 and 100 (inclusive) can be entered for the threshold.
- When specified manually, anomalies are determined based on the entered value regardless of the data point, and notifications are generated.
- If deselected, a notification is generated when the state of exceeding the threshold determined by anomaly detection continues for 5 minutes.

#### Check anomaly detection notifications

- Anomaly detection notifications can be checked in the same way as standard metric notifications, in the Notification Settings tab and the Notification History tab. Anomaly detection notifications are displayed with a separate badge to distinguish them.
- In the Notification History, you can filter to view only anomaly detection notifications using the **Target type** filter.

!!! danger "Caution"
    Notifications are generated only when the anomaly detection item is in the **Enabled - Normal** status. Notification conditions are not evaluated when data acquisition is in progress, or when the status is disabled, insufficient data, or temporarily suspended. You can check the item's status in the **Anomaly Detection** screen.
    If an anomaly detection item in use by a notification is deleted, the notification can still be viewed and saved, but the notification conditions for the deleted item cannot be changed.


### Notes

- Immediately after creating an item, the Score and Score threshold may not be displayed until learning and inference for anomaly detection are complete.
- If the source metric used by anomaly detection is not collected for 30 consecutive minutes, the status changes to insufficient data, and the Score and Score threshold are no longer generated. When metric collection resumes, the status recovers to 'Enabled - Pending' or 'Enabled - Normal'.