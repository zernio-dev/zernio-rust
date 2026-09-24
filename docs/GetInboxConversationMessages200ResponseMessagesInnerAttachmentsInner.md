# GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> | On Instagram and Facebook a shared reel, post or ad reaches Zernio with no type of its own (Meta's `unsupported_type`) and is resolved from the media's Content-Type at ingest into `image`, `video`, `audio` or `file` with `originalType: \"unsupported_type\"`. `unsupported_type` is returned only when the CDN could not be classified in time. (enum: image, video, audio, file, sticker, share, template, unsupported_type) | [optional]
**original_type** | Option<**String**> | Instagram and Facebook only, and present only when it differs from `type`. Meta's own type before normalization: `ig_reel` and `reel` become `video`, while `ig_post`, `post`, `ig_story` and `story_mention` become `share`. A story mention is `type: \"share\"` with `originalType: \"story_mention\"`; render on this field, since `share` alone is ambiguous. `originalType: \"unsupported_type\"` marks a share Meta did not classify, resolved by content type: `refreshUrl` cannot re-mint it (Meta answers `is_unsupported` with no attachments for the message node), so download it when the `message.received` webhook arrives. | [optional]
**mime_type** | Option<**String**> | MIME type of the media when Zernio knows it. On Instagram and Facebook it is set for shares resolved by content type (`originalType: \"unsupported_type\"`). | [optional]
**url** | Option<**String**> | Direct media link. On Instagram and Facebook this is a signed Meta CDN url that EXPIRES: use it now, do not store it. Persist `refreshUrl` instead. | [optional]
**refresh_url** | Option<**String**> | Instagram and Facebook only. Endpoint that resolves this attachment to a working url every time, re-minting it from Meta when the stored one has expired. Safe to store and render indefinitely, except for an attachment with `originalType: \"unsupported_type\"`: Meta cannot re-serve those, so the endpoint answers 404 once the url has expired. | [optional]
**filename** | Option<**String**> |  | [optional]
**preview_url** | Option<**String**> |  | [optional]
**payload** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Template content (title, subtitle, image, buttons) when type is template | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


