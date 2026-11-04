# UpdateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**level** | Option<[**models::AdRuleLevel**](AdRuleLevel.md)> |  | [optional]
**campaign_ids** | Option<**Vec<String>**> |  | [optional]
**filters** | Option<[**Vec<models::AdRuleFiltersInner>**](AdRuleFiltersInner.md)> | Narrows the objects the rule checks. Every filter must hold. Text compares without case, and a missing field reads as empty. | [optional]
**lifecycle** | Option<[**models::AdRuleLifecycle**](AdRuleLifecycle.md)> |  | [optional]
**conditions** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> |  | [optional]
**actions** | Option<[**Vec<models::AdRuleAction>**](AdRuleAction.md)> | Each type at most once, and at most one of `pause`, `activate`, `adjust_budget`, `adjust_bid`, `duplicate` and `edit_name`. | [optional]
**schedule** | Option<[**models::AdRuleSchedule**](AdRuleSchedule.md)> |  | [optional]
**cooldown_minutes** | Option<**i32**> |  | [optional]
**enabled** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


