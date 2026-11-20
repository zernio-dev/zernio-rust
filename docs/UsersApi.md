# \UsersApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_current_user**](UsersApi.md#get_current_user) | **GET** /v1/users/me | Get the current user
[**get_user**](UsersApi.md#get_user) | **GET** /v1/users/{userId} | Get user
[**list_users**](UsersApi.md#list_users) | **GET** /v1/users | List users
[**remove_user**](UsersApi.md#remove_user) | **DELETE** /v1/users/{userId} | Remove member



## get_current_user

> models::GetCurrentUser200Response get_current_user()
Get the current user

Returns the user the credential belongs to, in the same shape as one element of `users` in GET /v1/users, plus the workspace the credential acts in. Use it to check who an API key belongs to without listing every user.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetCurrentUser200Response**](getCurrentUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_user

> models::GetUser200Response get_user(user_id)
Get user

Returns a single user's details by ID, including name, email, and role.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**models::GetUser200Response**](getUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_users

> models::ListUsers200Response list_users()
List users

Returns all users in the team including roles and profile access. Also returns the currentUserId of the caller.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListUsers200Response**](listUsers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_user

> models::RemoveUser200Response remove_user(user_id)
Remove member

Removes a member from your team. The member keeps their own login and what they had before joining. What they added as a member passes to the team owner.  API keys the member used in the last 7 days pass to the owner and expire within 24 hours, and their other keys in the team are revoked.  Requires the owner or an admin, and a key that is not restricted. You cannot remove yourself.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**models::RemoveUser200Response**](removeUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

