# AdRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**name** | **String** |  | 
**account_id** | **String** | The ads connection the rule acts through. | 
**platform** | **String** | Ad platform, for example `facebook` (Meta) or `google`. | 
**ad_account_id** | **String** | Platform ad account ID. | 
**level** | [**models::AdRuleLevel**](AdRuleLevel.md) |  | 
**campaign_ids** | Option<**Vec<String>**> | Platform campaign IDs the rule is limited to. Null checks the whole ad account. | 
**filters** | [**Vec<models::AdRuleFiltersInner>**](AdRuleFiltersInner.md) | Narrows the objects the rule checks. Every filter must hold. A campaign rule reads `name`, `campaign_id`, `goal`, `days_live` and `budget_level`; an ad set rule also `campaign_name` and `adset_id`; an ad rule also `adset_name` and `ad_id`. | 
**groups** | Option<[**Vec<models::AdRuleGroupsInner>**](AdRuleGroupsInner.md)> | Campaigns judged together, campaign rules only. Each group's numbers and your results are added up across its campaigns, and rates and formulas are computed on the totals: a group's `result:cac_percent` is its total spend over its total revenue.  The conditions are judged once per group, and a matching group acts on each of its campaigns, each with its own cooldown and daily cap. Paused campaigns count toward a group's totals; only the ones the rule may act on are changed.  A group with no filters holds every campaign the rule checks: the whole ad account. A campaign in several groups is acted on once per run, by the first matching group. Reach and frequency cannot be added up across campaigns, so a rule with groups cannot use them.  A campaign with no results sent for the window adds its spend and no results to its group. A result sent as a rate (kind `percent` or `ratio`, no formula) reads as unknown for a group; define it as a formula over counts.  | 
**lifecycle** | Option<[**models::AdRuleLifecycle**](AdRuleLifecycle.md)> |  | 
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**actions** | [**Vec<models::AdRuleAction>**](AdRuleAction.md) | Each type at most once, and at most one of `pause`, `activate`, `adjust_budget`, `adjust_bid`, `adjust_target`, `reallocate_budget`, `duplicate` and `edit_name`. | 
**schedule** | [**models::AdRuleSchedule**](AdRuleSchedule.md) |  | 
**cooldown_minutes** | **i32** |  | 
**enabled** | **bool** |  | 
**last_run_at** | Option<**String**> |  | 
**next_run_at** | Option<**String**> | Null while the rule is disabled. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


