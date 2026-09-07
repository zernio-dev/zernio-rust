# PostPublishIncompleteResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post** | Option<[**models::Post**](Post.md)> |  | [optional]
**message** | Option<**String**> | Human-readable summary of the publish outcome. | [optional]
**error** | Option<**String**> | Present when no platform published. Absent on a partial success. Informational only; the per-platform detail is in `platformResults` and in `post.platforms[]`. | [optional]
**platform_results** | Option<[**Vec<models::PostPublishIncompleteResponsePlatformResultsInner>**](PostPublishIncompleteResponsePlatformResultsInner.md)> | Per-platform outcome of the publish attempt. Omitted when the attempt aborted before producing per-platform results (for example the post was already being processed); read `post.platforms[]` in that case. | [optional]
**warnings** | Option<**Vec<String>**> | Advisory notices about the post that was still created. Absent when there are none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


