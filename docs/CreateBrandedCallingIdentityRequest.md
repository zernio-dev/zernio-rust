# CreateBrandedCallingIdentityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enterprise_id** | **String** | A business from POST /v1/branded-calling/enterprises. | 
**display_name** | **String** | Shown on the callee's screen. No emoji. | 
**call_reasons** | **Vec<String>** | 1 to 10 reasons you call, each up to 64 characters. Pick from GET /v1/branded-calling/call-reasons to skip manual vetting. | 
**logo_url** | Option<**String**> | HTTPS URL of a PNG, JPEG, WebP or SVG logo. Zernio converts it to the 256x256 BMP the carriers require and hosts it. | [optional]
**authorizer** | [**models::CreateBrandedCallingIdentityRequestAuthorizer**](CreateBrandedCallingIdentityRequestAuthorizer.md) |  | 
**references** | [**models::BrandedCallingReferences**](BrandedCallingReferences.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


