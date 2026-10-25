# AdRuleCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **Metric** | `ctr` is a percentage. `spend`, `cpc`, `cpm` and `cpa` are in the ad account currency. (enum: spend, impressions, clicks, conversions, ctr, cpc, cpm, cpa, roas) | 
**window** | **Window** | Days in the ad account's own timezone. `last_7d` includes today. (enum: today, yesterday, last_3d, last_7d, last_14d, last_30d) | 
**op** | **Op** |  (enum: >, >=, <, <=) | 
**value** | **f64** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


