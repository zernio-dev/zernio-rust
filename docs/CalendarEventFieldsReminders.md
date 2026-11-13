# CalendarEventFieldsReminders

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use_default** | Option<**bool**> | Use the calendar's default reminders. Ignored when `overrides` has entries. | [optional]
**overrides** | Option<[**Vec<models::CalendarEventFieldsRemindersOverridesInner>**](CalendarEventFieldsRemindersOverridesInner.md)> | Google takes up to 5 overrides, `popup` or `email`. Outlook keeps one popup reminder (the first override), and an `email` override answers 400 `reminder_method_unsupported` on a Microsoft account. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


