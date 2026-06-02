# WorkflowEdge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**source** | **String** | Source node id | 
**target** | **String** | Target node id | 
**source_handle** | Option<**String**> | Selects a branch output of a multi-output node. Null (or omitted) = the node's single/default output. Known handles per node type:    - **condition** — a rule's `id`, or `'default'` (no rule matched)   - **wait_for_reply** — `'reply'` (contact replied) | `'timeout'` (no reply in window)   - **webhook** — `'success'` (2xx) | `'error'` (non-2xx / fetch failed)   - **ai** — `'success'` (text/JSON response) | `'tool:<toolName>'` (model invoked     that tool) | `'error'` (upstream failure / non-JSON in JSON mode)   - **start_call** — `'success'` | `'permission_required'` | `'failed'`   - **a_b_split** — `'a'` | `'b'`   - **enroll_sequence** — `'success'` | `'error'`  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


