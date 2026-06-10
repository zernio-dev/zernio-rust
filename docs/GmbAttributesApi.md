# \GmbAttributesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_gmb_attribute_metadata**](GmbAttributesApi.md#get_gmb_attribute_metadata) | **GET** /v1/accounts/{accountId}/gmb-attribute-metadata | Get attribute metadata
[**get_google_business_attributes**](GmbAttributesApi.md#get_google_business_attributes) | **GET** /v1/accounts/{accountId}/gmb-attributes | Get attributes
[**update_google_business_attributes**](GmbAttributesApi.md#update_google_business_attributes) | **PUT** /v1/accounts/{accountId}/gmb-attributes | Update attributes



## get_gmb_attribute_metadata

> models::GetGmbAttributeMetadata200Response get_gmb_attribute_metadata(account_id, location_id, category_name, region_code, language_code, page_size, page_token)
Get attribute metadata

Returns metadata about which Google Business Profile attributes are available for a location or business category. Use this endpoint to discover valid attribute names, value types, and allowed enum values before reading or writing via gmb-attributes.  Two mutually exclusive query modes:  **Location mode**: pass `locationId` (or rely on the account's stored `selectedLocationId`). Google returns attributes valid for that specific location.  **Category mode**: pass `categoryName` (must start with `categories/`) and `regionCode`. Google returns attributes valid for that category across the given region. `languageCode` is optional in category mode.  Both modes support `pageSize` and `pageToken` for pagination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**location_id** | Option<**String**> | GBP location ID (e.g. \"6257659026299438786\"). If omitted, uses the account's stored selectedLocationId. Mutually exclusive with categoryName.  |  |
**category_name** | Option<**String**> | Category resource name, must start with \"categories/\" (e.g. \"categories/gcid:plumber\"). Required together with regionCode. Mutually exclusive with locationId.  |  |
**region_code** | Option<**String**> | BCP-47 region code (e.g. \"US\", \"ES\"). Required when categoryName is provided.  |  |
**language_code** | Option<**String**> | BCP-47 language code for display names (e.g. \"en\", \"es\"). Optional when categoryName is provided. Omitted from the Google call when not supplied.  |  |
**page_size** | Option<**i32**> | Maximum number of attribute metadata items to return. Google defaults to 200. |  |
**page_token** | Option<**String**> | Pagination token from a previous response's nextPageToken field. |  |

### Return type

[**models::GetGmbAttributeMetadata200Response**](getGmbAttributeMetadata_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_attributes

> models::GetGoogleBusinessAttributes200Response get_google_business_attributes(account_id, location_id)
Get attributes

Returns GBP location attributes (amenities, services, accessibility, payment types). Available attributes vary by business category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**location_id** | Option<**String**> | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. |  |

### Return type

[**models::GetGoogleBusinessAttributes200Response**](getGoogleBusinessAttributes_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_business_attributes

> models::UpdateGoogleBusinessAttributes200Response update_google_business_attributes(account_id, update_google_business_attributes_request, location_id)
Update attributes

Updates location attributes (amenities, services, etc.).  The attributeMask specifies which attributes to update (comma-separated). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_google_business_attributes_request** | [**UpdateGoogleBusinessAttributesRequest**](UpdateGoogleBusinessAttributesRequest.md) |  | [required] |
**location_id** | Option<**String**> | Override which location to target. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. |  |

### Return type

[**models::UpdateGoogleBusinessAttributes200Response**](updateGoogleBusinessAttributes_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

