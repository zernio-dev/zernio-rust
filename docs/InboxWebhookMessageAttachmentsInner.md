# InboxWebhookMessageAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **String** | Attachment type (image, video, file, sticker, audio) | 
**url** | **String** | Where to fetch the attachment. The contract depends on direction and platform: inbound WhatsApp media points at the authenticated `GET /v1/whatsapp/media/{mediaId}` and requires `Authorization: Bearer <your API key>`, while outgoing media carries the URL originally supplied and Instagram / Facebook / Telegram carry direct platform CDN links that need no authentication.  | 
**payload** | Option<**serde_json::Value**> | Additional attachment metadata | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


