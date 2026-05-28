# WebhookPayloadCallReceivedCall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Internal Zernio Call doc id | [optional]
**meta_call_id** | Option<**String**> | Meta wacid.* call id when known | [optional]
**account_id** | Option<**String**> |  | [optional]
**phone_number_id** | Option<**String**> | Meta phone_number_id | [optional]
**direction** | Option<**Direction**> |  (enum: inbound, outbound) | [optional]
**from** | Option<**String**> | Consumer wa_id / E.164 | [optional]
**to** | Option<**String**> | Business number (E.164) | [optional]
**forward_to** | Option<**String**> | Destination snapshot at routing time | [optional]
**contact_id** | Option<**String**> |  | [optional]
**conversation_id** | Option<**String**> |  | [optional]
**started_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


