# GetCampaignAdSchedule200ResponsePerformance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**window_days** | Option<**i32**> | The trailing window used, or null when an explicit fromDate/toDate range was given. | [optional]
**by_day_of_week** | Option<[**Vec<models::GetCampaignAdSchedule200ResponsePerformanceByDayOfWeekInner>**](GetCampaignAdSchedule200ResponsePerformanceByDayOfWeekInner.md)> | One entry per day that delivered, Monday first. | [optional]
**by_hour** | Option<[**Vec<models::GetCampaignAdSchedule200ResponsePerformanceByHourInner>**](GetCampaignAdSchedule200ResponsePerformanceByHourInner.md)> | One entry per hour that delivered, 0-23 in the account time zone. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


