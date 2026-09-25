# GetInboxPostComments200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**String**> |  | [optional]
**comments** | Option<[**Vec<models::GetInboxPostComments200ResponseCommentsInner>**](GetInboxPostComments200ResponseCommentsInner.md)> |  | [optional]
**post** | Option<[**models::GetInboxPostComments200ResponsePost**](GetInboxPostComments200ResponsePost.md)> |  | [optional]
**comment** | Option<**serde_json::Value**> | (Facebook and Instagram only) Present when `commentId` was passed: the requested comment itself, in the same shape as an entry in comments[]. comments[] then holds that comment's replies instead of the post's top-level comments.  | [optional]
**pagination** | Option<[**models::GetInboxPostComments200ResponsePagination**](GetInboxPostComments200ResponsePagination.md)> |  | [optional]
**meta** | Option<[**models::GetInboxPostComments200ResponseMeta**](GetInboxPostComments200ResponseMeta.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


