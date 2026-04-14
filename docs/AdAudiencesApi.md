# \AdAudiencesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_users_to_ad_audience**](AdAudiencesApi.md#add_users_to_ad_audience) | **POST** /v1/ads/audiences/{audienceId}/users | Add users to audience
[**create_ad_audience**](AdAudiencesApi.md#create_ad_audience) | **POST** /v1/ads/audiences | Create custom audience
[**delete_ad_audience**](AdAudiencesApi.md#delete_ad_audience) | **DELETE** /v1/ads/audiences/{audienceId} | Delete custom audience
[**get_ad_audience**](AdAudiencesApi.md#get_ad_audience) | **GET** /v1/ads/audiences/{audienceId} | Get audience details
[**list_ad_audiences**](AdAudiencesApi.md#list_ad_audiences) | **GET** /v1/ads/audiences | List custom audiences



## add_users_to_ad_audience

> models::AddUsersToAdAudience200Response add_users_to_ad_audience(audience_id, add_users_to_ad_audience_request)
Add users to audience

Upload user data (emails and/or phone numbers) to a customer_list audience. Data is SHA256-hashed server-side before sending to Meta. Max 10,000 users per request.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** |  | [required] |
**add_users_to_ad_audience_request** | [**AddUsersToAdAudienceRequest**](AddUsersToAdAudienceRequest.md) |  | [required] |

### Return type

[**models::AddUsersToAdAudience200Response**](addUsersToAdAudience_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_audience

> models::CreateAdAudience201Response create_ad_audience(create_ad_audience_request)
Create custom audience

Create a customer list, website retargeting, or lookalike audience on Meta (Facebook/Instagram).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_audience_request** | [**CreateAdAudienceRequest**](CreateAdAudienceRequest.md) |  | [required] |

### Return type

[**models::CreateAdAudience201Response**](createAdAudience_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_audience

> models::DeleteAccountGroup200Response delete_ad_audience(audience_id)
Delete custom audience

Deletes the audience from both Meta and the local database.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_audience

> models::GetAdAudience200Response get_ad_audience(audience_id)
Get audience details

Returns the local audience record and fresh data from Meta (if available).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** |  | [required] |

### Return type

[**models::GetAdAudience200Response**](getAdAudience_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_audiences

> models::ListAdAudiences200Response list_ad_audiences(account_id, ad_account_id, platform)
List custom audiences

Returns custom audiences for the given ad account. Supports Meta, Google, TikTok, and Pinterest.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | [required] |
**ad_account_id** | **String** | Platform ad account ID | [required] |
**platform** | Option<**String**> |  |  |

### Return type

[**models::ListAdAudiences200Response**](listAdAudiences_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

