# GetWhatsAppCalling200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> |  | [optional]
**calling_enabled** | Option<**bool**> |  | [optional]
**call_deep_link** | Option<**String**> | Public calling deep link (https://wa.me/call/<number>). Null while calling is disabled. | [optional]
**forward_to** | Option<**String**> | tel:+E164 / sip:... / wss://... destination | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**sip_auth_username** | Option<**String**> |  | [optional]
**sip_auth_password_configured** | Option<**bool**> | True when a SIP digest password is stored. The plaintext is never returned. | [optional]
**call_icon_countries** | Option<**Vec<String>**> |  | [optional]
**outbound_disabled** | Option<**bool**> | True when the number's country blocks business-initiated (outbound) WhatsApp calling; inbound still works. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


