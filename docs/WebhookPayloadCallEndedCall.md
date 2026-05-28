# WebhookPayloadCallEndedCall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**meta_call_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**phone_number_id** | Option<**String**> |  | [optional]
**direction** | Option<**Direction**> |  (enum: inbound, outbound) | [optional]
**from** | Option<**String**> |  | [optional]
**to** | Option<**String**> |  | [optional]
**started_at** | Option<**String**> |  | [optional]
**ended_at** | Option<**String**> |  | [optional]
**duration_seconds** | Option<**i32**> |  | [optional]
**end_reason** | Option<**EndReason**> |  (enum: hangup, no_answer, rejected, error) | [optional]
**recording_url** | Option<**String**> |  | [optional]
**recording_expires_at** | Option<**String**> |  | [optional]
**billing** | Option<[**models::WebhookPayloadCallEndedCallBilling**](WebhookPayloadCallEndedCallBilling.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


