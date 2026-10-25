# WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: pause, activate, adjust_budget) | 
**status** | **Status** | `skipped` when the action could not or need not apply (already paused or active, budget at its limit, a budget that is unknown, not daily or set at another level, no live ads, or a permanent refusal from the platform), `failed` when it errored and will be retried on the next run. (enum: done, skipped, failed) | 
**reason** | Option<**String**> | Why the action was skipped or failed: `already_paused`, `already_active`, `at_limit`, `budget_unknown`, `budget_not_daily`, `budget_level_mismatch`, `no_live_ads`, `ads_allowance_exceeded` (a reactivation or budget increase for a team past its free live-ads allowance), or the platform's message. Null when done. | 
**previous_daily_budget** | Option<**f64**> | On `adjust_budget`, the daily budget before the change, in the ad account currency. Null otherwise. | 
**new_daily_budget** | Option<**f64**> | On `adjust_budget`, the daily budget after the change. Null when nothing changed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


