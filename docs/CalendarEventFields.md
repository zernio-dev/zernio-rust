# CalendarEventFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**description** | Option<**String**> | HTML. | [optional]
**location** | Option<**String**> |  | [optional]
**start** | Option<**String**> | ISO date-time, or a date (`YYYY-MM-DD`) for all-day events. | [optional]
**end** | Option<**String**> | Exclusive for all-day events. | [optional]
**all_day** | Option<**bool**> |  | [optional]
**timezone** | Option<**String**> | IANA zone the event is scheduled in. Default UTC. | [optional]
**participants** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**recurrence** | Option<**Vec<String>**> | RRULE lines, e.g. `RRULE:FREQ=WEEKLY;BYDAY=MO,WE;COUNT=10`. | [optional]
**reminders** | Option<[**models::CalendarEventFieldsReminders**](CalendarEventFieldsReminders.md)> |  | [optional]
**conferencing** | Option<**Conferencing**> |  (enum: google_meet, teams) | [optional]
**busy** | Option<**bool**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: default, public, private) | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


