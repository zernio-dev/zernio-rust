# InboxWebhookMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal message ID | 
**conversation_id** | **String** | Internal conversation ID | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, whatsapp) | 
**platform_message_id** | **String** | Platform's message ID | 
**direction** | **Direction** |  (enum: incoming, outgoing) | 
**text** | **String** | Message text content (retained on deleted messages for API consumers; Zernio dashboard UI hides this) | 
**attachments** | [**Vec<models::InboxWebhookMessageAttachmentsInner>**](InboxWebhookMessageAttachmentsInner.md) |  | 
**sender** | [**models::InboxWebhookMessageSender**](InboxWebhookMessageSender.md) |  | 
**sent_at** | **String** |  | 
**is_read** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


