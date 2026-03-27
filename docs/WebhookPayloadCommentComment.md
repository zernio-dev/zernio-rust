# WebhookPayloadCommentComment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform comment ID | 
**post_id** | **String** | Internal post ID | 
**platform_post_id** | **String** | Platform's post ID | 
**platform** | **Platform** |  (enum: instagram, facebook, twitter, youtube, linkedin, bluesky, reddit) | 
**text** | **String** | Comment text content | 
**author** | [**models::WebhookPayloadCommentCommentAuthor**](WebhookPayloadCommentCommentAuthor.md) |  | 
**created_at** | **String** |  | 
**is_reply** | **bool** | Whether this is a reply to another comment | 
**parent_comment_id** | **String** | Parent comment ID if this is a reply | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


