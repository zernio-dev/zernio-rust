# InboxWebhookMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal message ID | 
**conversation_id** | **String** | Internal conversation ID | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, whatsapp, sms) | 
**platform_message_id** | **String** | Platform's message ID | 
**direction** | **Direction** |  (enum: incoming, outgoing) | 
**text** | Option<**String**> | Message text content (retained on deleted messages for API consumers; Zernio dashboard UI hides this) | 
**attachments** | [**Vec<models::InboxWebhookMessageAttachmentsInner>**](InboxWebhookMessageAttachmentsInner.md) |  | 
**sender** | [**models::InboxWebhookMessageSender**](InboxWebhookMessageSender.md) |  | 
**sent_at** | **String** | When the message was sent, as reported by the platform and passed through unmodified. Full ISO 8601 date-time: Instagram and Facebook carry millisecond precision, while some platforms (for example WhatsApp and Telegram) report whole seconds. Use this field as the chronological ordering key. If two messages share the same value, fetch the conversation messages with sortOrder=desc for the deterministic order. | 
**is_read** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


