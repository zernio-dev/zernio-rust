# WorkflowExecutionEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | Option<**Action**> |  (enum: execution_started, execution_completed, execution_exited, execution_paused, execution_resumed, node_started, node_completed, node_failed, node_skipped) | [optional]
**status** | Option<**Status**> |  (enum: success, failed, pending) | [optional]
**node_id** | Option<**String**> | Present on `node_*` events | [optional]
**node_type** | Option<**String**> | Present on `node_*` events | [optional]
**source_handle** | Option<**String**> | The edge handle the executor followed out of this node (see `WorkflowEdge.sourceHandle`) | [optional]
**duration_ms** | Option<**i32**> | Node run time; present on `node_completed` and `node_failed` | [optional]
**error_message** | Option<**String**> | Failure detail; present on `node_failed` and `execution_exited` | [optional]
**meta** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Per-node-type payload. Shape varies — see WorkflowNode `type`. Examples:   `send_message` → `{ messageType, text, recipient }`,   `webhook` → `{ url, method, statusCode, responseTimeMs, responsePreview }`,   `ai` → `{ model, provider, inputTokens, outputTokens, responsePreview }`,   `condition` → `{ matchedHandle, rulesEvaluated }`,   `a_b_split` → `{ percentage, chosen }`.  | [optional]
**at** | Option<**String**> | Event timestamp (UTC) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


