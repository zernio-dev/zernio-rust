# ListWhatsAppCalls200ResponseCallsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**direction** | Option<**Direction**> |  (enum: inbound, outbound) | [optional]
**from** | Option<**String**> |  | [optional]
**to** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: ringing, answered, ended, failed) | [optional]
**started_at** | Option<**String**> |  | [optional]
**ended_at** | Option<**String**> |  | [optional]
**duration_seconds** | Option<**i32**> |  | [optional]
**end_reason** | Option<**EndReason**> |  (enum: hangup, no_answer, rejected, error) | [optional]
**recording_url** | Option<**String**> |  | [optional]
**billing** | Option<[**models::ListWhatsAppCalls200ResponseCallsInnerBilling**](ListWhatsAppCalls200ResponseCallsInnerBilling.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


