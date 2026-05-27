# \WhatsAppTemplatesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_whats_app_library_template**](WhatsAppTemplatesApi.md#get_whats_app_library_template) | **GET** /v1/whatsapp/template-library | Look up a library template



## get_whats_app_library_template

> models::GetWhatsAppLibraryTemplate200Response get_whats_app_library_template(account_id, name)
Look up a library template

Look up a single pre-approved Template Library template by its exact name, to introspect its structure before importing it. Most importantly it returns the template's `buttons`: a library template with `URL` / `PHONE_NUMBER` buttons must be created with a matching `library_template_button_inputs` array (see Create Template), or Meta rejects it. Use this to discover which inputs to collect. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**name** | **String** | Exact library template name | [required] |

### Return type

[**models::GetWhatsAppLibraryTemplate200Response**](getWhatsAppLibraryTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

