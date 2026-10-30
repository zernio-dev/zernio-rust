# AdRuleActionOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Change the daily budget. Not on ad-level rules (an ad has no budget), and on Google it needs a campaign-level rule (ad groups have no budget of their own). (enum: adjust_budget) | 
**direction** | **Direction** |  (enum: increase, decrease) | 
**percent** | **i32** | Change in percent: up to 100 for an increase, up to 90 for a decrease. | 
**limit** | **f64** | The budget never goes above this on an increase, or below it on a decrease, in the ad account currency. | 
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


