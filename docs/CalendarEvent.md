# CalendarEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft) | [optional]
**calendar_id** | Option<**String**> |  | [optional]
**title** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**location** | Option<**String**> |  | [optional]
**start** | Option<**String**> | ISO date-time with the rendered offset, or a date for all-day events. | [optional]
**end** | Option<**String**> |  | [optional]
**all_day** | Option<**bool**> |  | [optional]
**timezone** | Option<**String**> |  | [optional]
**participants** | Option<[**Vec<models::CalendarEventParticipantsInner>**](CalendarEventParticipantsInner.md)> |  | [optional]
**organizer** | Option<[**models::EmailAddress**](EmailAddress.md)> |  | [optional]
**recurrence** | Option<**Vec<String>**> |  | [optional]
**reminders** | Option<[**models::CalendarEventReminders**](CalendarEventReminders.md)> |  | [optional]
**conferencing** | Option<[**models::CalendarEventConferencing**](CalendarEventConferencing.md)> |  | [optional]
**busy** | Option<**bool**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: default, public, private) | [optional]
**status** | Option<**Status**> |  (enum: confirmed, tentative, cancelled) | [optional]
**ical_uid** | Option<**String**> |  | [optional]
**master_event_id** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> | `series` is a recurring master, `occurrence` one of its instances, and `exception` an instance changed on its own. Google flags an instance as an exception only when it was moved off its slot. (enum: single, series, occurrence, exception) | [optional]
**original_start** | Option<**String**> | For an occurrence or exception, the start it has in the series pattern. | [optional]
**html_link** | Option<**String**> |  | [optional]
**read_only** | Option<**bool**> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


