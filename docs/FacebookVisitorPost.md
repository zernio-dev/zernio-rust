# FacebookVisitorPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Facebook post ID (`{pageId}_{postId}`). | 
**message** | Option<**String**> | Text of the post. Null for media-only posts. | 
**created_time** | Option<**String**> | Creation time as Meta returns it (ISO 8601). | 
**from** | [**models::FacebookVisitorPostFrom**](FacebookVisitorPostFrom.md) |  | 
**permalink_url** | Option<**String**> | Public Facebook URL of the post. | 
**media** | [**models::FacebookVisitorPostMedia**](FacebookVisitorPostMedia.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


