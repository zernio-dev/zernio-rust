# WebhookPayloadMessageEdited

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**event** | **Event** |  (enum: message.edited) | 
**message** | [**models::InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**edit_history** | [**Vec<models::InboxMessageEditHistoryEntry>**](InboxMessageEditHistoryEntry.md) | Prior versions of the message, oldest first. | 
**edit_count** | **i32** | Total number of edits applied to this message. | 
**edited_at** | **String** | When the most recent edit happened. | 
**conversation** | [**models::InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**account** | [**models::InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


