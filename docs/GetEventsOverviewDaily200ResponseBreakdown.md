# GetEventsOverviewDaily200ResponseBreakdown

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**events** | Option<[**Vec<models::GetEventsOverviewDaily200ResponseBreakdownEventsInner>**](GetEventsOverviewDaily200ResponseBreakdownEventsInner.md)> | Conversions per event name, most first. | [optional]
**sources** | Option<[**Vec<models::GetEventsOverviewDaily200ResponseBreakdownSourcesInner>**](GetEventsOverviewDaily200ResponseBreakdownSourcesInner.md)> | Conversions per source (`web`, `api`, `stripe`...), most first. | [optional]
**campaigns** | Option<[**Vec<models::GetEventsOverviewDaily200ResponseBreakdownCampaignsInner>**](GetEventsOverviewDaily200ResponseBreakdownCampaignsInner.md)> | The counted conversions (the events that count as campaign results) per matched campaign, most first. Those not tied to one are rows with a `reason`: `not_from_an_ad`, or `campaign_not_found` for an ad Zernio could not match. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


