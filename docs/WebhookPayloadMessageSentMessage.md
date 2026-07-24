# WebhookPayloadMessageSentMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal message ID | 
**conversation_id** | **String** | Internal conversation ID | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, whatsapp) | 
**platform_message_id** | **String** | Platform's message ID | 
**direction** | **Direction** |  (enum: incoming, outgoing) | 
**text** | Option<**String**> | Message text content | 
**attachments** | [**Vec<models::WebhookPayloadMessageSentMessageAttachmentsInner>**](WebhookPayloadMessageSentMessageAttachmentsInner.md) |  | 
**sender** | [**models::WebhookPayloadMessageSentMessageSender**](WebhookPayloadMessageSentMessageSender.md) |  | 
**sent_at** | **String** |  | 
**is_read** | **bool** |  | 
**source** | Option<**Source**> | WhatsApp send origin. whatsapp_business_app when sent from the WhatsApp Business phone app on a Coexistence number; cloud_api when sent through Zernio (dashboard, API, or broadcasts). Absent on non-WhatsApp platforms. This is not the inbox metadata.source lineage field. (enum: whatsapp_business_app, cloud_api) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


