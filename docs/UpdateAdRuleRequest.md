# UpdateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**level** | Option<[**models::AdRuleLevel**](AdRuleLevel.md)> |  | [optional]
**campaign_ids** | Option<**Vec<String>**> |  | [optional]
**filters** | Option<[**Vec<models::AdRuleFiltersInner>**](AdRuleFiltersInner.md)> | Narrows the objects the rule checks. Every filter must hold. A campaign rule reads `name`, `campaign_id`, `goal`, `days_live`, `days_since_change` and `budget_level`; an ad set rule all but `days_since_change`, plus `campaign_name` and `adset_id`; an ad rule also `adset_name` and `ad_id`. | [optional]
**groups** | Option<[**Vec<models::AdRuleGroupsInner>**](AdRuleGroupsInner.md)> | Null removes the groups; each campaign is then judged on its own. | [optional]
**lifecycle** | Option<[**models::AdRuleLifecycle**](AdRuleLifecycle.md)> |  | [optional]
**conditions** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> |  | [optional]
**actions** | Option<[**Vec<models::AdRuleAction>**](AdRuleAction.md)> | Each type at most once, and at most one of `pause`, `activate`, `adjust_budget`, `adjust_bid`, `adjust_target`, `reallocate_budget`, `duplicate` and `edit_name`. | [optional]
**schedule** | Option<[**models::AdRuleSchedule**](AdRuleSchedule.md)> |  | [optional]
**cooldown_minutes** | Option<**i32**> |  | [optional]
**enabled** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


