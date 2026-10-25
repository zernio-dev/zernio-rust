# WebhookPayloadAdRuleTriggeredObjectsInnerConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **String** | `spend`, `impressions`, `clicks`, `conversions`, `ctr`, `cpc`, `cpm`, `cpa` or `roas`. New values may be added. | 
**window** | **String** | `today`, `yesterday`, `last_3d`, `last_7d`, `last_14d` or `last_30d`, in the account's calendar (see `run.today`). New values may be added. | 
**op** | **Op** |  (enum: >, >=, <, <=) | 
**value** | **f64** | The threshold set on the rule. | 
**actual** | Option<**f64**> | The object's value for the metric over the window. Null when it cannot be computed, for example a cost per action with no actions. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


