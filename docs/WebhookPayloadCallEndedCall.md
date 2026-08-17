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
**hangup_cause** | Option<**String**> | Raw carrier hangup cause behind endReason (e.g. normal_clearing, call_rejected, not_found). Null when the carrier reported none. | [optional]
**sip_hangup_cause** | Option<**String**> | SIP response code that ended the call when SIP-signalled (e.g. '403', '486', '603'). endReason collapses all three to 'rejected', so this is what separates a refused destination from a busy line. Null on non-SIP legs. | [optional]
**recording_url** | Option<**String**> |  | [optional]
**recording_expires_at** | Option<**String**> |  | [optional]
**billing** | Option<[**models::WebhookPayloadCallEndedCallBilling**](WebhookPayloadCallEndedCallBilling.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


