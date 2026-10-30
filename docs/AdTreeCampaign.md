# AdTreeCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | Option<**std::collections::HashMap<String, f64>**> | Only with `results=true`. The values you sent for this campaign over the range, plus each formula they allow, by metric key. A metric with no value is absent. | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai, reddit) | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> | Earliest `platformCreatedAt` across every ad in the campaign (platform ad creation time; falls back to `createdAt`, Zernio's sync time, for ads synced before that field existed).  Not the platform campaign's own creation time (Meta's `Campaign.created_time` etc. is not synced). A campaign created empty and populated later shows its first ad's time, not the campaign's.  Usable for sorting \"most recently created\" without the numeric-campaign-id heuristic. Same source as `AdTreeAdSet.createdTime` and `Ad.platformCreatedAt`; mirrors `AdCampaign.earliestAd`.  | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> | Delivery status derived from child ad statuses. Distinct from `reviewStatus`, which reflects the platform-side review state. | [optional]
**review_status** | Option<[**models::AdReviewStatus**](AdReviewStatus.md)> |  | [optional]
**platform_campaign_status** | Option<**String**> | Raw platform-level campaign status (Meta `effective_status`: ACTIVE, PAUSED, DELETED, ARCHIVED, IN_PROCESS, WITH_ISSUES; ChatGPT (OpenAI): the campaign's own switch, active / paused / archived, independent of the delivery `status`; TikTok: the campaign's own switch `operation_status`, ENABLE / DISABLE; Reddit: the campaign's `configured_status`, ACTIVE / PAUSED / ARCHIVED). Distinct from per-ad `platformStatus`. | [optional]
**campaign_issues_info** | Option<**Vec<serde_json::Value>**> | Platform-reported campaign issues (Meta `issues_info[]`). Populated only when the platform has delivery issues to report; contains the specific error codes and messages. | [optional]
**ad_count** | Option<**i32**> | Total ads across all ad sets | [optional]
**ad_set_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdTreeCampaignBudget**](AdTreeCampaignBudget.md)> |  | [optional]
**campaign_budget** | Option<[**models::AdTreeCampaignCampaignBudget**](AdTreeCampaignCampaignBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> | Canonical CBO/ABO indicator. `campaign` = CBO (Advantage Campaign Budget, budget lives on the campaign). `adset` = ABO (budget lives on each ad set). Route budget updates to the matching Meta entity. (enum: campaign, adset) | [optional]
**is_budget_schedule_enabled** | Option<**bool**> | Meta-only. Mirrors Campaign.is_budget_schedule_enabled: true when the campaign uses budget scheduling (time-based budget changes). Independent of CBO/ABO. | [optional][default to false]
**currency** | Option<**String**> | ISO 4217 currency code (e.g. USD, EUR, CLP, JPY) for all budget amounts in this campaign node. Budgets are NOT normalized to USD. | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**previous_metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> | Only with `compare=previous`. The same metrics over `previousRange`. | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**platform_ad_account_name** | Option<**String**> | Human-readable advertiser/account name from the platform. Refreshed on every sync. | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> | Profile the row belongs to: the profile of its owning connection (`accountId`); when that connection no longer exists, the requested profile (`profileId` filter) that reaches the row ad account, else the profile of the oldest connection of the row owner that reaches it. | [optional]
**is_smart_plus** | Option<**bool**> | TikTok only. true when the campaign is an Upgraded Smart+ campaign (TikTok lists it on /smart_plus/campaign/get/), false when it is not.  Set by ads sync, so the key is absent on other platforms and on TikTok campaigns not synced since this field shipped.  On Smart+ objects Zernio can pause, resume, rename, delete and change the budget of the campaign and ad set, and pause or resume an ad. Other edits answer 422 and belong in TikTok Ads Manager. | [optional]
**advertising_channel_type** | Option<**String**> | Google-only. Raw campaign.advertising_channel_type (SEARCH, PERFORMANCE_MAX, LOCAL_SERVICES, VIDEO, DEMAND_GEN, DISPLAY, SHOPPING, ...). Serving surface, distinct from platformObjective (advertiser intent). Null/absent for non-Google platforms. | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional]
**optimization_goal** | Option<[**models::AdTreeCampaignOptimizationGoal**](AdTreeCampaignOptimizationGoal.md)> |  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Representative bid for the campaign, bubbled up from the top-spending ad set (whole currency units). Meta: populated when the ad-set bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. LinkedIn: the campaign unitCost, which has no bidStrategy gate and where 0 is a real, delivery-stopping value rather than unset. | [optional]
**roas_average_floor** | Option<**f64**> | Representative ROAS floor for the campaign, bubbled up from the top-spending ad set. Decimal multiplier (2.0 = 2.0x). | [optional]
**promoted_object** | Option<[**models::AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md)> |  | [optional]
**ad_sets** | Option<[**Vec<models::AdTreeAdSet>**](AdTreeAdSet.md)> |  | [optional]
**daily** | Option<[**Vec<models::AdDailyMetrics>**](AdDailyMetrics.md)> | Per-day metric series for this campaign. Present only when `GET /v1/ads/tree` is called with `timeIncrement=1` (any `dailyLevel`). This is the per-campaign daily trend. Summing its additive fields reproduces the campaign `metrics` total, except `reach`: on Meta the range total is de-duplicated, so daily reach does not sum to it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


