# SendEmailDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**send_at** | Option<**String**> | Send later, 1 minute to 30 days ahead: answers 202 with a `ScheduledEmail`. The draft stays editable in the mailbox and goes out as it stands then. Cancelling with `DELETE /v1/email/messages/scheduled/{scheduleId}` keeps the draft. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


