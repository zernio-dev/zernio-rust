# PostRetryResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**error** | Option<**String**> | Present on a 207 only: summary of why the retry did not fully succeed. | [optional]
**platform_results** | Option<[**Vec<models::PostRetryPlatformResult>**](PostRetryPlatformResult.md)> | One entry per platform of the post, in `post.platforms[]` order. | [optional]
**post** | Option<[**models::Post**](Post.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


