# AdRuleRunEvaluationActionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object_id** | **String** |  | 
**r#type** | **Type** |  (enum: pause, activate, adjust_budget, adjust_bid, adjust_target, reallocate_budget, duplicate, edit_name) | 
**status** | **Status** |  (enum: done, skipped, failed) | 
**reason** | Option<**String**> | Why it was skipped or failed, for example `already_paused`. | [optional]
**previous_daily_budget** | Option<**f64**> |  | [optional]
**new_daily_budget** | Option<**f64**> |  | [optional]
**previous_name** | Option<**String**> |  | [optional]
**new_name** | Option<**String**> |  | [optional]
**previous_bid_amount** | Option<**f64**> |  | [optional]
**new_bid_amount** | Option<**f64**> |  | [optional]
**target_metric** | Option<**TargetMetric**> |  (enum: cpa, roas) | [optional]
**previous_target** | Option<**f64**> |  | [optional]
**new_target** | Option<**f64**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


