# CreatePhoneNumberKycLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**country** | **String** | ISO 3166-1 alpha-2 country code (must be a regulated/KYC country). | 
**area_code** | Option<**String**> | Area code (NDC) the eventual number must be in. Hard constraint carried by the link; the end customer filling the form makes no area choice. Options come from GET /v1/phone-numbers/availability (areaOptions). | [optional]
**language** | Option<**Language**> | Language of the hosted page: its copy, the carrier requirement texts (translated once per country and cached), the pre-submit review notes and the status emails to the end customer. Omitted: the browser language of the end customer, falling back to English. The end customer can also switch with `?lang=` on the page. (enum: en, es, pt-BR) | [optional]
**branding** | Option<[**models::CreatePhoneNumberKycLinkRequestBranding**](CreatePhoneNumberKycLinkRequestBranding.md)> |  | [optional]
**redirect_url** | Option<**String**> | Where to send the end customer's browser after a successful submit. On completion Zernio appends `kyc=submitted` and `country=<ISO-2>` as query params. When omitted, the hosted page shows a built-in confirmation screen instead.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


