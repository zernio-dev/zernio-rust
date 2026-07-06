# GetWhatsAppCallingConfig200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number_doc_id** | Option<**String**> | Phone number record ID (use on /v1/phone-numbers/{id}/whatsapp/calling) | [optional]
**phone_number** | Option<**String**> |  | [optional]
**calling_enabled** | Option<**bool**> |  | [optional]
**call_deep_link** | Option<**String**> | Public calling deep link (https://wa.me/call/<number>). Tapping it on a phone starts a WhatsApp voice call to this number. Embed it on websites, emails, or QR codes. Null while calling is disabled; not supported by WhatsApp desktop clients. | [optional]
**forward_to** | Option<**String**> | tel:+E164 / sip:... / wss://... destination | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**sip_auth_username** | Option<**String**> |  | [optional]
**sip_auth_password_configured** | Option<**bool**> | True when a SIP digest password is stored. The plaintext is never returned. | [optional]
**call_icon_countries** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


