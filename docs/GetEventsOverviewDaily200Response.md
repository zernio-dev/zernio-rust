# GetEventsOverviewDaily200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | Option<**Period**> |  (enum: today, 7d, 30d, 90d) | [optional]
**totals** | Option<[**models::GetEventsOverviewDaily200ResponseTotals**](GetEventsOverviewDaily200ResponseTotals.md)> |  | [optional]
**days** | Option<[**Vec<models::GetEventsOverviewDaily200ResponseDaysInner>**](GetEventsOverviewDaily200ResponseDaysInner.md)> | Every day of the period, oldest first, zero where nothing happened. | [optional]
**event_names** | Option<**Vec<String>**> | The event names stored in the period, most events first. | [optional]
**platforms** | Option<[**Vec<models::GetEventsOverviewDaily200ResponsePlatformsInner>**](GetEventsOverviewDaily200ResponsePlatformsInner.md)> | Each platform events were sent to in the period, most sends first. | [optional]
**pixel_missed** | Option<[**Vec<models::GetEventsOverviewDaily200ResponsePixelMissedInner>**](GetEventsOverviewDaily200ResponsePixelMissedInner.md)> | For each platform sent to in the period, the website conversions of people who allowed ad cookies (bots left out) and how many its browser pixel missed, which Zernio sent from its server. Most missed first; `null` without a tracked website in scope. | [optional]
**breakdown** | Option<[**models::GetEventsOverviewDaily200ResponseBreakdown**](GetEventsOverviewDaily200ResponseBreakdown.md)> |  | [optional]
**previous** | Option<[**models::GetEventsOverviewDaily200ResponsePrevious**](GetEventsOverviewDaily200ResponsePrevious.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


