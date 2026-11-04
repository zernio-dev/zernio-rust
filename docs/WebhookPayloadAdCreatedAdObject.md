# WebhookPayloadAdCreatedAdObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**level** | **Level** | Always `AD`. (enum: AD) | 
**platform_id** | **String** | Platform-native ad ID. | 
**platform_ad_account_id** | **String** | Platform-native ad account ID. | 
**ad_id** | **String** | Zernio ad ID, usable with GET /v1/ads/{adId}. | 
**name** | **String** |  | 
**campaign** | [**models::WebhookPayloadAdCreatedAdObjectCampaign**](WebhookPayloadAdCreatedAdObjectCampaign.md) |  | 
**ad_set** | [**models::WebhookPayloadAdCreatedAdObjectAdSet**](WebhookPayloadAdCreatedAdObjectAdSet.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


