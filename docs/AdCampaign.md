# AdCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai) | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> | Delivery status derived from child ad statuses. Distinct from `reviewStatus`. | [optional]
**review_status** | Option<[**models::AdReviewStatus**](AdReviewStatus.md)> |  | [optional]
**platform_campaign_status** | Option<**String**> | Raw platform-level campaign status (Meta `effective_status`; ChatGPT (OpenAI): the campaign's own switch, active / paused / archived; TikTok: the campaign's own switch `operation_status`, ENABLE / DISABLE). | [optional]
**status_read_at** | Option<**String**> | Only on GET /v1/ads/campaigns with `live=true`. When `platformCampaignStatus` was read from the platform; null when this campaign could not be read live. | [optional]
**native_settings** | Option<**std::collections::HashMap<String, serde_json::Value>**> | TikTok only, only on GET /v1/ads/campaigns with `live=true` and only on campaigns read live. TikTok's campaign/get record verbatim: operation_status, objective_type, budget_mode (BUDGET_MODE_INFINITE means no campaign budget, so budget lives on the ad groups), budget, and budget_optimize_on when TikTok returns it. Plus advertiser_currency and advertiser_timezone from TikTok's advertiser/info. | [optional]
**config_read_at** | Option<**String**> | Only on GET /v1/ads/campaigns with `live=true`. When `nativeSettings` was read from the platform. Null whenever native settings were not read now. | [optional]
**campaign_issues_info** | Option<**Vec<serde_json::Value>**> | Platform-reported campaign issues (Meta `issues_info[]`). | [optional]
**ad_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdCampaignBudget**](AdCampaignBudget.md)> |  | [optional]
**campaign_budget** | Option<[**models::AdCampaignBudget**](AdCampaignBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> | Canonical CBO/ABO indicator. See AdTreeCampaign.budgetLevel. (enum: campaign, adset) | [optional]
**is_budget_schedule_enabled** | Option<**bool**> | Meta-only. Mirrors Campaign.is_budget_schedule_enabled. | [optional][default to false]
**currency** | Option<**String**> | ISO 4217 currency code for all budget amounts. Budgets are NOT normalized to USD. | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**platform_ad_account_name** | Option<**String**> | Human-readable advertiser/account name from the platform. Refreshed on every sync. | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**advertising_channel_type** | Option<**String**> | Google-only. Raw campaign.advertising_channel_type. See AdTreeCampaign.advertisingChannelType. | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional]
**optimization_goal** | Option<[**models::AdTreeCampaignOptimizationGoal**](AdTreeCampaignOptimizationGoal.md)> |  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Representative bid from the top-spending ad set (whole currency units). Meta: populated when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. LinkedIn: the campaign unitCost, ungated, where 0 is a real delivery-stopping value. | [optional]
**roas_average_floor** | Option<**f64**> | Representative ROAS floor from the top-spending ad set. Decimal multiplier (2.0 = 2.0x). | [optional]
**promoted_object** | Option<[**models::AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md)> |  | [optional]
**earliest_ad** | Option<**String**> |  | [optional]
**latest_ad** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


