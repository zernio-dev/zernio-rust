# UpdateWhatsAppCallingLegacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**forward_to** | Option<**String**> |  | [optional]
**sip_auth_username** | Option<**String**> |  | [optional]
**sip_auth_password** | Option<**String**> |  | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**call_icon_countries** | Option<**Vec<String>**> |  | [optional]
**max_call_duration_seconds** | Option<**i32**> | Hard cap (seconds) on forwarded calls; null clears the cap. | [optional]
**forward_caller_id** | Option<**ForwardCallerId**> | caller = present the WhatsApp user's number to the forward destination (sip: only). (enum: business, caller) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


