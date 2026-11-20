# GoogleAnalyticsPlatformQueryBodyOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**report_type** | **ReportType** | A GA4 realtime report on the last 30 minutes, one page. (enum: realtime) | 
**account_id** | **String** | The Zernio id of the connected Google Analytics property. | 
**dimensions** | Option<**Vec<String>**> | GA4 dimension names, up to 9. | [optional]
**metrics** | **Vec<String>** | GA4 metric names, 1 to 10. | 
**dimension_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A GA4 FilterExpression on dimensions, sent to Google unchanged. | [optional]
**metric_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A GA4 FilterExpression on metrics, sent to Google unchanged. | [optional]
**order_bys** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | GA4 OrderBy objects, up to 10. | [optional]
**limit** | Option<**i32**> | Rows, up to 10,000. | [optional]
**minute_ranges** | Option<[**Vec<models::GoogleAnalyticsPlatformQueryBodyOneOf1MinuteRangesInner>**](GoogleAnalyticsPlatformQueryBodyOneOf1MinuteRangesInner.md)> | Up to 2 GA4 minute ranges. Defaults to the last 30 minutes. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


