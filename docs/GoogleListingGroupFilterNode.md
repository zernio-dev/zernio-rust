# GoogleListingGroupFilterNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**resource_name** | **String** | customers/{customerId}/assetGroupListingGroupFilters/{assetGroupId}~{filterId} | 
**parent_resource_name** | Option<**String**> | Null for the root node. | 
**r#type** | **Type** |  (enum: SUBDIVISION, UNIT_INCLUDED, UNIT_EXCLUDED) | 
**listing_source** | **String** |  | 
**dimension** | Option<**serde_json::Value**> | Google's case value for the node, such as { productBrand: { value: 'Acme' } }. A dimension with no value is the everything-else node. Null for the root. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


