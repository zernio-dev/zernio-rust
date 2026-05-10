# XApiPricingTiersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | Option<**String**> | Tier key derived from price (e.g. `x_api_005` for $0.005, `x_api_200` for $0.200). The first three keys map to the legacy `xApiCalls` aggregate; new tiers (e.g. `x_api_200` for the URL tier added April 2026) are surfaced here but not in the legacy shape.  | [optional]
**price_per_call_usd** | Option<**f64**> |  | [optional]
**operation_count** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


