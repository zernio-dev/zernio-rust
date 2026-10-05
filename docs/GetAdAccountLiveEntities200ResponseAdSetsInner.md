# GetAdAccountLiveEntities200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_ad_set_id** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_status** | Option<**String**> | Meta `effective_status`, for example ACTIVE, PAUSED, CAMPAIGN_PAUSED. | [optional]
**configured_status** | Option<**String**> | Meta `status`: the ad set's own switch. | [optional]
**status** | Option<**String**> | Zernio's normalized status, derived from `platformAdSetStatus`. | [optional]
**budget** | Option<[**models::GetAdAccountLiveEntities200ResponseAdSetsInnerBudget**](GetAdAccountLiveEntities200ResponseAdSetsInnerBudget.md)> |  | [optional]
**daily_budget** | Option<**f64**> | Meta `daily_budget` in whole units of `currency`. | [optional]
**lifetime_budget** | Option<**f64**> | Meta `lifetime_budget` in whole units of `currency`. | [optional]
**budget_remaining** | Option<**f64**> | Meta `budget_remaining` in whole units of `currency`. Null when the ad set has no budget of its own. | [optional]
**bid_strategy** | Option<**String**> | Meta `bid_strategy`. | [optional]
**bid_amount** | Option<**f64**> | Meta `bid_amount` (bid cap or cost target) in whole units of `currency`. Null when the strategy has none. | [optional]
**optimization_goal** | Option<**String**> | Meta `optimization_goal`. | [optional]
**billing_event** | Option<**String**> | Meta `billing_event`. | [optional]
**promoted_object** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta `promoted_object` verbatim (snake_case). | [optional]
**targeting** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta `targeting` verbatim (snake_case), as Meta returns it now. | [optional]
**schedule** | Option<[**models::GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule**](GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


