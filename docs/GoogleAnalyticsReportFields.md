# GoogleAnalyticsReportFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio account ID of the Google Analytics connection (platform `googleanalytics`). | 
**dimensions** | Option<**Vec<String>**> | GA4 dimension API names, e.g. `date`, `sessionSource`, `pagePath`. List them with GET /v1/analytics/googleanalytics/metadata. | [optional]
**metrics** | **Vec<String>** | GA4 metric API names, e.g. `sessions`, `activeUsers`, `keyEvents`, `totalRevenue`. | 
**dimension_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A Google FilterExpression on dimensions, in Google's own shape. | [optional]
**metric_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A Google FilterExpression on metrics, in Google's own shape. | [optional]
**order_bys** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | Google OrderBy objects, e.g. `{ \"metric\": { \"metricName\": \"sessions\" }, \"desc\": true }`. | [optional]
**limit** | Option<**i32**> | Rows to return. Defaults to Google's default (10000). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


