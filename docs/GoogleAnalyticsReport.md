# GoogleAnalyticsReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Zernio account ID of the Google Analytics connection. | [optional]
**property_id** | Option<**String**> | Numeric GA4 property ID. | [optional]
**dimension_headers** | Option<[**Vec<models::GoogleAnalyticsReportDimensionHeadersInner>**](GoogleAnalyticsReportDimensionHeadersInner.md)> |  | [optional]
**metric_headers** | Option<[**Vec<models::GoogleAnalyticsReportMetricHeadersInner>**](GoogleAnalyticsReportMetricHeadersInner.md)> |  | [optional]
**rows** | Option<[**Vec<models::GoogleAnalyticsReportRowsInner>**](GoogleAnalyticsReportRowsInner.md)> |  | [optional]
**row_count** | Option<**i32**> | Total rows matching the request, across all pages. | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Google report metadata (currency, time zone, sampling and thresholding flags). | [optional]
**property_quota** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Google quota left on this property after the request (tokens per day and per hour, concurrent requests). Cached responses carry the quota from when they were fetched. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


