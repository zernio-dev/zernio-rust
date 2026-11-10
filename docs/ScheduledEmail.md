# ScheduledEmail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The `scheduleId`. | [optional]
**account_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: scheduled, sending, sent, failed, cancelled) | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**subject** | Option<**String**> | Empty on a reply that keeps the thread subject. `null` once the send finishes under zero content retention. | [optional]
**content_not_retained** | Option<**bool**> | Present and `true` when the email content was dropped under [zero content retention](/security/zero-content-retention). | [optional]
**reply_to_message_id** | Option<**String**> | Set when scheduled through the reply route. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**sent_at** | Option<**String**> |  | [optional]
**sent_message_id** | Option<**String**> | Provider id of the sent message once `status` is sent. | [optional]
**sent_thread_id** | Option<**String**> |  | [optional]
**error** | Option<**String**> | Why a failed send did not leave. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


