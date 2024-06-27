## Monitoring > Cloud Monitoring > Usage Scenarios
This document describes overall usage scenarios, from configuring dashboard to creating notifications.<br>
To use Cloud Monitoring, follow the steps below.

- Select the service<br>
  Cloud Monitoring is provided by default when you create a project.<br>
  So you can use the service after creating a project without doing anything else.<br>
  To create a project, see the [NHN Cloud Console User Guide](https://docs.gov-nhncloud.com/en/nhncloud/en/console-guide-gov/).
- Set up metric collection<br>
  Set up metric collection for each service.
- Configure the dashboard<br>
  Add widgets to your dashboard to customize it.
- Create notifications<br>
  You can set thresholds to be notified when events occur.

## Enable metric collection
To configure the dashboard, you first set up metric collection by service.

1. Select **Cloud Monitoring > Manage Metrics**.
2. On the Manage Metrics page, check out the service-specific metrics provided by Cloud Monitoring.
3. Click the **Metrics Collection Settings** toggle for the service you want to collect metrics for to enable the service.
4. When "Do you want to start collecting metrics?" appears, click **Confirm**.
5. Once collection starts, you can add widgets using those metrics.

![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/bb42aa0c-f8f8-4ed6-bc58-9b9e4a15cec6)

- Metrics for Instance and GPU Instance are provided by default.
- Only enabled services collect metrics. Please note that the service is enabled.
- Clicking the **Metrics Collection Settings** toggle to disable it will stop collecting that metric and it will not appear in the dashboard.

## Configure the dashboard
You are now ready to configure your dashboard.<br>
Let's create a dashboard and add a widget.


### Create a dashboard
1. **+Create Dashboard**.
![Select the image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/87598547-0d55-498b-8a61-02eca1bdb5db)
2. Enter a **name** and **description** for your dashboard, then click **Confirm**.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/08175aa4-934e-4d09-afcd-03b5552cfae5)
3. Check the created dashboard.


### Add widgets
1. Click **Add Widget**to go to the Add widget page.
![Add an image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/9e20e916-7501-41b2-b24f-6961af8b026d)
2. Enter a **name for the widget**, and select a **graph type** and **service**.
   - In **Manage Metrics**, you can only select services that have collection settings enabled.
3. Select the **resource type** and **metric items** that correspond to the selected service.
   - You'll see boxes to set filters and a legend for each selected metric item.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/5b739451-7084-4928-8d36-13a68ee6f9e7)

4. You can set filters to selectively see only the metrics you want.
   - For example, to monitor specific instances that are only in the Korea (Pangyo) region, you would set it up like this
     - Click **+Add** to add a filter.
     - Set the filter `Region``=``kr1` (Korea (Pangyo)) in the order of label, operator, and condition.
     - Add a filter to select ` Instances` `= {Instance name}`by label, operator, and condition.
     - This will display the specific instance metrics for the KR1 (Korea (Pangyo)) region in the graph.
5. You can set the name of the legend, units, and position of the y-axis as needed.
   - If the metrics have the same units, they will be displayed as one y-axis.
   - In Y-Axis Positioning, Auto will automatically position the y-axis in left, then right order if the units are different for each metric.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/c2d9ca1d-45c0-4d6c-92b6-c36c44748925)

6. Use the **preview** feature to make sure the graph looks the way you want.
7. Once checked, click **Add** to add the widget to your dashboard.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/3e194309-7b0d-427c-bf93-64fb2fc7a00a)


### Edit Dashboard
Check the widgets added to your dashboard and edit them to your liking.

1. Click the toggle in the top-right corner of the dashboard to change from **View Mode**to **Edit Mode**.
2. Drag and drop widgets to change their position or add groups of widgets to organize your dashboard.
   - Click **Add Widget Group** to add a group at the bottom. Drag and drop widgets into the group to place them.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/83543ece-bfd0-434f-bcc6-d117b3f18942)

## Notification Settings
Enable the setting to receive notifications when events occur for more efficient monitoring.

### Create a notification
1. Select **Cloud Monitoring > Manage Notifications > Notifications Settings**.
2. Click **Create Notifications** to go to the creation page.
![Enter an image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/50e2c389-e784-4b9b-84ab-08359da04c1a)

3. In **Basic information**, enter a **name** and **description**for the notification and select a **service**.
4. Select the **resource type** and **metrics** that correspond to the selected service.
   - You'll see a filter for the selected metric and a box to set notification conditions.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/23b67551-d97c-4bf9-8a58-009e89d38fbc)

5. Set up filters to set up notifications on the metrics you want.
6. Enter the **threshold** and **duration**, which are the conditions under which the notifications will occur.
   - For example, if your CPU utilization is above 30% and you want to be notified when this state lasts for more than 3 minutes, you would set it up like this
     - Select the **metric** as **CPU usage**, and set filters as needed.
     - Select `>=`(greater than or equal to) for the **comparison method**.
     - Enter `30`for the **threshold** and `3` for the **duration**.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/30b3c669-d180-433d-9652-9a65a18f17ba)

7. Select a **notification recipient**.
   - You can select the notification recipient group that you created in your project.
   - Create a group to receive project notifications first.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/65e5d9ca-86e1-4d0d-b260-fad9817e4ac5)

You can also quickly set up notifications from the dashboard widget.

1. Click the More icon in the top-right corner of the widget, then click **Create Notifications** from the drop-down menu.
2. You will be taken to the **Create Notifications** page, and the metric-specific filters you selected when creating the widget will still be applied.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/9ef138c3-51ef-4463-ae97-14098331a1e1)

Notifications are now fired when the threshold you set is reached, and you can view the history of the firing in **Manage Notifications > Notifications History**.

## Project Dashboard Visibility Settings
You can view the dashboards generated by the Cloud Monitoring service on the project main screen.

1. Click **Cloud Monitoring > Dashboard > Manage Dashboard**.
2. Click the **Project Dashboard Visibility Settings** toggle for the dashboard you want to show on the project main screen to enable it.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/8e2383b5-99c5-4d7d-ac17-9a406af90869)

You can also view the dashboards you've set up in your project's **custom dashboard** for quick monitoring.
