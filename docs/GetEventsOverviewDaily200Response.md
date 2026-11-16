# GetEventsOverviewDaily200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | Option<**Period**> |  (enum: today, 7d, 30d) | [optional]
**totals** | Option<[**models::GetEventsOverviewDaily200ResponseTotals**](GetEventsOverviewDaily200ResponseTotals.md)> |  | [optional]
**days** | Option<[**Vec<models::GetEventsOverviewDaily200ResponseDaysInner>**](GetEventsOverviewDaily200ResponseDaysInner.md)> | Every day of the period, oldest first, zero where nothing happened. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


