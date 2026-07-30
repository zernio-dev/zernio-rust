# EnableWhatsAppCallingLegacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**forward_to** | **String** | tel:+E164 / sip:... / wss://... destination | 
**sip_auth_username** | Option<**String**> |  | [optional]
**sip_auth_password** | Option<**String**> | Stored encrypted, never returned by any endpoint. | [optional]
**recording_enabled** | Option<**bool**> |  | [optional][default to false]
**call_icon_countries** | Option<**Vec<String>**> |  | [optional]
**max_call_duration_seconds** | Option<**i32**> | Hard cap (seconds) on a forwarded call; the carrier hangs up both legs when it fires. Safety valve against dead-air billing when a destination hangs up but the signal is lost. | [optional]
**forward_caller_id** | Option<**ForwardCallerId**> | Caller ID presented to the forward destination. caller = the WhatsApp user's number (sip: destinations only; ignored on tel: forwards). Fixes AI-agent trunks that reject seeing the business number call itself. (enum: business, caller) | [optional][default to Business]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


