# WebhookPayloadAdStatusChangedAdObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**level** | **Level** | Hierarchy level the status applies to. Mirrors Meta's `level`. Creative-level events are not forwarded. (enum: CAMPAIGN, AD_SET, AD) | 
**platform_id** | **String** | Platform-native ID of the campaign / ad set / ad. For Meta this is the bare numeric ID (e.g. `120244894077860689`).  | 
**platform_ad_account_id** | **String** | Platform-native ad-account ID. For Meta this uses the `act_<id>` shape.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


