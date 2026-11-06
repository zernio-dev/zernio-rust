# ListAdRuleTemplates200ResponseTemplatesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**name** | **String** |  | 
**description** | **String** |  | 
**level** | [**models::AdRuleLevel**](AdRuleLevel.md) |  | 
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**actions** | [**Vec<models::AdRuleAction>**](AdRuleAction.md) | Each type at most once, and at most one of `pause`, `activate`, `adjust_budget`, `adjust_bid`, `adjust_target`, `reallocate_budget`, `duplicate` and `edit_name`. | 
**goal** | **Goal** | What the template is for: stop waste, grow what works, act at set times, or only tell you. (enum: protect, scale, schedule, alert) | 
**schedule** | [**models::AdRuleSchedule**](AdRuleSchedule.md) |  | 
**cooldown_minutes** | **i32** |  | 
**platforms** | Option<**Vec<String>**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


