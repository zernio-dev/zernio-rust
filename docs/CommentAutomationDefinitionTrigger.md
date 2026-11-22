# CommentAutomationDefinitionTrigger

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | `comment.keyword` for a comment on a post or reel. The `comment.received` event starts an event automation, not comment to DM. (enum: comment.keyword, comment.live, story.reply, story.mention) | 
**profile_id** | **String** |  | 
**account_id** | **String** | The account it answers on, on the profile. It cannot change once saved. | 
**platform_post_id** | Option<**String**> | The platform post or story it answers. Null answers every one. One active automation per post. | [optional]
**post_id** | Option<**String**> | A Zernio post. A scheduled one is answered once it publishes. | [optional]
**post_title** | Option<**String**> |  | [optional]
**filter** | [**models::CommentAutomationFilter**](CommentAutomationFilter.md) |  | 
**entry** | **Vec<String>** | The nodes a run starts at. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


