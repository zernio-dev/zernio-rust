# \ConnectedAppsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_connected_apps**](ConnectedAppsApi.md#list_connected_apps) | **GET** /v1/me/connected-apps | List connected apps
[**revoke_connected_app**](ConnectedAppsApi.md#revoke_connected_app) | **DELETE** /v1/me/connected-apps/{clientId} | Revoke connected app



## list_connected_apps

> models::ListConnectedApps200Response list_connected_apps()
List connected apps

Returns the OAuth clients (AI assistants and MCP connectors) the authenticated user has authorized and that still hold a live token.  Requires a session or a full-scope API key. A profile-scoped API key or an OAuth access token is rejected with 403: an app must not be able to enumerate its sibling authorizations. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListConnectedApps200Response**](listConnectedApps_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_connected_app

> models::RevokeConnectedApp200Response revoke_connected_app(client_id)
Revoke connected app

Ends an app's access: invalidates the client's pending authorization codes and revokes every live token it holds for the authenticated user. Takes effect on the app's next request.  Idempotent while the authorization is still on record: revoking an app that was already revoked returns 200 with `revokedTokens: 0`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**client_id** | **String** | OAuth client id, as returned by GET /v1/me/connected-apps. | [required] |

### Return type

[**models::RevokeConnectedApp200Response**](revokeConnectedApp_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

