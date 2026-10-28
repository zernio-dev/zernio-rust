# AdRuleActivityEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable ID of this entry. | 
**ran_at** | **String** |  | 
**rule_id** | **String** |  | 
**rule_name** | **String** | The rule's name when it acted. | 
**platform** | **String** |  | 
**account_id** | **String** | The ads connection the rule runs on. | 
**ad_account_id** | **String** |  | 
**level** | **Level** |  (enum: campaign, adset) | 
**object_id** | **String** | Platform ID of the campaign or ad set. | 
**object_name** | Option<**String**> | Its name when the rule acted. | 
**r#type** | **Type** |  (enum: pause, activate, adjust_budget) | 
**status** | **Status** |  (enum: done, skipped, failed) | 
**reason** | Option<**String**> | Why it was skipped or failed, for example `already_paused`. | 
**previous_daily_budget** | Option<**f64**> |  | 
**new_daily_budget** | Option<**f64**> |  | 
**currency** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


