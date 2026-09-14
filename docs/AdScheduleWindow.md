# AdScheduleWindow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**criterion_id** | Option<**String**> | Google campaign criterion id. Changes whenever the window is rewritten, because Google cannot edit a schedule in place. | [optional]
**resource_name** | Option<**String**> |  | [optional]
**day_of_week** | Option<**DayOfWeek**> |  (enum: MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY) | [optional]
**start_hour** | Option<**i32**> |  | [optional]
**start_minute** | Option<**StartMinute**> |  (enum: 0, 15, 30, 45) | [optional]
**end_hour** | Option<**i32**> | 24 means midnight at the end of the day. | [optional]
**end_minute** | Option<**EndMinute**> |  (enum: 0, 15, 30, 45) | [optional]
**bid_modifier** | Option<**f64**> | Bid adjustment for this window, 0.1-10.0. Null when the window runs at the campaign bid. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


