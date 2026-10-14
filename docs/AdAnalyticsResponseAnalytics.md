# AdAnalyticsResponseAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**summary** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**daily** | Option<[**Vec<models::CampaignAnalyticsResponseAnalyticsDailyInner>**](CampaignAnalyticsResponseAnalyticsDailyInner.md)> |  | [optional]
**breakdowns** | Option<[**std::collections::HashMap<String, Vec<serde_json::Value>>**](Vec.md)> | Requested demographic breakdowns, keyed by dimension. Fetched live from the platform per request and never stored, so these rows can carry fields the stored `summary` and `daily` series do not.  LinkedIn rows carry `value` (the pivot URN), `name` (resolved label where LinkedIn provides one), the usual spend/impressions/clicks/ctr/cpc/cpm/engagement figures, plus two reach fields:  - `reach`: the segment's `approximateMemberReach`. - `audiencePenetration`: LinkedIn's own ratio of members reached to the size of   the targeted audience, passed through verbatim.  LinkedIn withholds both below its audience privacy threshold, in which case the keys are ABSENT rather than 0. `audiencePenetration` is available here only: it is not part of the stored metrics series.  TikTok rows are keyed by TikTok's own dimension name (`country_code` for `country`, `platform` for `publisher_platform`). `placement` rows carry the label TikTok Ads Manager shows (`TikTok`, `TikTok Ad Network`, `News Feed App Series`) in `placement` and TikTok's API value (`PLACEMENT_TIKTOK`, `PLACEMENT_PANGLE`, `PLACEMENT_GLOBAL_APP_BUNDLE`) in `placementRaw`; a value without a known label carries the raw value in both.  A requested dimension with no data in the range is an empty array.  | [optional]
**unsupported_breakdowns** | Option<**Vec<String>**> | Requested breakdowns this platform cannot break down by (e.g. region on TikTok, any breakdown on Google). Absent when every requested breakdown is supported. | [optional]
**breakdown_hints** | Option<**std::collections::HashMap<String, String>**> | Guidance for some names in unsupportedBreakdowns, keyed by that name (e.g. placement on Meta points at publisher_platform and platform_position; platform_position on TikTok points at placement). Absent when no unsupported name has a hint. | [optional]
**breakdown_errors** | Option<[**Vec<models::CampaignAnalyticsResponseAnalyticsBreakdownErrorsInner>**](CampaignAnalyticsResponseAnalyticsBreakdownErrorsInner.md)> | TikTok only: breakdowns the platform failed to return (rate limit, permission, rejected query). Each one is an empty array under breakdowns; summary and daily are unaffected. Absent when every breakdown answered. | [optional]
**breakdown_dropped_metrics** | Option<[**std::collections::HashMap<String, Vec<String>>**](Vec.md)> | TikTok only: TikTok metric names TikTok refused for a breakdown, keyed by the requested breakdown (e.g. total_purchase and total_purchase_value have no relation to platform, ac or language). Every row value derived from a refused metric is null in that breakdown (purchaseValue and roas, or the matching actions and actionValues entries), never a number computed without it. Absent when no metric was refused. | [optional]
**breakdowns_range** | Option<[**models::CampaignAnalyticsResponseAnalyticsBreakdownsRange**](CampaignAnalyticsResponseAnalyticsBreakdownsRange.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


