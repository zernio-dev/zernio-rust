# AdTreeCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> | Delivery status derived from child ad statuses. Distinct from `reviewStatus`, which reflects the platform-side review state. | [optional]
**review_status** | Option<**ReviewStatus**> | Platform-side review state of the campaign. Independent of the children-derived delivery `status`: a campaign can have ads already active (status=active) while the campaign itself is still being reviewed by the platform (reviewStatus=in_review). For Meta, derived from `effective_status` + `issues_info` on the Campaign, plus ad-level PENDING_REVIEW rollup.  (enum: in_review, approved, rejected, with_issues) | [optional]
**platform_campaign_status** | Option<**String**> | Raw platform-level campaign status (Meta `effective_status`: ACTIVE, PAUSED, DELETED, ARCHIVED, IN_PROCESS, WITH_ISSUES). Distinct from per-ad `platformStatus`. | [optional]
**campaign_issues_info** | Option<**Vec<serde_json::Value>**> | Platform-reported campaign issues (Meta `issues_info[]`). Populated only when the platform has delivery issues to report; contains the specific error codes and messages. | [optional]
**ad_count** | Option<**i32**> | Total ads across all ad sets | [optional]
**ad_set_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdTreeCampaignBudget**](AdTreeCampaignBudget.md)> |  | [optional]
**campaign_budget** | Option<[**models::AdTreeCampaignCampaignBudget**](AdTreeCampaignCampaignBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> | Canonical CBO/ABO indicator. `campaign` = CBO (Advantage Campaign Budget, budget lives on the campaign). `adset` = ABO (budget lives on each ad set). Route budget updates to the matching Meta entity. (enum: campaign, adset) | [optional]
**is_budget_schedule_enabled** | Option<**bool**> | Meta-only. Mirrors Campaign.is_budget_schedule_enabled — true when the campaign uses budget scheduling (time-based budget changes). Independent of CBO/ABO. | [optional][default to false]
**currency** | Option<**String**> | ISO 4217 currency code (e.g. USD, EUR, CLP, JPY) for all budget amounts in this campaign node. Budgets are NOT normalized to USD. | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional]
**optimization_goal** | Option<**String**> | Meta optimization goal shared across ad sets, or comma-separated values when ad sets differ (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION) | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Campaign-level bid strategy. Ad sets inherit this unless they override. | [optional]
**bid_amount** | Option<**f64**> | Representative bid cap for the campaign — bubbled up from the top-spending ad set's `bid_amount` (whole currency units). Populated when the ad-set bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. | [optional]
**roas_average_floor** | Option<**f64**> | Representative ROAS floor for the campaign — bubbled up from the top-spending ad set. Decimal multiplier (2.0 = 2.0x). | [optional]
**promoted_object** | Option<[**models::AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md)> |  | [optional]
**ad_sets** | Option<[**Vec<models::AdTreeAdSet>**](AdTreeAdSet.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


