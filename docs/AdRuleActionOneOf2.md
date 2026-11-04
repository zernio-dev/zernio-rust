# AdRuleActionOneOf2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Reactivate a campaign, ad set or ad a rule paused, once `cooldownMinutes` has passed since the pause. Objects you paused yourself are left alone unless `includeManuallyPaused` is true. (enum: activate) | 
**include_manually_paused** | Option<**bool**> | Also reactivate paused objects that no rule paused, as soon as they match. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]
**max_changes_per_object** | Option<**i32**> | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


