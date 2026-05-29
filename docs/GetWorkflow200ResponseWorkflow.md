# GetWorkflow200ResponseWorkflow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: draft, active, paused) | [optional]
**entry_node_id** | Option<**String**> |  | [optional]
**nodes** | Option<[**Vec<models::WorkflowNode>**](WorkflowNode.md)> |  | [optional]
**edges** | Option<[**Vec<models::WorkflowEdge>**](WorkflowEdge.md)> |  | [optional]
**total_started** | Option<**i32**> |  | [optional]
**total_completed** | Option<**i32**> |  | [optional]
**total_exited** | Option<**i32**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


