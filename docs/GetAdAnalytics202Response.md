# GetAdAnalytics202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backfill_pending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 
**ad** | Option<[**models::AdAnalyticsResponseAd**](AdAnalyticsResponseAd.md)> |  | [optional]
**analytics** | Option<[**models::CampaignAnalyticsResponseAnalytics**](CampaignAnalyticsResponseAnalytics.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


