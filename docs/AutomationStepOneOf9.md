# AutomationStepOneOf9

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**Id**> |  (enum: reallocate) | [optional]
**r#type** | **Type** |  (enum: ads.reallocate_budget) | 
**metric** | **String** | A condition metric or `result:<key>`, not a calendar metric. | 
**window** | **String** | A condition window. | 
**best** | Option<**Best**> | Which end is best. Defaults to lowest for `cpa`, `cpc`, `cpm`, `frequency` and cost results, highest otherwise. (enum: highest, lowest) | [optional]
**from** | **i32** | How many objects give budget. | 
**to** | **i32** | How many objects receive it. | 
**by** | Option<**String**> | From 1% to 90%. | [optional]
**amount** | Option<**f64**> |  | [optional]
**min** | Option<**f64**> | A giver's budget never goes below this. | [optional]
**max** | Option<**f64**> | A receiver's budget never goes above this. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


