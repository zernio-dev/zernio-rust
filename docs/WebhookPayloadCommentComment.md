# WebhookPayloadCommentComment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform comment ID | 
**post_id** | Option<**String**> | Internal post ID (null for posts not published through Zernio) | 
**platform_post_id** | **String** | Platform's post ID | 
**platform** | **Platform** |  (enum: instagram, facebook, threads, youtube, linkedin, bluesky, reddit, tiktok) | 
**text** | **String** | Comment text content | 
**author** | [**models::WebhookPayloadCommentCommentAuthor**](WebhookPayloadCommentCommentAuthor.md) |  | 
**created_at** | **String** |  | 
**is_reply** | **bool** | Whether this is a reply to another comment | 
**parent_comment_id** | Option<**String**> | Parent comment ID if this is a reply | 
**is_live** | Option<**bool**> | Instagram only: true when the comment was made on a live broadcast (the live_comments webhook field). Absent on every other comment. | [optional]
**ad** | Option<[**models::WebhookPayloadCommentCommentAd**](WebhookPayloadCommentCommentAd.md)> |  | [optional]
**attachment** | Option<[**models::CommentAttachment**](CommentAttachment.md)> | Facebook only. Present on graphic-only comments (sticker, GIF, photo) that carry no text: the webhook only includes it when the comment has no text. The REST comments API returns it whenever Facebook returns one, text or not.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


