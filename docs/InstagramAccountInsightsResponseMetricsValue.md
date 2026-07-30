# InstagramAccountInsightsResponseMetricsValue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | Option<**f64**> | Sum or aggregate value for the metric | [optional]
**values** | Option<[**Vec<models::InstagramAccountInsightsResponseMetricsValueValuesInner>**](InstagramAccountInsightsResponseMetricsValueValuesInner.md)> | Daily values (for time_series, and always on monetary metrics) | [optional]
**breakdowns** | Option<[**Vec<models::InstagramAccountInsightsResponseMetricsValueBreakdownsInner>**](InstagramAccountInsightsResponseMetricsValueBreakdownsInner.md)> | Breakdown values (only for total_value with breakdown) | [optional]
**unit** | Option<**Unit**> | Present on monetary metrics only. The scale of \"total\" and of every \"values[].value\", exactly as the platform returned them.  \"micro_amount\": the platform returned an object shape carrying a micro amount, and the values are that integer, summed, unconverted. Zernio does not publish a divisor because Meta does not document one; divide by the scale you have verified against the Page's own Meta Business Suite export. On Facebook Page insights this is always content_monetization_earnings.  \"unspecified\": the platform returned a bare number with no unit metadata. It is passed through as-is; the platform does not state whether it is major or minor currency units. On Facebook Page insights this is always monetization_approximate_earnings.  (enum: micro_amount, unspecified) | [optional]
**currency** | Option<**String**> | ISO 4217 currency of a monetary metric, or null when the platform omitted it. Always null on monetization_approximate_earnings, which Meta returns as a bare number with no currency; always present on content_monetization_earnings.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


