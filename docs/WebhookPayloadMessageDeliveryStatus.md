# WebhookPayloadMessageDeliveryStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**event** | **Event** |  (enum: message.delivered, message.read, message.failed) | 
**message** | [**models::InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**status_at** | **String** | When the platform reported this status. | 
**error** | Option<[**models::WebhookPayloadMessageDeliveryStatusError**](WebhookPayloadMessageDeliveryStatusError.md)> |  | [optional]
**conversation** | [**models::InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**account** | [**models::InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


