# Graphing a Metric<a name="graph_a_metric"></a>

You can select metrics and create graphs of the data using the CloudWatch console\.

CloudWatch supports the following statistics on metrics: `Average`, `Minimum`, `Maximum`, `Sum`, and `SampleCount`\. For more information, see [Statistics](cloudwatch_concepts.md#Statistic)\.

You can view your data at different granularities\. For example, you can choose a detailed view \(for example, 1 minute\), which can be useful when troubleshooting\. You can choose a less detailed view \(for example, 1 hour\), which can be useful when viewing a broader time range \(for example, 3 days\) so that you can see trends over time\. For more information, see [Periods](cloudwatch_concepts.md#CloudWatchPeriods)\.

## Creating a Graph<a name="create-metric-graph"></a>

**To graph a metric**

1. Open the CloudWatch console at [https://console\.aws\.amazon\.com/cloudwatch/](https://console.aws.amazon.com/cloudwatch/)\.

1. In the navigation pane, choose **Metrics**\.

1. On the **All metrics** tab, enter a search term in the search field, such as a metric name or resource name, and press Enter\.

   For example, if you search for the `CPUUtilization` metric, you see the namespaces and dimensions with this metric\.

1. Select one of the results for your search to view the metrics\.

1. To graph one or more metrics, select the check box next to each metric\. To select all metrics, select the check box in the heading row of the table\.

1. \(Optional\) To add a band that shows expected values for the metric, choose the anomaly detection icon under **Actions** next to the metric\.   
![\[The metrics console, with the anomaly detection icon circled.\]](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/images/Anomaly_Detection_Icon.PNG)

   CloudWatch uses up to two weeks of the metric's recent historical data to calculate a model for expected values, then displays this range of expected values as a band on the graph\. CloudWatch adds a new row under the metric to display the anomaly detection band math expression, labeled **ANOMALY\_DETECTION\_BAND**\. It may take 15 minutes before the model can be visualized on a graph\.

   By default, CloudWatch creates the upper and lower bounds of the band of expected values with a default value of two standard deviations\. To change this number, change the value at the end of the formula under **Details** for the band\.

   1. \(Optional\) You can also choose **Edit model** to change how the anomaly detection model is calculated\. You can exclude past time periods from being used in the training for calculating the model, and specify the time zone to use for the model to accurately model fluctuations that depend on the time of day\.

   For more information, see [CloudWatch Anomaly Detection](CloudWatch_Anomaly_Detection.md)\.

   To hide the model from the graph, uncheck the line with the ` ANOMALY_DETECTION_BAND` function or choose the `X` icon\. To delete the model entirely, choose **Edit model** and then choose **Delete model**\.

1. \(Optional\) As you choose metrics to graph, you can specify a dynamic label to appear on the graph legend for each metric\. Dynamic labels display a statistic about the metric and automatically update when the dashboard or graph is refreshed\. To add a dynamic label, choose **Graphed metrics** and then **Dynamic labels**\.

   By default, the dynamic values you add to the label appear at the beginning of the label\. You can then click the **Label** value for the metric to edit the label\. For more information, see [Using Dynamic Labels](graph-dynamic-labels.md)\.

1. To view more information about the metric being graphed, hover over the legend\.

1. Horizontal annotations can help graph users quickly see when a metric has spiked to a certain level, or whether the metric is within a predefined range\. To add a horizontal annotation, choose **Graph options** and then **Add horizontal annotation**:

   1. For **Label**, enter a label for the annotation\.

   1. For **Value**, enter the metric value where the horizontal annotation appears\.

   1. For **Fill**, specify whether to use fill shading with this annotation\. For example, choose `Above` or `Below` for the corresponding area to be filled\. If you specify `Between`, another `Value` field appears, and the area of the graph between the two values is filled\.

   1. For **Axis**, specify whether the numbers in `Value` refer to the metric associated with the left Y\-axis or the right Y\-axis, if the graph includes multiple metrics\.

      You can change the fill color of an annotation by choosing the color square in the left column of the annotation\. 

   Repeat these steps to add multiple horizontal annotations to the same graph\.

   To hide an annotation, clear the check box in the left column for that annotation\.

   To delete an annotation, choose **x** in the **Actions** column\.

1. To get a URL for your graph, choose **Actions**, **Share**\. Copy the URL and save it or share it\.

1. To add your graph to a dashboard, choose **Actions**, **Add to dashboard**\.

## Updating a Graph<a name="update-metric-graph"></a>

**To update your graph**

1. To change the name of the graph, choose the pencil icon\.

1. To change the time range, select one of the predefined values or choose **custom**\. For more information, see [Modifying the Time Range or Time Zone Format for a Graph](modify_graph_date_time.md)\.

1. To change the statistic, choose the **Graphed metrics** tab\. Choose the column heading or an individual value and then choose one of the statistics or predefined percentiles, or specify a custom percentile \(for example, **p95\.45**\)\.

1. To change the period, choose the **Graphed metrics** tab\. Choose the column heading or an individual value and then choose a different value\.

1. To add a horizontal annotation, choose **Graph options** and then **Add horizontal annotation**:

   1. For **Label**, enter a label for the annotation\.

   1. For **Value**, enter the metric value where the horizontal annotation appears\.

   1. For **Fill**, specify whether to use fill shading with this annotation\. For example, choose `Above` or `Below` for the corresponding area to be filled\. If you specify `Between`, another `Value` field appears, and the area of the graph between the two values is filled\.

   1. For **Axis**, specify whether the numbers in `Value` refer to the metric associated with the left y\-axis or the right y\-axis, if the graph includes multiple metrics\.

      You can change the fill color of an annotation by choosing the color square in the left column of the annotation\. 

   Repeat these steps to add multiple horizontal annotations to the same graph\.

   To hide an annotation, clear the check box in the left column for that annotation\.

   To delete an annotation, choose **x** in the **Actions** column\.

1. To change the refresh interval, choose **Refresh options** and then select **Auto refresh** or choose **1 Minute**, **2 Minutes**, **5 Minutes**, or **15 Minutes**\.

## Duplicating a Metric<a name="duplicate-metric-graph"></a>

**To duplicate a metric**

1. Choose the **Graphed metrics** tab\.

1. For **Actions**, choose the **Duplicate** icon\.  
![\[Duplicate a metric\]](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/images/metric_graph_duplicate.png)

1. Update the duplicate metric as needed\.