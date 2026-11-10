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
**timezone** | Option<**String**> | IANA zone the event is scheduled in. Defaults to the calendar's zone on Google and the mailbox's working-hours zone on Microsoft (UTC when Outlook has none, as on personal accounts). A PATCH that moves an event without a zone keeps the zone the event already has. | [optional]
**participants** | Option<[**Vec<models::CalendarEventFieldsParticipantsInner>**](CalendarEventFieldsParticipantsInner.md)> |  | [optional]
**recurrence** | Option<**Vec<String>**> | RRULE lines, e.g. `RRULE:FREQ=WEEKLY;BYDAY=MO,WE;COUNT=10`. Microsoft takes one RRULE plus EXDATE lines; Zernio removes the EXDATE occurrences after saving the series. | [optional]
**reminders** | Option<[**models::CalendarEventFieldsReminders**](CalendarEventFieldsReminders.md)> |  | [optional]
**conferencing** | Option<**Conferencing**> |  (enum: google_meet, teams) | [optional]
**busy** | Option<**bool**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: default, public, private) | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> | String pairs stored on the event and returned on reads, on Google and Microsoft. | [optional]
**notify_participants** | Option<**NotifyParticipants**> | Who gets an invitation or update email for this write: everyone, only guests outside the organizer's domain, or nobody. Google only; Outlook always notifies, so `external` and `none` answer 400 `unsupported_for_provider` on a Microsoft account. (enum: all, external, none) | [optional][default to All]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


