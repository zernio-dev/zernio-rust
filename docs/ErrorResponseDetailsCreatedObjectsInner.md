# ErrorResponseDetailsCreatedObjectsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> |  (enum: campaign, adset, creative, ad, video, image) | [optional]
**id** | Option<**String**> | Meta object id; for `image` the image hash. | [optional]
**cleanup** | Option<**Cleanup**> | `deleted`: Zernio deleted it. `left_behind`: Meta refused the delete, so it still exists. `kept`: deliberately not deleted (image hashes are shared by every upload of the same file). (enum: deleted, left_behind, kept) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


