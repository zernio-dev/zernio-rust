# GetCampaignAdSchedule200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**campaign_id** | Option<**String**> |  | [optional]
**schedule** | Option<[**Vec<models::AdScheduleWindow>**](AdScheduleWindow.md)> |  | [optional]
**serves_around_the_clock** | Option<**bool**> | True when the campaign carries no ad schedule at all, so it can serve at any time. | [optional]
**cached_at** | Option<**String**> |  | [optional]
**stale** | Option<**bool**> | True when a quota-exhausted read served the last-good copy. | [optional]
**performance** | Option<[**models::GetCampaignAdSchedule200ResponsePerformance**](GetCampaignAdSchedule200ResponsePerformance.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


