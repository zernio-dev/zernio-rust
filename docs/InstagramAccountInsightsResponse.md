# InstagramAccountInsightsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> | The Zernio SocialAccount ID | [optional]
**platform** | Option<**Platform**> | Platform that served this response. (enum: facebook, instagram, youtube, linkedin, tiktok) | [optional]
**date_range** | Option<[**models::InstagramAccountInsightsResponseDateRange**](InstagramAccountInsightsResponseDateRange.md)> |  | [optional]
**metric_type** | Option<**MetricType**> |  (enum: time_series, total_value) | [optional]
**breakdown** | Option<**String**> | Breakdown dimension used (only present when breakdown was requested) | [optional]
**metrics** | Option<[**std::collections::HashMap<String, models::InstagramAccountInsightsResponseMetricsValue>**](InstagramAccountInsightsResponseMetricsValue.md)> | Object keyed by metric name. For time_series: each metric has \"total\" (number) and \"values\" (array of {date, value}). For total_value: each metric has \"total\" (number) and optionally \"breakdowns\" (array of {dimension, value}).  Monetary metrics additionally carry \"unit\" and \"currency\". Zernio never rescales money: \"total\" and every \"values[].value\" are the platform's raw numbers in the stated unit. Monetary metrics also keep \"values\" on metricType=total_value, because their \"total\" is the sum of the daily buckets the platform returned over the range: keep the series so you can reconcile that sum against the platform's own reporting before invoicing on it. A metric that could not be served is absent from this object and listed in \"unavailableMetrics\" instead, so an unavailable metric is never reported as a zero.  | [optional]
**unavailable_metrics** | Option<[**Vec<models::InstagramAccountInsightsResponseUnavailableMetricsInner>**](InstagramAccountInsightsResponseUnavailableMetricsInner.md)> | Requested metrics that could not be served. Present only when at least one metric is unavailable, and absent otherwise. Each listed metric is OMITTED from \"metrics\" rather than reported as 0, which is how an unavailable metric is distinguished from a genuine zero. The request itself still succeeds with HTTP 200.  | [optional]
**data_delay** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


