# ListPhoneNumbers200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numbers** | Option<[**Vec<models::ListPhoneNumbers200ResponseNumbersInner>**](ListPhoneNumbers200ResponseNumbersInner.md)> |  | [optional]
**connected** | Option<[**Vec<models::ListPhoneNumbers200ResponseConnectedInner>**](ListPhoneNumbers200ResponseConnectedInner.md)> | Connected (bring-your-own) WhatsApp numbers: your own WABA numbers linked via Embedded Signup. Not provisioned or billed by Zernio, so they are not in `numbers`; `accountId` is the social-account id used by the messaging and inbox endpoints. Included only on the default and `status=active` views.  | [optional]
**imessage** | Option<[**Vec<models::ImessageSenderLifecycle>**](ImessageSenderLifecycle.md)> | iMessage phone senders (see /v1/imessage/senders/order). Hosted by the iMessage provider, not on your Telnyx numbers: SMS and Calls can never be enabled on them, and they bill as iMessage senders. `handle` is null until the carrier assigns the number at activation. Included only on the default and `status=active` views.  | [optional]
**sandbox** | Option<[**models::ListPhoneNumbers200ResponseSandbox**](ListPhoneNumbers200ResponseSandbox.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


