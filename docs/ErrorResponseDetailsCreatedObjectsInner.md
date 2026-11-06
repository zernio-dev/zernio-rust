# ErrorResponseDetailsCreatedObjectsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> |  (enum: campaign, adset, creative, ad, video, image) | [optional]
**id** | Option<**String**> | Meta object id; for `image` the image hash. | [optional]
**cleanup** | Option<**Cleanup**> | `deleted`: Zernio deleted it. `left_behind`: cleanup could not delete it (Meta refused the delete, or the delete hit a network error), so it still exists. `kept`: deliberately not deleted: an image (hashes are shared by every upload of the same file), or an object Zernio found by name after Meta lost its answer to the create, which may belong to another request with the same name. (enum: deleted, left_behind, kept) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


