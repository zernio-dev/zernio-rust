# AdRuleActionOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Change the daily budget. Google ad groups have no budget of their own, so on Google it needs a campaign-level rule. (enum: adjust_budget) | 
**direction** | **Direction** |  (enum: increase, decrease) | 
**percent** | **i32** | Change in percent: up to 100 for an increase, up to 90 for a decrease. | 
**limit** | **f64** | The budget never goes above this on an increase, or below it on a decrease, in the ad account currency. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


