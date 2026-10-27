# MetaAdScheduleInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day_of_week** | **DayOfWeek** |  (enum: MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY) | 
**start_hour** | **i32** |  | 
**end_hour** | **i32** | Must be after startHour. 24 is midnight at the end of the day. | 
**timezone_type** | Option<**TimezoneType**> | Meta `timezone_type`: USER runs the hours in each viewer's time zone, ADVERTISER in the ad account time zone. (enum: USER, ADVERTISER) | [optional][default to User]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


