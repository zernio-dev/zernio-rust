# SendInboxMessage429Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **String** |  | 
**r#type** | **Type** | Error class for programmatic handling. (enum: invalid_request_error, authentication_error, permission_error, not_found, rate_limit_error, platform_error, api_error) | 
**code** | **Code** |  (enum: platform_api_error) | 
**param** | Option<**String**> | The request field that caused the error, when applicable. | [optional]
**platform** | **Platform** |  (enum: whatsapp) | 
**platform_error** | Option<[**models::WhatsAppTemplateLookupErrorPlatformError**](WhatsAppTemplateLookupErrorPlatformError.md)> |  | [optional]
**details** | [**models::WhatsAppTemplateLookupErrorDetails**](WhatsAppTemplateLookupErrorDetails.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


