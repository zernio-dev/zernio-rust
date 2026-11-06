# MetaRecoveredWritesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: campaign, adset, ad) | 
**id** | **String** | The Meta object id this response uses. | 
**adopted** | Option<**bool**> | Always true when present. Zernio found this object by name under its parent and reused it instead of creating it again. | [optional]
**reposted_after** | Option<**RepostedAfter**> | Zernio sent the create again after Meta answered a 5xx and the read-back found no such object. (enum: server_error) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


