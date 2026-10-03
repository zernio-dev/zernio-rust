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
**optimization_goal** | Option<**String**> | TikTok only, only with `live=true` and only on rows read live. The ad group's `optimization_goal` exactly as TikTok's adgroup/get returns it now (for example ENGAGED_VIEW, ENGAGED_VIEW_FIFTEEN, CLICK, CONVERT). Absent on rows not read live and on other platforms. | [optional]
**billing_event** | Option<**String**> | TikTok only, only with `live=true` and only on rows read live. The ad group's `billing_event` exactly as TikTok's adgroup/get returns it now (for example CPV, CPC, OCPM). | [optional]
**native_settings** | Option<**std::collections::HashMap<String, serde_json::Value>**> | TikTok only, only with `live=true` and only on rows read live. TikTok's adgroup/get record verbatim (snake_case, TikTok's own names and enums): operation_status, optimization_goal, optimization_event, billing_event, bid_type, bid_price, budget, budget_mode, pacing, schedule_type, schedule_start_time, schedule_end_time, dayparting, placement_type, placements, location_ids, age_groups, gender, languages, interest_category_ids, interest_keyword_ids, actions, audience_ids, excluded_audience_ids, operating_systems, frequency, frequency_schedule, smart_audience_enabled, smart_interest_behavior_enabled. schedule_start_time and schedule_end_time are UTC wall clocks (YYYY-MM-DD HH:MM:SS). location_ids holds TikTok's native location ids (GeoNames ids for countries); GET /v1/ads/targeting/search?dimension=geo returns them as `platformId` on country results. Plus advertiser_currency and advertiser_timezone from TikTok's advertiser/info. A field TikTok does not return is absent. | [optional]
**config_read_at** | Option<**String**> | Only with `live=true`. When `nativeSettings` was read from the platform. Null on every row whose native settings were not read now (row past the cap, failed read, or a platform without a native read). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


