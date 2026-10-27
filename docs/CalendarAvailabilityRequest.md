# CalendarAvailabilityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**participants** | [**Vec<models::CalendarAvailabilityRequestParticipantsInner>**](CalendarAvailabilityRequestParticipantsInner.md) |  | 
**from** | **String** |  | 
**to** | **String** |  | 
**duration_minutes** | **i32** |  | 
**interval_minutes** | Option<**i32**> |  | [optional][default to 30]
**round_to** | Option<**i32**> | Rounds the first candidate slot up to this many minutes. | [optional]
**buffer** | Option<[**models::CalendarAvailabilityRequestBuffer**](CalendarAvailabilityRequestBuffer.md)> |  | [optional]
**default_open_hours** | Option<[**Vec<models::OpenHoursInner>**](OpenHoursInner.md)> |  | [optional]
**method** | Option<**Method**> |  (enum: collective, max_availability) | [optional][default to Collective]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


