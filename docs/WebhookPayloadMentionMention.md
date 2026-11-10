# WebhookPayloadMentionMention

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Mention ID, the same as `id` on GET /v1/inbox/mentions. | 
**platform** | **Platform** |  (enum: instagram, facebook, linkedin) | 
**r#type** | Option<**Type**> | Null on LinkedIn. (enum: caption, post, comment, ) | 
**media_id** | Option<**String**> | Instagram media ID. | 
**post_id** | Option<**String**> | Facebook post ID. | 
**comment_id** | Option<**String**> |  | 
**content** | Option<**String**> | Text that mentioned the account. | 
**permalink** | Option<**String**> | URL to the source post on LinkedIn. Null on Instagram and Facebook. | 
**author_urn** | Option<**String**> |  | 
**author_name** | Option<**String**> |  | 
**author_username** | Option<**String**> |  | 
**author_picture** | Option<**String**> |  | 
**organizational_entity** | **String** | The mentioned organization, Page or Instagram account. | 
**published_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


