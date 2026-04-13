# WebhookPayloadMessageEdited

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**event** | **Event** |  (enum: message.edited) | 
**message** | [**models::InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**edit_history** | [**Vec<models::WebhookPayloadMessageEditedEditHistoryInner>**](WebhookPayloadMessageEditedEditHistoryInner.md) | Prior versions of the message, oldest first. | 
**edit_count** | **i32** | Total number of edits applied to this message. | 
**edited_at** | **String** | When the most recent edit happened. | 
**conversation** | [**models::InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**account** | [**models::InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**timestamp** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


