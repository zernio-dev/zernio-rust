# GetWhatsAppCallingConfig200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number_doc_id** | Option<**String**> | WhatsAppPhoneNumber Mongo ID (use on /v1/whatsapp/phone-numbers/{id}/calling) | [optional]
**phone_number** | Option<**String**> |  | [optional]
**calling_enabled** | Option<**bool**> |  | [optional]
**forward_to** | Option<**String**> | tel:+E164 / sip:... / wss://... destination | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**sip_auth_username** | Option<**String**> |  | [optional]
**sip_auth_password_configured** | Option<**bool**> | True when a SIP digest password is stored. The plaintext is never returned. | [optional]
**call_icon_countries** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


