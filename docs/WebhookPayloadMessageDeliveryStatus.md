# WebhookPayloadMessageDeliveryStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**event** | **Event** |  (enum: message.delivered, message.read, message.failed) | 
**message** | [**models::WebhookPayloadMessageMessage**](WebhookPayloadMessageMessage.md) |  | 
**status_at** | **String** | When the platform reported this status. | 
**error** | Option<[**models::WebhookPayloadMessageDeliveryStatusError**](WebhookPayloadMessageDeliveryStatusError.md)> |  | [optional]
**conversation** | [**models::WebhookPayloadMessageConversation**](WebhookPayloadMessageConversation.md) |  | 
**account** | [**models::WebhookPayloadMessageAccount**](WebhookPayloadMessageAccount.md) |  | 
**timestamp** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


