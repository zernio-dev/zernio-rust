# GoogleListingGroupNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dimension** | [**models::GoogleListingGroupDimension**](GoogleListingGroupDimension.md) |  | 
**excluded** | Option<**bool**> | Leaf only. true excludes these products. | [optional]
**children** | Option<[**Vec<models::GoogleListingGroupNode>**](GoogleListingGroupNode.md)> | Makes the node a subdivision. Children share one dimension (and level or index) and include exactly one everything-else node. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


