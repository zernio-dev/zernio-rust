# WebhookPayloadCalendarEventCalendarEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**change_type** | Option<**ChangeType**> |  (enum: created, updated, deleted) | [optional]
**calendar_id** | Option<**String**> | The calendar holding the event, to pass as `calendarId` when reading it: `primary` for the user's main calendar, else the Google calendar id. Null when it is not known, as for a deleted Outlook event. | [optional]
**master_event_id** | Option<**String**> | The series this event belongs to, when it is an occurrence or exception. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


