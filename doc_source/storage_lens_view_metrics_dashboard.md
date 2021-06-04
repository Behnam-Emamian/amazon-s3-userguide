# Viewing S3 Storage Lens metrics on the dashboards<a name="storage_lens_view_metrics_dashboard"></a>

S3 Storage Lens provides you with a dashboard containing usage metrics at no additional cost\. If you want to receive advanced metrics and recommendations, including usage and activity metrics, prefix aggregations, and contextual recommendations in the dashboard, you must select it from the dashboard configuration page on the Amazon S3 console\.

The dashboard provides an interactive visualization for your storage usage and activity metrics\. You can view organization\-wide trends, or see more granular trends by AWS account, AWS Region, storage class, S3 bucket, or prefix\. 

If your account is a member of AWS Organizations, you can also see your storage usage and activity for your entire organization across member accounts\. This information is available to you provided that S3 Storage Lens has been given trusted access to your organization, and you are an authorized management or delegated administrator account\.

Use the interactive dashboard to explore your storage usage and activity trends and insights, and get contextual recommendations for best practices to optimize your storage\. For more information, see [Understanding Amazon S3 Storage Lens](storage_lens_basics_metrics_recommendations.md)\.

Amazon S3 preconfigures the S3 Storage Lens *default dashboard* to help you visualize summarized insights and trends of your entire account’s aggregated storage usage and activity metrics\(optional upgrade\)\. You can't modify the default dashboard configuration scope, but the metrics selection can be upgraded from *free metrics* to the paid *advanced metrics and recommendations*\. You can configure the optional metrics export, or even disable the dashboard\. However, the default dashboard cannot be deleted\.

In addition to the default dashboard that Amazon S3 creates, you can also create custom dashboards scoped to your own organization’s accounts, Regions, buckets, and prefixes\(account\-level only\)\. These custom dashboards can be edited, deleted, and disabled\. Summary information from the **default dashboard** appears in the account snapshot section in the S3 console home \(bucket lists\) page\.

**Note**  
The Amazon S3 Storage Lens dashboard is only available from the Amazon S3 console\. For more information, see [Viewing an Amazon S3 Storage Lens dashboard](storage_lens_console_viewing.md)\.