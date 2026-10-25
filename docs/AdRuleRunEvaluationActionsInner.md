# AdRuleRunEvaluationActionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object_id** | **String** |  | 
**r#type** | **Type** |  (enum: pause, activate, adjust_budget) | 
**status** | **Status** |  (enum: done, skipped, failed) | 
**reason** | Option<**String**> | Why it was skipped or failed, for example `already_paused`. | [optional]
**previous_daily_budget** | Option<**f64**> |  | [optional]
**new_daily_budget** | Option<**f64**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


