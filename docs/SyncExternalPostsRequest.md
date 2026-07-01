# SyncExternalPostsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID whose posts to sync. Must be connected to Zernio. | 
**url** | Option<**String**> | The post URL to locate. Optional. Provide `url` or `postId` to return a specific post; omit both to just refresh and return the account's recent posts. | [optional]
**post_id** | Option<**String**> | The platform post/media/video id to locate, as an alternative to `url`. Optional. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


