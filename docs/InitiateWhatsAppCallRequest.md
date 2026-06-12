# InitiateWhatsAppCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | **String** | Consumer wa_id (E.164 | 
**action** | Option<**Action**> | Omit to place a call. Set to send the consent prompt instead. (enum: send_call_permission_request) | [optional]
**body_text** | Option<**String**> | Body text shown with the consent prompt (send_call_permission_request only). | [optional]
**forward_to** | Option<**String**> | Per-call destination override. Same accepted shape as the number's stored forwardTo (tel:+E164, sip:..., wss://...).  | [optional]
**record_override** | Option<**bool**> |  | [optional]
**biz_opaque_callback_data** | Option<**String**> | Accepted for forward compatibility. Not currently echoed back in webhook payloads (SIP-first flow does not pass through Meta's Graph API where Meta would echo this).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


