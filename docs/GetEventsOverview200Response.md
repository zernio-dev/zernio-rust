# GetEventsOverview200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**today** | Option<[**models::GetEventsOverview200ResponseToday**](GetEventsOverview200ResponseToday.md)> |  | [optional]
**platforms** | Option<[**Vec<models::GetEventsOverview200ResponsePlatformsInner>**](GetEventsOverview200ResponsePlatformsInner.md)> | One entry per forwarding rule of the profile. | [optional]
**sources** | Option<[**Vec<models::GetEventsOverview200ResponseSourcesInner>**](GetEventsOverview200ResponseSourcesInner.md)> | Each source that stored an event in the last 30 days, most recent first. | [optional]
**website** | Option<[**models::GetEventsOverview200ResponseWebsite**](GetEventsOverview200ResponseWebsite.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


