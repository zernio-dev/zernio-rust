# GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: image, video, audio, file, sticker, share) | [optional]
**original_type** | Option<**String**> | Instagram and Facebook only, and present only when it differs from `type`. Meta's own type before normalization: `ig_reel` and `reel` become `video`, while `ig_post`, `post`, `ig_story` and `story_mention` become `share`. A story mention is `type: \"share\"` with `originalType: \"story_mention\"`; render on this field, since `share` alone is ambiguous. | [optional]
**url** | Option<**String**> | Direct media link. On Instagram and Facebook this is a signed Meta CDN url that EXPIRES: use it now, do not store it. Persist `refreshUrl` instead. | [optional]
**refresh_url** | Option<**String**> | Instagram and Facebook only. Endpoint that resolves this attachment to a working url every time, re-minting it from Meta when the stored one has expired. Safe to store and render indefinitely. | [optional]
**filename** | Option<**String**> |  | [optional]
**preview_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


