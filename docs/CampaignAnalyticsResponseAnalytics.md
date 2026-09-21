# CampaignAnalyticsResponseAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**summary** | Option<[**models::CampaignAnalyticsResponseAnalyticsSummary**](CampaignAnalyticsResponseAnalyticsSummary.md)> |  | [optional]
**impression_share_cache** | Option<[**models::CampaignAnalyticsResponseAnalyticsImpressionShareCache**](CampaignAnalyticsResponseAnalyticsImpressionShareCache.md)> |  | [optional]
**daily** | Option<[**Vec<models::CampaignAnalyticsResponseAnalyticsDailyInner>**](CampaignAnalyticsResponseAnalyticsDailyInner.md)> |  | [optional]
**breakdowns** | Option<[**std::collections::HashMap<String, Vec<serde_json::Value>>**](Vec.md)> | Requested demographic breakdowns, keyed by dimension. Fetched live from the platform per request and never stored, so these rows can carry fields the stored `summary` and `daily` series do not.  LinkedIn rows carry `value` (the pivot URN), `name` (resolved label where LinkedIn provides one), the usual spend/impressions/clicks/ctr/cpc/cpm/engagement figures, plus two reach fields:  - `reach`: the segment's `approximateMemberReach`. - `audiencePenetration`: LinkedIn's own ratio of members reached to the size of   the targeted audience, passed through verbatim.  LinkedIn withholds both below its audience privacy threshold, in which case the keys are ABSENT rather than 0. `audiencePenetration` is available here only: it is not part of the stored metrics series.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


