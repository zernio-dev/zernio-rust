# AdRuleCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | Option<**Metric**> |  (enum: spend, impressions, clicks, conversions, ctr, cpc, cpm, cpa, roas, reach, frequency, daily_budget, budget_used) | 
**window** | Option<**Window**> |  (enum: today, yesterday, last_3d, last_7d, last_14d, last_30d) | 
**op** | **Op** |  (enum: >, >=, <, <=) | 
**value** | **f64** |  | 
**compare_to** | Option<**String**> | Makes the condition relative: `value` becomes a ratio of the metric over `window` to the same metric over this window. `previous_period` is the same number of days just before `window`; any other value is a window, such as `30_to_2_days_ago`.  Spend, impressions, clicks, conversions and reach are compared per day, so windows of different lengths compare fairly; rates such as `cpc` compare as they are. A comparison window with no value never matches.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


