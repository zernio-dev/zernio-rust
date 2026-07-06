# CreatePhoneNumberKycLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**country** | **String** | ISO 3166-1 alpha-2 country code (must be a regulated/KYC country). | 
**branding** | Option<[**models::CreatePhoneNumberKycLinkRequestBranding**](CreatePhoneNumberKycLinkRequestBranding.md)> |  | [optional]
**redirect_url** | Option<**String**> | Where to send the end customer's browser after a successful submit. On completion Zernio appends `kyc=submitted` and `country=<ISO-2>` as query params. When omitted, the hosted page shows a built-in confirmation screen instead.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


