# FacebookPostEarningsResponseUnavailableMetricsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | Option<**String**> | The requested metric name. | [optional]
**reason** | Option<**Reason**> | \"not_enrolled\": the account is not enrolled in the program behind this metric. \"permission_missing\": the connected user lacks access to this metric. \"unsupported_metric\": Meta does not accept this metric name on the API version Zernio uses. \"no_data\": Meta returned no bucket for this metric. \"unreadable_value\": Meta returned a value shape Zernio cannot read, so no total is reported. \"mixed_currency\": readable values disagree on currency or unit. \"upstream_error\": any other platform failure.  \"no_data\" is the common case in practice; the others are defensive.  (enum: not_enrolled, permission_missing, unsupported_metric, no_data, unreadable_value, mixed_currency, upstream_error) | [optional]
**message** | Option<**String**> | Platform-provided explanation when available (access tokens redacted), otherwise Zernio copy. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


