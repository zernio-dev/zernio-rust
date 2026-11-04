# AdRuleCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | Option<**Metric**> |  (enum: spend, impressions, clicks, conversions, ctr, cpc, cpm, cpa, roas, reach, frequency, daily_budget, budget_used, day_of_month, working_day_of_month) | 
**window** | Option<**Window**> |  (enum: today, yesterday, last_3d, last_7d, last_14d, last_30d, this_month, last_month) | 
**op** | **Op** | `top` and `bottom` rank the rule's objects by the metric over the window, highest first for `top`, and match the first `value` (a whole number from 1 to 100). Objects with no value are not ranked; the run history shows each one's position. (enum: >, >=, <, <=, top, bottom) | 
**value** | **f64** |  | 
**compare_to** | Option<**String**> | Makes the condition relative: `value` becomes a ratio of the metric over `window` to the same metric over this window, such as `30_to_2_days_ago`.  `previous_period` is the same number of days just before `window`. For `this_month` it is the same days of last month, and for `last_month` the month before.  Spend, impressions, clicks, conversions and reach are compared per day, so windows of different lengths compare fairly; rates such as `cpc` compare as they are. A comparison window with no value never matches.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


