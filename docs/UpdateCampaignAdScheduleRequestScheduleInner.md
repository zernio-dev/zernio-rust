# UpdateCampaignAdScheduleRequestScheduleInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day_of_week** | **DayOfWeek** |  (enum: MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY) | 
**start_hour** | **i32** |  | 
**start_minute** | Option<**StartMinute**> | Quarter-hours only. (enum: 0, 15, 30, 45) | [optional][default to Variant0]
**end_hour** | **i32** | 24 means midnight at the end of the day. | 
**end_minute** | Option<**EndMinute**> | Quarter-hours only. Must be 0 when endHour is 24. (enum: 0, 15, 30, 45) | [optional][default to Variant0]
**bid_modifier** | Option<**f64**> | Bid adjustment for this window. Null runs it at the campaign bid. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


