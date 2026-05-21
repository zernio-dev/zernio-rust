# WebhookPayloadMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID | 
**event** | **Event** |  (enum: message.received) | 
**message** | [**models::WebhookPayloadMessageMessage**](WebhookPayloadMessageMessage.md) |  | 
**conversation** | [**models::WebhookPayloadReactionConversation**](WebhookPayloadReactionConversation.md) |  | 
**account** | [**models::WebhookPayloadReactionAccount**](WebhookPayloadReactionAccount.md) |  | 
**metadata** | Option<[**models::WebhookPayloadMessageMetadata**](WebhookPayloadMessageMetadata.md)> |  | [optional]
**timestamp** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


