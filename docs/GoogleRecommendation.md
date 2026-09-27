# GoogleRecommendation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource_name** | **String** | customers/{customerId}/recommendations/{id}. Pass it to apply or dismiss. | 
**id** | **String** |  | 
**r#type** | **String** | Google RecommendationType, such as CAMPAIGN_BUDGET, KEYWORD or SET_TARGET_CPA. | 
**dismissed** | **bool** |  | 
**campaign_id** | Option<**String**> |  | 
**campaign_ids** | **Vec<String>** | Every campaign the recommendation targets (several for account-level types). | 
**ad_group_id** | Option<**String**> |  | 
**campaign_budget_id** | Option<**String**> |  | 
**impact** | [**models::GoogleRecommendationImpact**](GoogleRecommendationImpact.md) |  | 
**details** | Option<**serde_json::Value**> | The type-specific recommendation payload exactly as Google returns it (camelCase, amounts in micros), for example recommendedTargetCpaMicros or budgetOptions. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


