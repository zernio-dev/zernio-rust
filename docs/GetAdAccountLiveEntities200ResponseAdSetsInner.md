# GetAdAccountLiveEntities200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_ad_set_id** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_status** | Option<**String**> | Meta `effective_status` (ACTIVE, PAUSED, CAMPAIGN_PAUSED...) or TikTok `secondary_status` (ADGROUP_STATUS_DELIVERY_OK, ADGROUP_STATUS_AUDIT...). | [optional]
**configured_status** | Option<**String**> | The ad set's own switch: Meta `status`, or TikTok `operation_status` as ACTIVE / PAUSED. | [optional]
**status** | Option<**String**> | Zernio's normalized status, derived from `platformAdSetStatus`. | [optional]
**budget** | Option<[**models::GetAdAccountLiveEntities200ResponseAdSetsInnerBudget**](GetAdAccountLiveEntities200ResponseAdSetsInnerBudget.md)> |  | [optional]
**daily_budget** | Option<**f64**> | Daily budget in whole units of `currency`. | [optional]
**lifetime_budget** | Option<**f64**> | Lifetime budget in whole units of `currency`. | [optional]
**budget_mode** | Option<**String**> | TikTok only: `budget_mode` as TikTok reports it. | [optional]
**budget_remaining** | Option<**f64**> | Meta `budget_remaining` in whole units of `currency`. Null when the ad set has no budget of its own, and always on TikTok. | [optional]
**bid_strategy** | Option<**String**> | Meta `bid_strategy`. On TikTok the ad group's `bid_type` normalized to the same vocabulary (LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, LOWEST_COST_WITH_MIN_ROAS). | [optional]
**bid_amount** | Option<**f64**> | Bid cap or cost target in whole units of `currency` (Meta `bid_amount`; TikTok `bid_price`, else `conversion_bid_price`, else `deep_cpa_bid`). Null when the strategy has none. | [optional]
**optimization_goal** | Option<**String**> | Meta or TikTok `optimization_goal`. | [optional]
**billing_event** | Option<**String**> | Meta or TikTok `billing_event`. | [optional]
**promoted_object** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta `promoted_object` verbatim (snake_case). On TikTok `{ pixelId, customEventType, applicationId, customConversionId }` from `pixel_id`, `optimization_event`, `app_id` and `custom_conversion_id`, only the keys TikTok has set; null when none is. | [optional]
**targeting** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The platform's targeting verbatim (snake_case), as it reports it now: Meta `targeting`, or TikTok's ad group targeting fields (location_ids, age_groups, gender, languages, interest_category_ids, audience_ids, placements...). | [optional]
**schedule** | Option<[**models::GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule**](GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


