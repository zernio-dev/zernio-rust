# SupportRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **String** | Run id, a 24-character hex string. | 
**thread_id** | **String** | Conversation thread id. Send it back as `threadId` to ask a follow-up in the same thread. | 
**status** | **Status** | queued and running are in progress. needs_human means Ana handed the question to a person instead of answering. (enum: queued, running, completed, needs_human, failed) | 
**stop_reason** | Option<**StopReason**> | Why the run stopped. Null while it is in progress. (enum: answered, human_review, cost_cap, deadline, max_iterations, error, expired, ) | 
**answer** | Option<**String**> | Ana's answer. Null while the run is in progress or when it failed. | 
**usage** | [**models::SupportRunUsage**](SupportRunUsage.md) |  | 
**cost_usd** | **f64** | The amount billed for the run, in USD: the model cost plus 20%, never above `maxCostUsd`. 0 for a failed run. | 
**max_cost_usd** | **f64** | The cost cap this run was started with, in USD. | 
**created_at** | **String** |  | 
**started_at** | Option<**String**> |  | 
**finished_at** | Option<**String**> |  | 
**poll_after_seconds** | Option<**i32**> | Seconds to wait before polling again. Present only while the run is queued or running. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


