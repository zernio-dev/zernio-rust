# FacebookPostEarningsResponseMetricsValue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | Option<**f64**> | Lifetime earnings in \"unit\", exactly as Meta returned them. Never rescaled. | [optional]
**unit** | Option<**Unit**> | \"micro_amount\": Meta returned an object shape carrying a micro amount, and \"total\" is that integer, unconverted. Zernio does not publish a divisor because Meta does not document one; divide by the scale you have verified against the Page's own Meta Business Suite export. This is always content_monetization_earnings.  \"unspecified\": Meta returned a bare number with no unit metadata, passed through as-is; Meta does not state whether it is major or minor currency units. This is always monetization_approximate_earnings.  (enum: micro_amount, unspecified) | [optional]
**currency** | Option<**String**> | ISO 4217 currency, or null when Meta omitted it. Always null on monetization_approximate_earnings; always present on content_monetization_earnings.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


