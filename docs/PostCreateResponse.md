# PostCreateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**post** | Option<[**models::Post**](Post.md)> |  | [optional]
**warnings** | Option<**Vec<String>**> | Advisory notices about a post that was still created: media truncated for a platform, a recycling caveat, or a field that was ignored because it sat outside platforms[].platformSpecificData. Absent when there are none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


