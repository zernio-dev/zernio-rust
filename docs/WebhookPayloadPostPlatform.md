# WebhookPayloadPostPlatform

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID. | 
**event** | **Event** |  (enum: post.platform.published, post.platform.failed, post.platform.deleted, post.tiktok.url_resolved) | 
**post** | [**models::WebhookPayloadPostPlatformPost**](WebhookPayloadPostPlatformPost.md) |  | 
**platform** | [**models::WebhookPayloadPostPlatformPlatform**](WebhookPayloadPostPlatformPlatform.md) |  | 
**account** | [**models::WebhookPayloadPostPlatformAccount**](WebhookPayloadPostPlatformAccount.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


