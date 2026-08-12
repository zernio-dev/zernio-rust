# WebhookPayloadMessageSent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID | 
**event** | **Event** |  (enum: message.sent) | 
**message** | [**models::WebhookPayloadMessageSentMessage**](WebhookPayloadMessageSentMessage.md) |  | 
**conversation** | [**models::InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**account** | [**models::InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


