# ListInboxMentions200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Mention document ID | [optional]
**platform** | Option<**Platform**> |  (enum: linkedin, instagram) | [optional]
**r#type** | Option<**Type**> | Instagram only: `caption` when the account was tagged in a media caption, `comment` when it was tagged in a comment. Null for LinkedIn. (enum: caption, comment, ) | [optional]
**media_id** | Option<**String**> | Instagram only: ID of the media the account was mentioned in (or under). Null for LinkedIn. | [optional]
**comment_id** | Option<**String**> | Instagram only: ID of the comment that mentioned the account. Null for caption mentions and LinkedIn. | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**content** | Option<**String**> | Text that mentioned you: the post text on LinkedIn, the caption or comment text on Instagram. Empty until it has been read. | [optional]
**permalink** | Option<**String**> | URL to the source post on LinkedIn. Null on Instagram. | [optional]
**author_urn** | Option<**String**> | LinkedIn URN of the person who mentioned you, or the Instagram-scoped ID of the commenter on an Instagram comment mention. | [optional]
**author_name** | Option<**String**> | Display name of the author, resolved from authorUrn. Null when LinkedIn does not allow resolving the profile. | [optional]
**author_username** | Option<**String**> | LinkedIn vanity name of the author (the slug in their profile URL), or the Instagram username of the commenter or media owner. | [optional]
**author_picture** | Option<**String**> | Profile picture URL of the author. LinkedIn CDN URLs expire after some time, so fetch promptly rather than storing long-term. | [optional]
**organizational_entity** | Option<**String**> | URN of the LinkedIn organization that was mentioned, or the Instagram user ID of the mentioned account. | [optional]
**published_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


