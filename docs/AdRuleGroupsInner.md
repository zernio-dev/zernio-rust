# AdRuleGroupsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Unique in the rule, ignoring case. | 
**filters** | [**Vec<models::AdRuleFiltersInner>**](AdRuleFiltersInner.md) | Narrows the objects the rule checks. Every filter must hold. A campaign rule reads `name`, `campaign_id`, `goal`, `days_live`, `days_since_change`, `budget_level` and `channel_type`; an ad set rule all but `days_since_change`, plus `campaign_name` and `adset_id`; an ad rule also `adset_name` and `ad_id`. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


