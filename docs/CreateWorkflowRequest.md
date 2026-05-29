# CreateWorkflowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** |  | 
**platform** | Option<**Platform**> |  (enum: whatsapp, instagram, facebook, telegram, twitter, bluesky, reddit) | [optional][default to Whatsapp]
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**nodes** | Option<[**Vec<models::WorkflowNode>**](WorkflowNode.md)> |  | [optional]
**edges** | Option<[**Vec<models::WorkflowEdge>**](WorkflowEdge.md)> |  | [optional]
**entry_node_id** | Option<**String**> | The trigger node id; derived from the single trigger node if omitted | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


