# WebhookPayloadMessageMessageAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **String** | Attachment type (image, video, file, sticker, audio, share) | 
**original_type** | Option<**String**> | Instagram and Facebook only, and present only when it differs from `type`. Meta's own attachment type before Zernio normalized it: `ig_reel` and `reel` become `video`, while `ig_post`, `post`, `ig_story` and `story_mention` all become `share`.  Read it before rendering, because `type: \"share\"` alone is ambiguous. In particular a story mention arrives as `type: \"share\"` with `originalType: \"story_mention\"`; treating an unrecognized type as a generic document shows your agent \"document received\" for what is usually a lead.  | [optional]
**url** | **String** | Where to fetch the attachment. **The contract differs by platform.**  - **WhatsApp**: points at `GET /v1/whatsapp/media/{mediaId}`, an   authenticated Zernio endpoint. You MUST send   `Authorization: Bearer <your API key>`; fetching it without that   header returns `401`. Download and store the bytes when this   webhook arrives: Meta drops inbound media after a limited   retention window, after which the endpoint answers `400`   permanently and the media is unrecoverable. - **Instagram / Facebook / Telegram**: a direct platform CDN link   that needs no authentication and expires on the platform's own   schedule.  **Webhook attachments carry no `refreshUrl`.** That field is stamped only when you read a message back over REST (`GET /v1/inbox/conversations/{conversationId}/messages`). On Instagram and Facebook the url above is a signed Meta CDN link that expires, so do not persist it: store the message id and resolve the media through `GET /v1/inbox/conversations/{conversationId}/messages/{messageId}/attachments/{index}?accountId={accountId}`, which re-mints it on demand. Every value that URL needs is already in this payload: `message.conversationId`, `message.platformMessageId`, `account.accountId`, and the attachment's zero-based position in this array.  | 
**payload** | Option<**serde_json::Value**> | Additional attachment metadata | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


