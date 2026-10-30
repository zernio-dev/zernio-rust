# AdRuleActionOneOf2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Reactivate a campaign, ad set or ad a rule paused, once `cooldownMinutes` has passed since the pause. Objects you paused yourself are never touched. (enum: activate) | 
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


