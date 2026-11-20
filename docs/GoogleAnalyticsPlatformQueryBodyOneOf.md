# GoogleAnalyticsPlatformQueryBodyOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**report_type** | **ReportType** | A GA4 report over date ranges, paged with a cursor. (enum: standard) | 
**account_id** | **String** | The Zernio id of the connected Google Analytics property. | 
**dimensions** | Option<**Vec<String>**> | GA4 dimension names, up to 9. | [optional]
**metrics** | **Vec<String>** | GA4 metric names, 1 to 10. | 
**dimension_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A GA4 FilterExpression on dimensions, sent to Google unchanged. | [optional]
**metric_filter** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A GA4 FilterExpression on metrics, sent to Google unchanged. | [optional]
**order_bys** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | GA4 OrderBy objects, up to 10. | [optional]
**limit** | Option<**i32**> | Rows per page, up to 10,000. Defaults to 10,000. | [optional][default to 10000]
**date_ranges** | Option<[**Vec<models::GoogleAnalyticsPlatformQueryBodyOneOfDateRangesInner>**](GoogleAnalyticsPlatformQueryBodyOneOfDateRangesInner.md)> | Up to 4 GA4 date ranges. Defaults to the 28 days ending yesterday. | [optional]
**keep_empty_rows** | Option<**bool**> | Keep rows whose metrics are all 0. | [optional]
**currency_code** | Option<**String**> | ISO 4217 code for money metrics. | [optional]
**cursor** | Option<**String**> | The pagination.nextCursor of the previous page, unchanged. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


