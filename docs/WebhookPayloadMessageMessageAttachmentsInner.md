# WebhookPayloadMessageMessageAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **String** | Attachment type (image, video, file, sticker, audio) | 
**url** | **String** | Where to fetch the attachment. **The contract differs by platform.**  - **WhatsApp**: points at `GET /v1/whatsapp/media/{mediaId}`, an   authenticated Zernio endpoint. You MUST send   `Authorization: Bearer <your API key>`; fetching it without that   header returns `401`. Download and store the bytes when this   webhook arrives: Meta drops inbound media after a limited   retention window, after which the endpoint answers `400`   permanently and the media is unrecoverable. - **Instagram / Facebook / Telegram**: a direct platform CDN link   that needs no authentication and expires on the platform's own   schedule.  | 
**payload** | Option<**serde_json::Value**> | Additional attachment metadata | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


