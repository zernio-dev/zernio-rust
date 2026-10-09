# BrowseAdTargeting200ResponseNodesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_id** | **String** | Identifies the node within this response. Not a Meta id: never put it in a targeting spec. | 
**parent_node_id** | Option<**String**> | nodeId of the parent organizational node, null for a root. | 
**id** | Option<**String**> | Meta targeting id, null on organizational nodes. | 
**name** | **String** |  | 
**r#type** | Option<**String**> | Meta's targeting spec key (interests, behaviors, industries, life_events, education_statuses, relationship_statuses, family_statuses, income, ...). Null on most organizational nodes. | 
**path** | **Vec<String>** | Labels of the ancestors, root first. Does not include the node itself. | 
**selectable** | **bool** | True when the node can be targeted (it has a Meta id). | 
**description** | Option<**String**> | Meta's description, when it has one. | [optional]
**audience_size_lower_bound** | Option<**i32**> | Meta's estimated audience size, lower bound, when reported. | [optional]
**audience_size_upper_bound** | Option<**i32**> | Meta's estimated audience size, upper bound, when reported. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


