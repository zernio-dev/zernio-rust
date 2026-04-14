# Ad

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> |  | [optional]
**ad_type** | Option<**AdType**> |  (enum: boost, standalone) | [optional]
**goal** | Option<**Goal**> |  (enum: engagement, traffic, awareness, video_views) | [optional]
**is_external** | Option<**bool**> | True for ads synced from platform ad managers | [optional]
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_id** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC). Only present for Meta ads. | [optional]
**optimization_goal** | Option<**String**> | Meta ad set optimization goal (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION, LINK_CLICKS). Only present for Meta ads. | [optional]
**bid_strategy** | Option<**String**> | Bid strategy (e.g. LOWEST_COST_WITHOUT_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS). Ad set level overrides campaign level. Only present for Meta ads. | [optional]
**promoted_object** | Option<[**models::AdPromotedObject**](AdPromotedObject.md)> |  | [optional]
**creative** | Option<[**models::AdCreative**](AdCreative.md)> |  | [optional]
**targeting** | Option<**serde_json::Value**> |  | [optional]
**schedule** | Option<[**models::AdSchedule**](AdSchedule.md)> |  | [optional]
**rejection_reason** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


