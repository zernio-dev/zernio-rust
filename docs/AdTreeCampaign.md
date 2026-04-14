# AdTreeCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | Derived from child ad statuses (enum: active, paused, pending_review, rejected, completed, cancelled, error) | [optional]
**ad_count** | Option<**i32**> | Total ads across all ad sets | [optional]
**ad_set_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional]
**optimization_goal** | Option<[**models::AdTreeCampaignOptimizationGoal**](AdTreeCampaignOptimizationGoal.md)> |  | [optional]
**bid_strategy** | Option<**String**> | Campaign-level bid strategy (e.g. LOWEST_COST_WITHOUT_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) | [optional]
**promoted_object** | Option<[**models::AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md)> |  | [optional]
**ad_sets** | Option<[**Vec<models::AdTreeAdSet>**](AdTreeAdSet.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


