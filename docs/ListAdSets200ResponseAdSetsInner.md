# ListAdSets200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_ad_set_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**platform_ad_set_status** | Option<**String**> | Raw platform ad set status. On TikTok the ad group's own switch `operation_status` (ENABLE / DISABLE), independent of its campaign. | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**budget** | Option<[**models::ListAdSets200ResponseAdSetsInnerBudget**](ListAdSets200ResponseAdSetsInnerBudget.md)> |  | [optional]
**schedule** | Option<[**models::ListAdSets200ResponseAdSetsInnerSchedule**](ListAdSets200ResponseAdSetsInnerSchedule.md)> |  | [optional]
**targeting** | Option<[**models::ListAdSets200ResponseAdSetsInnerTargeting**](ListAdSets200ResponseAdSetsInnerTargeting.md)> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**platform_created_at** | Option<**String**> |  | [optional]
**status_read_at** | Option<**String**> | Only with `live=true`. When `platformAdSetStatus` was read from the platform; null when this row was not read live. | [optional]
**optimization_goal** | Option<**String**> | The ad set's optimization goal as last synced, in the platform's own enum (Meta `optimization_goal`, for example OFFSITE_CONVERSIONS or LINK_CLICKS; TikTok `optimization_goal`; Pinterest the conversion event of `optimization_goal_metadata`, for example CHECKOUT; X the line item `goal`; OpenAI the campaign `bidding_type`). Always null on Google, which has no per-ad-group optimization goal. On TikTok with `live=true`, rows read live carry the ad group's `optimization_goal` exactly as TikTok's adgroup/get returns it now (for example ENGAGED_VIEW, ENGAGED_VIEW_FIFTEEN, CLICK, CONVERT). | [optional]
**billing_event** | Option<**String**> | The ad set's billing event as last synced, in the platform's own enum (Meta `billing_event`, TikTok `billing_event`, Pinterest `billable_event`, X `pay_by`, OpenAI `bidding_config.billing_event_type`). Always null on Google, which reports none per ad group. On TikTok with `live=true`, rows read live carry the ad group's `billing_event` exactly as TikTok's adgroup/get returns it now (for example CPV, CPC, OCPM). | [optional]
**bid_strategy** | Option<**String**> | The bid strategy as last synced, in Meta's vocabulary (LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) on every platform that has an equivalent. On Meta under a campaign budget this is the campaign's strategy. TikTok maps bid_type / deep_bid_type, Pinterest AUTOMATIC_BID / MAX_BID / TARGET_AVG, X AUTO / MAX / TARGET, OpenAI Maximize Results / a max bid. Google bids at the campaign, so an ad group carries its campaign's strategy; one without a Meta equivalent (MANUAL_CPC, TARGET_IMPRESSION_SHARE, or a portfolio strategy's type such as TARGET_CPA) keeps Google's own name. Null on LinkedIn. | [optional]
**bid_amount** | Option<**f64**> | Bid cap or cost target in whole units of `currency`, as last synced. Null when the strategy has none (automatic bidding, ROAS targets, a Google portfolio strategy). On Google a campaign target CPA, a Maximize clicks ceiling, the ad group's own target CPA override, or its CPC bid under MANUAL_CPC. | [optional]
**promoted_object** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta only. The ad set's `promoted_object` verbatim (snake_case, for example pixel_id + custom_event_type, page_id, application_id), as last synced from its most recent ad. Null on other platforms and on an ad set with no ad yet; GET /v1/ads/accounts/live reads it live for every ad set. | [optional]
**native_settings** | Option<**std::collections::HashMap<String, serde_json::Value>**> | TikTok only, only with `live=true` and only on rows read live. TikTok's adgroup/get record verbatim (snake_case, TikTok's own names and enums): operation_status, optimization_goal, optimization_event, billing_event, bid_type, bid_price, budget, budget_mode, pacing, schedule_type, schedule_start_time, schedule_end_time, dayparting, placement_type, placements, location_ids, age_groups, gender, languages, interest_category_ids, interest_keyword_ids, actions, audience_ids, excluded_audience_ids, operating_systems, frequency, frequency_schedule, smart_audience_enabled, smart_interest_behavior_enabled. schedule_start_time and schedule_end_time are UTC wall clocks (YYYY-MM-DD HH:MM:SS). location_ids holds TikTok's native location ids (GeoNames ids for countries); GET /v1/ads/targeting/search?dimension=geo returns them as `platformId` on country results. Plus advertiser_currency and advertiser_timezone from TikTok's advertiser/info. A field TikTok does not return is absent. | [optional]
**config_read_at** | Option<**String**> | Only with `live=true`. When `nativeSettings` was read from the platform. Null on every row whose native settings were not read now (row past the cap, failed read, or a platform without a native read). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


