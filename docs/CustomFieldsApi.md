# \CustomFieldsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clear_contact_field_value**](CustomFieldsApi.md#clear_contact_field_value) | **DELETE** /v1/contacts/{contactId}/fields/{slug} | Clear custom field value
[**create_custom_field**](CustomFieldsApi.md#create_custom_field) | **POST** /v1/custom-fields | Create custom field
[**delete_custom_field**](CustomFieldsApi.md#delete_custom_field) | **DELETE** /v1/custom-fields/{fieldId} | Delete custom field
[**list_custom_fields**](CustomFieldsApi.md#list_custom_fields) | **GET** /v1/custom-fields | List custom field definitions
[**set_contact_field_value**](CustomFieldsApi.md#set_contact_field_value) | **PUT** /v1/contacts/{contactId}/fields/{slug} | Set custom field value
[**update_custom_field**](CustomFieldsApi.md#update_custom_field) | **PATCH** /v1/custom-fields/{fieldId} | Update custom field



## clear_contact_field_value

> clear_contact_field_value(contact_id, slug)
Clear custom field value

Remove a custom field value from a contact. The field definition is not affected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** |  | [required] |
**slug** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_custom_field

> models::CreateCustomField200Response create_custom_field(create_custom_field_request)
Create custom field

Create a new custom field definition. Supported types are text, number, date, boolean, and select.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_custom_field_request** | [**CreateCustomFieldRequest**](CreateCustomFieldRequest.md) |  | [required] |

### Return type

[**models::CreateCustomField200Response**](createCustomField_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_custom_field

> delete_custom_field(field_id)
Delete custom field

Delete a custom field definition and remove its values from all contacts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**field_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_custom_fields

> models::ListCustomFields200Response list_custom_fields(profile_id)
List custom field definitions

Returns all custom field definitions. Optionally filter by profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |

### Return type

[**models::ListCustomFields200Response**](listCustomFields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_contact_field_value

> set_contact_field_value(contact_id, slug, set_contact_field_value_request)
Set custom field value

Set or overwrite a custom field value on a contact. The value type must match the field definition.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** |  | [required] |
**slug** | **String** |  | [required] |
**set_contact_field_value_request** | [**SetContactFieldValueRequest**](SetContactFieldValueRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_custom_field

> models::UpdateCustomField200Response update_custom_field(field_id, update_custom_field_request)
Update custom field

Update a custom field definition. The field type cannot be changed after creation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**field_id** | **String** |  | [required] |
**update_custom_field_request** | Option<[**UpdateCustomFieldRequest**](UpdateCustomFieldRequest.md)> |  |  |

### Return type

[**models::UpdateCustomField200Response**](updateCustomField_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

