# ErrorResponseDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**quota_exhausted** | Option<**bool**> | Google Ads 429 only. True when the upstream Google Ads quota is spent rather than a Zernio limit. | [optional]
**quota_scope** | Option<**QuotaScope**> | Google Ads 429 only, when Google names the scope. DEVELOPER is the shared developer-token budget; ACCOUNT is your ad account. (enum: DEVELOPER, ACCOUNT) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


