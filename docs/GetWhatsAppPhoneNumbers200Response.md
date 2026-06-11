# GetWhatsAppPhoneNumbers200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numbers** | Option<[**Vec<models::GetWhatsAppPhoneNumbers200ResponseNumbersInner>**](GetWhatsAppPhoneNumbers200ResponseNumbersInner.md)> |  | [optional]
**connected** | Option<[**Vec<models::GetWhatsAppPhoneNumbers200ResponseConnectedInner>**](GetWhatsAppPhoneNumbers200ResponseConnectedInner.md)> | Connected (bring-your-own) WhatsApp numbers — your own WABA numbers linked via Embedded Signup. Not provisioned or billed by Zernio, so they are not in `numbers`; `accountId` is the social-account id used by the messaging and inbox endpoints. Included only on the default and `status=active` views.  | [optional]
**sandbox** | Option<[**models::GetWhatsAppPhoneNumbers200ResponseSandbox**](GetWhatsAppPhoneNumbers200ResponseSandbox.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


