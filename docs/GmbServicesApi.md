# \GmbServicesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_services**](GmbServicesApi.md#get_google_business_services) | **GET** /v1/accounts/{accountId}/gmb-services | Get services
[**update_google_business_services**](GmbServicesApi.md#update_google_business_services) | **PUT** /v1/accounts/{accountId}/gmb-services | Replace services



## get_google_business_services

> models::GetGoogleBusinessServices200Response get_google_business_services(account_id, location_id)
Get services

Gets the services offered by a Google Business Profile location. Returns an array of service items (structured or free-form with optional price). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**location_id** | Option<**String**> | Override which location to query. If omitted, uses the account's selected location. |  |

### Return type

[**models::GetGoogleBusinessServices200Response**](getGoogleBusinessServices_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_business_services

> models::UpdateGoogleBusinessServices200Response update_google_business_services(account_id, update_google_business_services_request, location_id)
Replace services

Replaces the entire service list for a location. Google's API requires full replacement; individual item updates are not supported. Each service can be structured (using a predefined serviceTypeId) or free-form (custom label). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_google_business_services_request** | [**UpdateGoogleBusinessServicesRequest**](UpdateGoogleBusinessServicesRequest.md) |  | [required] |
**location_id** | Option<**String**> | Override which location to target. If omitted, uses the account's selected location. |  |

### Return type

[**models::UpdateGoogleBusinessServices200Response**](updateGoogleBusinessServices_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

