# CreateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**account_id** | **String** | The ads connection (account ID from `GET /v1/accounts`). | 
**ad_account_id** | **String** | Platform ad account ID, from `GET /v1/ads/accounts`. | 
**level** | [**models::AdRuleLevel**](AdRuleLevel.md) |  | 
**campaign_ids** | Option<**Vec<String>**> | Only check these platform campaign IDs (or their ad sets). Leave out to check the whole ad account. | [optional]
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**actions** | [**Vec<models::AdRuleAction>**](AdRuleAction.md) | Each type at most once, and at most one of `pause`, `activate` and `adjust_budget`. | 
**schedule** | Option<[**models::AdRuleSchedule**](AdRuleSchedule.md)> | Leave it out to run every 60 minutes. | [optional]
**cooldown_minutes** | Option<**i32**> | How long the rule leaves an object alone after acting on it. | [optional][default to 1440]
**enabled** | Option<**bool**> |  | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


