# AdRuleObjectEvaluationConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **Metric** |  (enum: spend, impressions, clicks, conversions, ctr, cpc, cpm, cpa, roas, reach, frequency) | 
**window** | **Window** | Days in the ad account's own timezone. `last_7d` is the 7 full days before today; only `today` reads the day in progress. (enum: today, yesterday, last_3d, last_7d, last_14d, last_30d) | 
**op** | **Op** |  (enum: >, >=, <, <=) | 
**value** | **f64** |  | 
**actual** | Option<**f64**> | The object's value over the window. Null when it cannot be computed. | 
**met** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


