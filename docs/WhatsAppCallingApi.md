# \WhatsAppCallingApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**disable_whats_app_calling**](WhatsAppCallingApi.md#disable_whats_app_calling) | **DELETE** /v1/phone-numbers/{id}/whatsapp/calling | Disable calling on a number
[**disable_whats_app_calling_legacy**](WhatsAppCallingApi.md#disable_whats_app_calling_legacy) | **DELETE** /v1/whatsapp/phone-numbers/{id}/calling | Disable calling on a number
[**enable_whats_app_calling**](WhatsAppCallingApi.md#enable_whats_app_calling) | **POST** /v1/phone-numbers/{id}/whatsapp/calling | Enable calling on a number
[**enable_whats_app_calling_legacy**](WhatsAppCallingApi.md#enable_whats_app_calling_legacy) | **POST** /v1/whatsapp/phone-numbers/{id}/calling | Enable calling on a number
[**get_whats_app_call**](WhatsAppCallingApi.md#get_whats_app_call) | **GET** /v1/whatsapp/calls/{callId} | Get a single call
[**get_whats_app_call_estimate**](WhatsAppCallingApi.md#get_whats_app_call_estimate) | **GET** /v1/whatsapp/calls/estimate | Estimate per-minute cost
[**get_whats_app_call_permissions**](WhatsAppCallingApi.md#get_whats_app_call_permissions) | **GET** /v1/whatsapp/call-permissions | Check call permission
[**get_whats_app_call_recording**](WhatsAppCallingApi.md#get_whats_app_call_recording) | **GET** /v1/whatsapp/calls/{callId}/recording | Get a call recording
[**get_whats_app_calling**](WhatsAppCallingApi.md#get_whats_app_calling) | **GET** /v1/phone-numbers/{id}/whatsapp/calling | Get calling config for a number
[**get_whats_app_calling_config**](WhatsAppCallingApi.md#get_whats_app_calling_config) | **GET** /v1/whatsapp/calling | Get calling config for an account
[**initiate_whats_app_call**](WhatsAppCallingApi.md#initiate_whats_app_call) | **POST** /v1/whatsapp/calls | Initiate outbound call
[**list_whats_app_calls**](WhatsAppCallingApi.md#list_whats_app_calls) | **GET** /v1/whatsapp/calls | List call history for an account
[**update_whats_app_calling**](WhatsAppCallingApi.md#update_whats_app_calling) | **PATCH** /v1/phone-numbers/{id}/whatsapp/calling | Update calling config
[**update_whats_app_calling_legacy**](WhatsAppCallingApi.md#update_whats_app_calling_legacy) | **PATCH** /v1/whatsapp/phone-numbers/{id}/calling | Update calling config



## disable_whats_app_calling

> disable_whats_app_calling(id, account_id)
Disable calling on a number

Disable calling. Sends calling.status=DISABLED to Meta (best-effort) and flips the local `callingEnabled` flag off. forwardTo and SIP creds are preserved so a re-enable does not lose the destination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_whats_app_calling_legacy

> disable_whats_app_calling_legacy(id, account_id)
Disable calling on a number

Deprecated alias of `/v1/phone-numbers/{id}/whatsapp/calling`; same contract. New integrations should use that path.  Disable calling. Sends calling.status=DISABLED to Meta (best-effort) and flips the local `callingEnabled` flag off. forwardTo and SIP creds are preserved so a re-enable does not lose the destination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_whats_app_calling

> models::EnableWhatsAppCallingLegacy200Response enable_whats_app_calling(id, enable_whats_app_calling_legacy_request)
Enable calling on a number

Enable WhatsApp Business Calling on a connected number. Configures Meta calling.status=ENABLED with our Telnyx SIP endpoint, fetches and stores the Meta-issued SIP password (encrypted), and snapshots the customer's forward-to destination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID (from GET /v1/phone-numbers). | [required] |
**enable_whats_app_calling_legacy_request** | [**EnableWhatsAppCallingLegacyRequest**](EnableWhatsAppCallingLegacyRequest.md) |  | [required] |

### Return type

[**models::EnableWhatsAppCallingLegacy200Response**](enableWhatsAppCallingLegacy_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_whats_app_calling_legacy

> models::EnableWhatsAppCallingLegacy200Response enable_whats_app_calling_legacy(id, enable_whats_app_calling_legacy_request)
Enable calling on a number

Deprecated alias of `/v1/phone-numbers/{id}/whatsapp/calling`; same contract. New integrations should use that path.  Enable WhatsApp Business Calling on a connected number. Configures Meta calling.status=ENABLED with our Telnyx SIP endpoint, fetches and stores the Meta-issued SIP password (encrypted), and snapshots the customer's forward-to destination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | WhatsAppPhoneNumber Mongo ID | [required] |
**enable_whats_app_calling_legacy_request** | [**EnableWhatsAppCallingLegacyRequest**](EnableWhatsAppCallingLegacyRequest.md) |  | [required] |

### Return type

[**models::EnableWhatsAppCallingLegacy200Response**](enableWhatsAppCallingLegacy_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_call

> models::GetWhatsAppCall200Response get_whats_app_call(call_id, account_id)
Get a single call

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**call_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::GetWhatsAppCall200Response**](getWhatsAppCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_call_estimate

> models::GetWhatsAppCallEstimate200Response get_whats_app_call_estimate(account_id, to, minutes, recording)
Estimate per-minute cost

Returns a zero-markup estimated cost for an outbound call to the given destination, broken down by Meta + Telnyx + recording line items. Costs are pass-through, no margin applied. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**to** | **String** |  | [required] |
**minutes** | Option<**i32**> |  |  |
**recording** | Option<**bool**> |  |  |

### Return type

[**models::GetWhatsAppCallEstimate200Response**](getWhatsAppCallEstimate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_call_permissions

> models::GetWhatsAppCallPermissions200Response get_whats_app_call_permissions(account_id, to)
Check call permission

Returns the permission state and the list of available actions for a given consumer wa_id (e.g. `start_call`, `send_call_permission_request`). Use this before placing a call to decide whether to prompt for consent first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**to** | **String** | Consumer wa_id (E.164, leading + optional) | [required] |

### Return type

[**models::GetWhatsAppCallPermissions200Response**](getWhatsAppCallPermissions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_call_recording

> models::GetWhatsAppCallRecording200Response get_whats_app_call_recording(call_id, account_id, r#as)
Get a call recording

Resolves a fresh, playable MP3 URL for the call's recording. Provider-signed recording URLs expire ~10 minutes after signing, so the `recordingUrl` stored on the call is usually stale by the time it is played; this endpoint re-signs on demand. Default responds `302 Found` redirecting to the fresh URL (point an `<audio>` element or a link straight at this endpoint); pass `as=json` to receive `{ url }` instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**call_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**r#as** | Option<**String**> | `json` returns `{ url }` instead of a 302 redirect. |  |

### Return type

[**models::GetWhatsAppCallRecording200Response**](getWhatsAppCallRecording_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_calling

> models::GetWhatsAppCalling200Response get_whats_app_calling(id)
Get calling config for a number

The WhatsApp Business Calling configuration of this number, keyed the same way as the POST/PATCH/DELETE below (full read-write on one sub-resource). Encrypted secrets are never returned; only a boolean saying whether a SIP password is stored. The account-scoped read (`GET /v1/whatsapp/calling?accountId=`) remains for callers that only know the social account id, and additionally carries account-level extras (billing eligibility, current-period spend). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID (from GET /v1/phone-numbers). | [required] |

### Return type

[**models::GetWhatsAppCalling200Response**](getWhatsAppCalling_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_calling_config

> models::GetWhatsAppCallingConfig200Response get_whats_app_calling_config(account_id)
Get calling config for an account

Returns the local calling configuration snapshot for the connected WhatsApp account: whether calling is enabled, the forward-to destination URI, recording opt-in state, the phone number record id (use as `{id}` on the read-write calling sub-resource at /v1/phone-numbers/{id}/whatsapp/calling) and whether SIP digest credentials are stored (the encrypted password itself is never returned). Also carries account-level extras (billing eligibility, current-period spend) that the number-keyed GET does not. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppCallingConfig200Response**](getWhatsAppCallingConfig_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## initiate_whats_app_call

> models::InitiateWhatsAppCall200Response initiate_whats_app_call(initiate_whats_app_call_request, idempotency_key)
Initiate outbound call

Initiates an outbound Business-Initiated Call. The Telnyx-side SIP leg is originated server-side (Option B: SIP-first). Telnyx INVITEs Meta directly over TLS:5061 with the SIP digest credentials we captured at calling-enablement time). No client-side SDP is required; pass only `accountId` and `to`.  To send the consumer the call-consent prompt instead of placing a call, pass `action: \"send_call_permission_request\"` (+ optional `bodyText`). The consumer must tap Allow in WhatsApp before `start_call` is permitted; Meta limits the prompt to 1 per consumer per 24h (2 per 7 days) and requires an open 24h service window.  **Idempotency:** send an `Idempotency-Key` header to make retries safe; same key + same body replays the original response instead of dialing (and billing) a second call. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**initiate_whats_app_call_request** | [**InitiateWhatsAppCallRequest**](InitiateWhatsAppCallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes dial retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::InitiateWhatsAppCall200Response**](initiateWhatsAppCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_calls

> models::ListWhatsAppCalls200Response list_whats_app_calls(account_id, status, direction, since, until, before, limit)
List call history for an account

Compact history listing for a single connected account. Results are scoped to the resolved SocialAccount; profile-scoped team members cannot read calls on sibling accounts.  Cursor pagination: pass the returned `nextCursor` as `before` to fetch the next page (same scheme as `GET /v1/calls`). `since`/`until` remain as absolute range filters and combine with the cursor. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**direction** | Option<**String**> |  |  |
**since** | Option<**String**> |  |  |
**until** | Option<**String**> |  |  |
**before** | Option<**String**> | Return calls with startedAt strictly before this instant (use the previous page's nextCursor). |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**models::ListWhatsAppCalls200Response**](listWhatsAppCalls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_calling

> update_whats_app_calling(id, update_whats_app_calling_legacy_request)
Update calling config

Update fields on an already-enabled number. Only fields present in the body are written; `undefined` leaves the stored value alone, explicit `null` clears a nullable field. No Meta side effect, this only changes local routing state consumed by the Telnyx webhook handler. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_whats_app_calling_legacy_request** | [**UpdateWhatsAppCallingLegacyRequest**](UpdateWhatsAppCallingLegacyRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_calling_legacy

> update_whats_app_calling_legacy(id, update_whats_app_calling_legacy_request)
Update calling config

Deprecated alias of `/v1/phone-numbers/{id}/whatsapp/calling`; same contract. New integrations should use that path.  Update fields on an already-enabled number. Only fields present in the body are written; `undefined` leaves the stored value alone, explicit `null` clears a nullable field. No Meta side effect, this only changes local routing state consumed by the Telnyx webhook handler. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_whats_app_calling_legacy_request** | [**UpdateWhatsAppCallingLegacyRequest**](UpdateWhatsAppCallingLegacyRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

