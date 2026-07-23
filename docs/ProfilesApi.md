# \ProfilesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_profile**](ProfilesApi.md#create_profile) | **POST** /v1/profiles | Create profile
[**delete_profile**](ProfilesApi.md#delete_profile) | **DELETE** /v1/profiles/{profileId} | Delete profile
[**get_profile**](ProfilesApi.md#get_profile) | **GET** /v1/profiles/{profileId} | Get profile
[**list_profiles**](ProfilesApi.md#list_profiles) | **GET** /v1/profiles | List profiles
[**update_profile**](ProfilesApi.md#update_profile) | **PUT** /v1/profiles/{profileId} | Update profile



## create_profile

> models::ProfileCreateResponse create_profile(create_profile_request, idempotency_key)
Create profile

Creates a new profile with a name, optional description, and color. Names are unique per workspace: a duplicate returns a 409 whose details.existingProfileId carries the id of the existing profile. Send an Idempotency-Key header to make retries safe: a retried create with the same key and body replays the original 201 (same _id) instead of conflicting.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_profile_request** | [**CreateProfileRequest**](CreateProfileRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes create retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::ProfileCreateResponse**](ProfileCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_profile

> models::ProfileDeleteResponse delete_profile(profile_id)
Delete profile

Permanently deletes a profile. Active connected accounts block deletion (returns 400) - disconnect them first. Any remaining disconnected accounts and provisioned WhatsApp numbers are moved to another of your profiles (a new one is created only if needed), never deleted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

[**models::ProfileDeleteResponse**](ProfileDeleteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_profile

> models::ProfileGetResponse get_profile(profile_id)
Get profile

Returns a single profile by ID, including its name, color, and default status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

[**models::ProfileGetResponse**](ProfileGetResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_profiles

> models::ProfilesListResponse list_profiles(include_over_limit, name, limit, skip)
List profiles

Returns profiles sorted default-first, then by creation date. Filter with name (exact match) and paginate with limit/skip; without those params the full list is returned unchanged. Use includeOverLimit=true to include profiles that exceed the plan limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include_over_limit** | Option<**bool**> | When true, includes over-limit profiles (marked with isOverLimit: true). |  |[default to false]
**name** | Option<**String**> | Exact-match filter on the profile name. Useful to recover a profile id after an ambiguous create (timeout followed by a 409 on retry). |  |
**limit** | Option<**i32**> | Page size. When limit or skip is present, the response includes total and skip (and echoes limit). |  |
**skip** | Option<**i32**> | Number of profiles to skip, applied after sorting and filtering. |  |

### Return type

[**models::ProfilesListResponse**](ProfilesListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_profile

> models::ProfileUpdateResponse update_profile(profile_id, update_profile_request)
Update profile

Updates a profile's name, description, color, or default status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  | [required] |

### Return type

[**models::ProfileUpdateResponse**](ProfileUpdateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

