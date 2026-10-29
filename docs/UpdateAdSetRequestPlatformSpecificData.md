# UpdateAdSetRequestPlatformSpecificData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**optimization_goal** | Option<**String**> | Meta ad-set optimization_goal (e.g. OFFSITE_CONVERSIONS, LANDING_PAGE_VIEWS). | [optional]
**billing_event** | Option<**String**> | Meta ad-set billing_event (e.g. IMPRESSIONS, LINK_CLICKS, THRUPLAY). | [optional]
**start_date** | Option<**String**> | Ad set start_time (ISO 8601). A value without an offset (`YYYY-MM-DD`, `YYYY-MM-DD HH:MM:SS` or `YYYY-MM-DDTHH:MM:SS`) is read in the ad account timezone. | [optional]
**end_date** | Option<**String**> | Ad set end_time (ISO 8601). A value without an offset (`YYYY-MM-DD`, `YYYY-MM-DD HH:MM:SS` or `YYYY-MM-DDTHH:MM:SS`) is read in the ad account timezone. | [optional]
**daily_min_spend_target** | Option<**f64**> | Meta `daily_min_spend_target`: the least this ad set should spend per day, in whole currency units of the ad account.  It reserves a share of a CAMPAIGN budget for one ad set, so the campaign must use Advantage campaign budget (CBO). On an ad set that owns its budget (ABO) it returns 409; move the budget to the campaign with `PUT /v1/ads/campaigns/{campaignId}` first.  Meta treats it as a target, not a guarantee, and rejects a combined minimum of a campaign's ad sets above the campaign budget.  Mutually exclusive with `lifetimeMinSpendTarget` (400): the flavour must match the campaign budget type, so a daily budget takes a daily target.  Read it back with `GET /v1/ads/ad-sets/{adSetId}?fields=daily_min_spend_target`.  | [optional]
**lifetime_min_spend_target** | Option<**f64**> | Meta `lifetime_min_spend_target`: the lifetime-budget flavour of `dailyMinSpendTarget`, in whole currency units. Send this one when the campaign budget is a lifetime budget. Same rules and same rejections.  | [optional]
**customer_lifecycle** | Option<[**models::MetaCustomerLifecycle**](MetaCustomerLifecycle.md)> |  | [optional]
**ad_schedule** | Option<[**Vec<models::MetaAdScheduleInner>**](MetaAdScheduleInner.md)> | Replaces the ad set's dayparting (Meta `adset_schedule`, `pacing_type: [\"day_parting\"]`). An empty array removes the schedule (`pacing_type: [\"standard\"]`).  Meta runs a schedule only on a lifetime budget. Before writing anything, Zernio takes `budget.type` from the same request or reads the ad set's budget (or its campaign's under Advantage campaign budget). A daily one is a 400 with `param: platformSpecificData.adSchedule`.  Read it back with `GET /v1/ads/ad-sets/{adSetId}` (`adset_schedule`, `pacing_type`) or as `adSchedule` on `GET /v1/ads/accounts/live`.  | [optional]
**promoted_object** | Option<[**models::UpdateAdSetRequestPlatformSpecificDataPromotedObject**](UpdateAdSetRequestPlatformSpecificDataPromotedObject.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


