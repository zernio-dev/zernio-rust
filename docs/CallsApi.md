# \CallsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_call**](CallsApi.md#get_call) | **GET** /v1/calls/{id} | Get a call (any channel)
[**get_call_recording**](CallsApi.md#get_call_recording) | **GET** /v1/calls/{id}/recording | Get a call recording (any channel)
[**list_calls**](CallsApi.md#list_calls) | **GET** /v1/calls | List all calls (unified history)



## get_call

> models::GetCall200Response get_call(id)
Get a call (any channel)

Channel-agnostic call detail: works for both WhatsApp and regular phone (PSTN) calls, so any row from `GET /v1/calls` can be opened without branching on `channel`. Returns the full call including transcript segments, with `contactId`/`contactName` set when the counterparty matches a CRM contact. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::GetCall200Response**](getCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_call_recording

> models::GetWhatsAppCallRecording200Response get_call_recording(id, r#as)
Get a call recording (any channel)

Channel-agnostic recording fetch: resolves a fresh, playable MP3 URL for any call regardless of channel (provider-signed URLs expire ~10 minutes after signing, so this re-signs on demand). Default responds `302 Found` redirecting to the fresh URL; pass `as=json` to receive `{ url }` instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**r#as** | Option<**String**> | `json` returns `{ url }` instead of a 302 redirect. |  |

### Return type

[**models::GetWhatsAppCallRecording200Response**](getWhatsAppCallRecording_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_calls

> models::ListCalls200Response list_calls(channel, status, direction, number, search, before, limit)
List all calls (unified history)

Unified call history across ALL of your numbers: both channels (WhatsApp Business Calling + regular phone/PSTN), inbound and outbound, newest first. Unlike `GET /v1/voice/calls` (PSTN-only) and `GET /v1/whatsapp/calls` (one account at a time), this endpoint needs no `accountId` and never requires fanning out one request per number.  Any row can be opened channel-agnostically via `GET /v1/calls/{id}` and `GET /v1/calls/{id}/recording`; no branching on `channel` needed. When the counterparty number matches a CRM contact, `contactId` and `contactName` are set.  Cursor pagination: pass the returned `nextCursor` as `before` to fetch the next page. `nextCursor` is null on the last page. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel** | Option<**String**> |  |  |
**status** | Option<**String**> |  |  |
**direction** | Option<**String**> |  |  |
**number** | Option<**String**> | Exact filter: calls involving this number (typically one of YOUR numbers, to scope history to a single line). E.164, leading + optional. |  |
**search** | Option<**String**> | Free-text match on the from/to numbers. Non-digits are stripped, so partial queries like `302` or `+1 302` work. |  |
**before** | Option<**String**> | Return calls with startedAt strictly before this instant (use the previous page's nextCursor). |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListCalls200Response**](listCalls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

