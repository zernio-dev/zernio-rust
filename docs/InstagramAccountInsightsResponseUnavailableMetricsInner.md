# InstagramAccountInsightsResponseUnavailableMetricsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | Option<**String**> | The requested metric name. | [optional]
**reason** | Option<**Reason**> | \"not_enrolled\": the account is not enrolled in the program behind this metric. \"permission_missing\": the connected user lacks access to this metric. \"unsupported_metric\": the platform does not accept this metric name on the API version Zernio uses. \"no_data\": the platform returned no bucket for this metric over the requested range. \"unreadable_value\": the platform returned a value shape Zernio cannot read, so no total is reported. \"mixed_currency\": readable values disagree on currency or unit within the range. \"upstream_error\": any other platform failure.  \"no_data\" is the common case in practice. The others are defensive: \"not_enrolled\" and \"unsupported_metric\" in particular have not been observed on live Facebook traffic, since a non-enrolled Page returns zeros rather than an error and metric names are validated before any platform call.  (enum: not_enrolled, permission_missing, unsupported_metric, no_data, unreadable_value, mixed_currency, upstream_error) | [optional]
**message** | Option<**String**> | Platform-provided explanation when available (access tokens redacted), otherwise Zernio copy. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


