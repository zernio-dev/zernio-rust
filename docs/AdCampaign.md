# AdCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> | Delivery status derived from child ad statuses. Distinct from `reviewStatus`. | [optional]
**review_status** | Option<**ReviewStatus**> | Platform-side review state of the campaign. See AdTreeCampaign.reviewStatus for the full description. (enum: in_review, approved, rejected, with_issues) | [optional]
**platform_campaign_status** | Option<**String**> | Raw platform-level campaign status (Meta `effective_status`). | [optional]
**campaign_issues_info** | Option<**Vec<serde_json::Value>**> | Platform-reported campaign issues (Meta `issues_info[]`). | [optional]
**ad_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdCampaignBudget**](AdCampaignBudget.md)> |  | [optional]
**campaign_budget** | Option<[**models::AdCampaignCampaignBudget**](AdCampaignCampaignBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> | Canonical CBO/ABO indicator. See AdTreeCampaign.budgetLevel. (enum: campaign, adset) | [optional]
**is_budget_schedule_enabled** | Option<**bool**> | Meta-only. Mirrors Campaign.is_budget_schedule_enabled. | [optional][default to false]
**currency** | Option<**String**> | ISO 4217 currency code for all budget amounts. Budgets are NOT normalized to USD. | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional]
**optimization_goal** | Option<**String**> | Meta optimization goal shared across ad sets, or comma-separated values when ad sets differ (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION) | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Campaign-level bid strategy. Ad sets inherit this unless they override. | [optional]
**bid_amount** | Option<**f64**> | Representative bid cap from the top-spending ad set (whole currency units). Populated when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. | [optional]
**roas_average_floor** | Option<**f64**> | Representative ROAS floor from the top-spending ad set. Decimal multiplier (2.0 = 2.0x). | [optional]
**promoted_object** | Option<[**models::AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md)> |  | [optional]
**earliest_ad** | Option<**String**> |  | [optional]
**latest_ad** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


