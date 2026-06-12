# \WhatsAppCallingApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**disable_whats_app_calling**](WhatsAppCallingApi.md#disable_whats_app_calling) | **DELETE** /v1/whatsapp/phone-numbers/{id}/calling | Disable calling on a number
[**enable_whats_app_calling**](WhatsAppCallingApi.md#enable_whats_app_calling) | **POST** /v1/whatsapp/phone-numbers/{id}/calling | Enable calling on a number
[**get_whats_app_call**](WhatsAppCallingApi.md#get_whats_app_call) | **GET** /v1/whatsapp/calls/{callId} | Get a single call
[**get_whats_app_call_estimate**](WhatsAppCallingApi.md#get_whats_app_call_estimate) | **GET** /v1/whatsapp/calls/estimate | Estimate per-minute cost for a destination
[**get_whats_app_call_permissions**](WhatsAppCallingApi.md#get_whats_app_call_permissions) | **GET** /v1/whatsapp/call-permissions | Check call permission for a consumer
[**get_whats_app_calling_config**](WhatsAppCallingApi.md#get_whats_app_calling_config) | **GET** /v1/whatsapp/calling | Get calling config for an account
[**initiate_whats_app_call**](WhatsAppCallingApi.md#initiate_whats_app_call) | **POST** /v1/whatsapp/calls | Initiate outbound call
[**list_whats_app_calls**](WhatsAppCallingApi.md#list_whats_app_calls) | **GET** /v1/whatsapp/calls | List call history for an account
[**update_whats_app_calling**](WhatsAppCallingApi.md#update_whats_app_calling) | **PATCH** /v1/whatsapp/phone-numbers/{id}/calling | Update calling config



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


## enable_whats_app_calling

> models::EnableWhatsAppCalling200Response enable_whats_app_calling(id, enable_whats_app_calling_request)
Enable calling on a number

Enable WhatsApp Business Calling on a connected number. Configures Meta calling.status=ENABLED with our Telnyx SIP endpoint, fetches and stores the Meta-issued SIP password (encrypted), and snapshots the customer's forward-to destination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | WhatsAppPhoneNumber Mongo ID | [required] |
**enable_whats_app_calling_request** | [**EnableWhatsAppCallingRequest**](EnableWhatsAppCallingRequest.md) |  | [required] |

### Return type

[**models::EnableWhatsAppCalling200Response**](enableWhatsAppCalling_200_response.md)

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
Estimate per-minute cost for a destination

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
Check call permission for a consumer

Returns the permission state and the list of available actions for a given consumer wa_id (e.g. `start_call`, `send_call_permission_request`). Use this before placing a call to decide whether to prompt for consent first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**to** | **String** | Consumer wa_id (E.164 | [required] |

### Return type

[**models::GetWhatsAppCallPermissions200Response**](getWhatsAppCallPermissions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_calling_config

> models::GetWhatsAppCallingConfig200Response get_whats_app_calling_config(account_id)
Get calling config for an account

Returns the local calling configuration snapshot for the connected WhatsApp account: whether calling is enabled, the forward-to destination URI, recording opt-in state, the WhatsAppPhoneNumber doc id (use as `{id}` on the calling-config write endpoints) and whether SIP digest credentials are stored (the encrypted password itself is never returned). 

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

> models::InitiateWhatsAppCall200Response initiate_whats_app_call(initiate_whats_app_call_request)
Initiate outbound call

Initiates an outbound Business-Initiated Call. The Telnyx-side SIP leg is originated server-side (Option B: SIP-first). Telnyx INVITEs Meta directly over TLS:5061 with the SIP digest credentials we captured at calling-enablement time). No client-side SDP is required; pass only `accountId` and `to`.  To send the consumer the call-consent prompt instead of placing a call, pass `action: \"send_call_permission_request\"` (+ optional `bodyText`). The consumer must tap Allow in WhatsApp before `start_call` is permitted; Meta limits the prompt to 1 per consumer per 24h (2 per 7 days) and requires an open 24h service window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**initiate_whats_app_call_request** | [**InitiateWhatsAppCallRequest**](InitiateWhatsAppCallRequest.md) |  | [required] |

### Return type

[**models::InitiateWhatsAppCall200Response**](initiateWhatsAppCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_calls

> models::ListWhatsAppCalls200Response list_whats_app_calls(account_id, status, direction, since, until, limit)
List call history for an account

Compact history listing for a single connected account. Results are scoped to the resolved SocialAccount; profile-scoped team members cannot read calls on sibling accounts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**direction** | Option<**String**> |  |  |
**since** | Option<**String**> |  |  |
**until** | Option<**String**> |  |  |
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

> update_whats_app_calling(id, update_whats_app_calling_request)
Update calling config

Update fields on an already-enabled number. Only fields present in the body are written; `undefined` leaves the stored value alone, explicit `null` clears a nullable field. No Meta side effect, this only changes local routing state consumed by the Telnyx webhook handler. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_whats_app_calling_request** | [**UpdateWhatsAppCallingRequest**](UpdateWhatsAppCallingRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

