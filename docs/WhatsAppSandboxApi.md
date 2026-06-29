# \WhatsAppSandboxApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_whats_app_sandbox_session**](WhatsAppSandboxApi.md#create_whats_app_sandbox_session) | **POST** /v1/whatsapp/sandbox/sessions | Start a sandbox activation
[**delete_whats_app_sandbox_session**](WhatsAppSandboxApi.md#delete_whats_app_sandbox_session) | **DELETE** /v1/whatsapp/sandbox/sessions/{sessionId} | Revoke a sandbox session
[**list_whats_app_sandbox_sessions**](WhatsAppSandboxApi.md#list_whats_app_sandbox_sessions) | **GET** /v1/whatsapp/sandbox/sessions | List your sandbox sessions



## create_whats_app_sandbox_session

> models::CreateWhatsAppSandboxSession200Response create_whats_app_sandbox_session(create_whats_app_sandbox_session_request)
Start a sandbox activation

Creates (or refreshes) a pending sandbox session for the given phone and immediately fires the verified sandbox template from the shared sandbox number to that phone. The session activates when the phone owner replies to that WhatsApp message — the reply itself is proof of ownership.  One phone per user: if the caller already has a non-expired session for a DIFFERENT phone, the request is rejected with `invalid_field_value` (the message names the existing phone so it can be revoked first). Re-creating a session for the SAME phone is idempotent and refreshes the verification template.  If Meta rejects the template send (not a WhatsApp number, paused WABA, token issue), the pending row is rolled back and the Meta error message is returned in `error` so the caller knows why. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_sandbox_session_request** | [**CreateWhatsAppSandboxSessionRequest**](CreateWhatsAppSandboxSessionRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppSandboxSession200Response**](createWhatsAppSandboxSession_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_sandbox_session

> models::UpdateYoutubeDefaultPlaylist200Response delete_whats_app_sandbox_session(session_id)
Revoke a sandbox session

Hard-deletes the session. The user loses the ability to send to that phone via the sandbox until they re-activate it. Existing conversations and messages already exchanged with that phone are untouched — revocation only blocks FUTURE sends.  Sessions belonging to other users cannot be revoked; the response is the same 400 as \"session not found\" so existence isn't leaked. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**session_id** | **String** | The session id returned by POST /v1/whatsapp/sandbox/sessions. | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_sandbox_sessions

> models::ListWhatsAppSandboxSessions200Response list_whats_app_sandbox_sessions()
List your sandbox sessions

Returns all of the authenticated user's non-expired sandbox sessions (pending + active) plus the sandbox phone number. In practice there is at most one session per user since the sandbox is one-phone-per-user; the array shape is preserved for forward compatibility. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListWhatsAppSandboxSessions200Response**](listWhatsAppSandboxSessions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

