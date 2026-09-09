# ConnectWhatsAppEmbeddedSignupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | Authorization code from the WA_EMBEDDED_SIGNUP postMessage | 
**profile_id** | **String** |  | 
**waba_id** | Option<**String**> | WhatsApp Business Account id, when the SDK reported one | [optional]
**phone_number_id** | Option<**String**> |  | [optional]
**is_coexistence** | Option<**bool**> | Number is also live in the WhatsApp Business app | [optional]
**expected_phone_number** | Option<**String**> | Rejects the connect when Meta returns a different number | [optional]
**redirect_url** | Option<**String**> | Hosted signup page only. When present, the response also carries `redirectUrl`, the URL the user should land on, with the outcome mapped exactly like the redirect flow (success params, or `error` and `platform` with the same values). Must be an absolute http(s) URL or a custom app scheme. | [optional]
**echo_connect_token** | Option<**bool**> | Hosted signup page only. Append the connect token to the success redirect, as the redirect flow does for API-key callers. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


