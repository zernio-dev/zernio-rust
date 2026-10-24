# ListInboxMentions200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Mention document ID | [optional]
**platform** | Option<**Platform**> |  (enum: linkedin, instagram, facebook) | [optional]
**r#type** | Option<**Type**> | Instagram and Facebook: `caption` when the Instagram account was tagged in a media caption, `post` when the Facebook Page was tagged in a post, `comment` when either was tagged in a comment. Null for LinkedIn. (enum: caption, post, comment, ) | [optional]
**media_id** | Option<**String**> | Instagram only: ID of the media the account was mentioned in (or under). Null for LinkedIn and Facebook. | [optional]
**post_id** | Option<**String**> | Facebook only: ID of the post the Page was mentioned in (or under). Null for LinkedIn and Instagram. | [optional]
**comment_id** | Option<**String**> | Instagram and Facebook: ID of the comment that mentioned the account. Null for caption and post mentions and for LinkedIn. | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**content** | Option<**String**> | Text that mentioned you: the post text on LinkedIn, the caption or comment text on Instagram, the post or comment text on Facebook. Empty until it has been read. | [optional]
**permalink** | Option<**String**> | URL to the source post on LinkedIn. Null on Instagram and Facebook. | [optional]
**author_urn** | Option<**String**> | LinkedIn URN of the person who mentioned you, the Instagram-scoped ID of the commenter on an Instagram comment mention, or the ID of the Facebook user or Page that mentioned your Page when Meta sends it. | [optional]
**author_name** | Option<**String**> | Display name of the author, resolved from authorUrn on LinkedIn (null when LinkedIn does not allow resolving the profile) and taken from the webhook on Facebook. | [optional]
**author_username** | Option<**String**> | LinkedIn vanity name of the author (the slug in their profile URL), or the Instagram username of the commenter or media owner. | [optional]
**author_picture** | Option<**String**> | Profile picture URL of the author. LinkedIn CDN URLs expire after some time, so fetch promptly rather than storing long-term. | [optional]
**organizational_entity** | Option<**String**> | URN of the LinkedIn organization that was mentioned, the Instagram user ID of the mentioned account, or the ID of the mentioned Facebook Page. | [optional]
**published_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


