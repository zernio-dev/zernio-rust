# SyncExternalPosts200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**synced** | Option<[**models::SyncExternalPosts200ResponseSynced**](SyncExternalPosts200ResponseSynced.md)> |  | [optional]
**found** | Option<**bool**> | Present only when a locator (`url`/`postId`) was provided — whether the post was found. | [optional]
**post** | Option<[**models::ExternalPostSummary**](ExternalPostSummary.md)> |  | [optional]
**posts** | Option<[**Vec<models::ExternalPostSummary>**](ExternalPostSummary.md)> | The account's recent external posts. Present only when no locator was provided. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


