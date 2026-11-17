# AdRuleRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**ran_at** | **String** |  | 
**outcome** | **Outcome** | Result of the rule run:  - `triggered`: the rule acted on at least one object (`error` is set if the webhook could not be sent afterwards). - `cooldown`: objects matched but all were in cooldown. - `daily_limit`: objects matched but the rule had used its `maxChangesPerDay`. - `paused`: the run did not happen: the team used its free automation runs with no payment method on file (see `error`). - `no_match`: nothing matched. - `failed`: the metrics could not be read, every action failed, or the webhook of a notify-only rule could not be sent (see `error`).  (enum: triggered, cooldown, daily_limit, no_match, failed, paused) | 
**objects_evaluated** | **i32** | Objects the rule judged. 0 means its campaigns and filters matched nothing that is running. | 
**acted_object_ids** | **Vec<String>** |  | 
**evaluation** | [**models::AdRuleRunEvaluation**](AdRuleRunEvaluation.md) |  | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


