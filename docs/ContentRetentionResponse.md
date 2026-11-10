# ContentRetentionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | **Mode** | `standard` stores content. `none` is zero content retention: identifiers and metadata only. (enum: standard, none) | 
**profile_ids** | Option<**Vec<String>**> | Returned by GET. Profiles that use zero content retention on their own while the team is `standard`. Change one with `contentRetention` on PUT /v1/profiles/{profileId}. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


