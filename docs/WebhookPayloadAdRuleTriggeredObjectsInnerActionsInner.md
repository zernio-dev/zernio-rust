# WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: pause, activate, adjust_budget, adjust_bid, adjust_target, reallocate_budget, duplicate, edit_name) | 
**status** | **Status** | Action result.  - `skipped`: the action could not or need not apply (already paused or active, budget at its limit, a budget that is unknown, not daily or set at another level, no live ads, or a permanent refusal from the platform). - `failed`: it errored and will be retried on the next run. (enum: done, skipped, failed) | 
**reason** | Option<**String**> | Why the action was skipped or failed, or the platform's message. Null when done.  Skipped: `already_paused`, `already_active`, `at_limit`, `budget_unknown`, `budget_not_daily`, `budget_level_mismatch`, `no_live_ads`, `budget_shared`, `portfolio_bid_strategy`, `unsupported_bid_strategy`, `no_target_cpa`, `no_target_roas`.  `daily_limit_reached`: held back by the action's `maxChangesPerDay`. `ads_allowance_exceeded`: a reactivation or budget increase for a team past its free live-ads allowance.  `reallocation_incomplete` (failed): a receiver left alone because a giver's cut did not apply, tried again next run. | 
**previous_daily_budget** | Option<**f64**> | On `adjust_budget`, the daily budget before the change, in the ad account currency. Null otherwise. | 
**new_daily_budget** | Option<**f64**> | On `adjust_budget`, the daily budget after the change. Null when nothing changed. | 
**previous_name** | Option<**String**> | On `edit_name`, the object's name before the change. Null otherwise. | 
**new_name** | Option<**String**> | On `edit_name`, the name after the change. Null when nothing changed. | 
**previous_bid_amount** | Option<**f64**> | On `adjust_bid`, the cap before the change. Null otherwise. | 
**new_bid_amount** | Option<**f64**> | On `adjust_bid`, the cap after the change. Null when nothing changed. | 
**target_metric** | Option<**TargetMetric**> | On `adjust_target`, which target moved. Null otherwise. (enum: cpa, roas, ) | 
**previous_target** | Option<**f64**> | On `adjust_target`, the target before the change. Null otherwise. | 
**new_target** | Option<**f64**> | On `adjust_target`, the target after the change. Null when nothing changed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


