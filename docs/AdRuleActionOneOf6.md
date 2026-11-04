# AdRuleActionOneOf6

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Set the daily budget to an exact amount, such as a reset every midnight. Same level rules as the percent change. (enum: adjust_budget) | 
**amount** | **f64** | The daily budget to set, in the ad account currency. An object already at it is skipped with `already_at_amount`. | 
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


