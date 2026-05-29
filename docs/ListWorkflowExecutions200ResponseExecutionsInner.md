# ListWorkflowExecutions200ResponseExecutionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: running, waiting, completed, exited, failed) | [optional]
**current_node_id** | Option<**String**> |  | [optional]
**waiting_for** | Option<[**models::ListWorkflowExecutions200ResponseExecutionsInnerWaitingFor**](ListWorkflowExecutions200ResponseExecutionsInnerWaitingFor.md)> |  | [optional]
**variables** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**platform_identifier** | Option<**String**> |  | [optional]
**conversation_id** | Option<**String**> |  | [optional]
**step_count** | Option<**i32**> |  | [optional]
**last_error** | Option<**String**> |  | [optional]
**resume_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**completed_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


