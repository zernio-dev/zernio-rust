# ListSmsOptOuts200ResponseOptOutsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> |  | [optional]
**opted_out_at** | Option<**String**> |  | [optional]
**keyword** | Option<**String**> | The keyword they sent (e.g. STOP), when the carrier recorded one. | [optional]
**from** | Option<**String**> | Which of your numbers the recipient opted out from. | [optional]
**source** | Option<**Source**> | `inbound_stop` when the recipient texted an opt-out keyword, `api` when recorded with `POST /v1/sms/opt-outs`. Null when unknown. (enum: inbound_stop, api, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


