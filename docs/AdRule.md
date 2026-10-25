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
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**actions** | [**Vec<models::AdRuleAction>**](AdRuleAction.md) | Each type at most once, and at most one of `pause`, `activate` and `adjust_budget`. | 
**schedule** | [**models::AdRuleSchedule**](AdRuleSchedule.md) |  | 
**cooldown_minutes** | **i32** |  | 
**enabled** | **bool** |  | 
**last_run_at** | Option<**String**> |  | 
**next_run_at** | Option<**String**> | Null while the rule is disabled. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


