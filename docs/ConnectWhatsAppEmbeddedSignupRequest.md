# ConnectWhatsAppEmbeddedSignupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | Authorization code from the FB.login response (authResponse.code) | 
**profile_id** | **String** |  | 
**waba_id** | Option<**String**> | waba_id from the WA_EMBEDDED_SIGNUP message event | [optional]
**phone_number_id** | Option<**String**> | phone_number_id from the WA_EMBEDDED_SIGNUP message event. With wabaId it skips the number picker. | [optional]
**is_coexistence** | Option<**bool**> | Set when the popup ended with the FINISH_WHATSAPP_BUSINESS_APP_ONBOARDING event, so the number stays live in the WhatsApp Business app | [optional]
**expected_phone_number** | Option<**String**> | Rejects the connect when Meta returns a different number | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


