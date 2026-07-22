# WebhookPayloadMessageSentMessageAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **String** | Attachment type (image, video, file, sticker, audio) | 
**url** | **String** | Where to fetch the attachment. For outgoing messages this is the media URL as sent, so for WhatsApp it is the URL you supplied when publishing (WhatsApp sends media by link), not a Zernio endpoint, and it needs no Zernio credentials. Contrast the inbound direction: `message.received` attachment URLs on WhatsApp point at the authenticated `GET /v1/whatsapp/media/{mediaId}`.  | 
**payload** | Option<**serde_json::Value**> | Additional attachment metadata | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


