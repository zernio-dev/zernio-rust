# EstimateAdReachRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio social account ID on the target ad platform (the estimate runs against its platform). | 
**ad_account_id** | **String** | Required. The platform ad-account ID the reach call runs against (Meta act_..., LinkedIn numeric sponsoredAccount ID, Pinterest ad-account ID, X account ID) - every backing reach API is scoped to one ad account. Get it from GET /v1/ads/accounts. | 
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> | The targeting spec to estimate. Same shape used by POST /v1/ads/create. | 
**optimization_goal** | Option<**String**> | Optional. The optimization goal the estimate should assume (platform's own vocabulary, e.g. Meta `REACH`, `LINK_CLICKS`, `OFFSITE_CONVERSIONS`). Some platforms vary the estimate by goal; omit to use the platform default.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


