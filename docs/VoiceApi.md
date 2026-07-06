# \VoiceApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_voice_call**](VoiceApi.md#create_voice_call) | **POST** /v1/voice/calls | Place an outbound phone call
[**create_voice_web_session**](VoiceApi.md#create_voice_web_session) | **POST** /v1/voice/calls/web | Mint a browser softphone session
[**dial_voice_web_call**](VoiceApi.md#dial_voice_web_call) | **POST** /v1/voice/calls/web/dial | Dial from the browser softphone
[**disable_voice_on_number**](VoiceApi.md#disable_voice_on_number) | **DELETE** /v1/phone-numbers/{id}/voice | Disable phone calling on a number
[**enable_voice_on_number**](VoiceApi.md#enable_voice_on_number) | **POST** /v1/phone-numbers/{id}/voice | Enable phone calling on a number
[**end_voice_call**](VoiceApi.md#end_voice_call) | **POST** /v1/voice/calls/{id}/end | Hang up a live call
[**get_voice_call**](VoiceApi.md#get_voice_call) | **GET** /v1/voice/calls/{id} | Get a phone call
[**get_voice_call_estimate**](VoiceApi.md#get_voice_call_estimate) | **GET** /v1/voice/calls/estimate | Estimate call cost
[**get_voice_call_recording**](VoiceApi.md#get_voice_call_recording) | **GET** /v1/voice/calls/{id}/recording | Get a call recording
[**list_voice_calls**](VoiceApi.md#list_voice_calls) | **GET** /v1/voice/calls | List phone calls
[**transfer_voice_call**](VoiceApi.md#transfer_voice_call) | **POST** /v1/voice/calls/{id}/transfer | Blind-transfer a live call



## create_voice_call

> models::CreateVoiceCall200Response create_voice_call(create_voice_call_request, idempotency_key)
Place an outbound phone call

Dials `to` FROM one of your voice-enabled numbers and, on answer, bridges the callee to the number's stored forward destination, or to the per-call `forwardTo` override. Destinations can be your own AI voice agent (Vapi/Retell), a phone, or a SIP endpoint. An optional `greeting` is spoken to the callee before the bridge.  The 200 response means the call is dialing; the lifecycle continues asynchronously (track it via `GET /v1/voice/calls/{id}` or the `call.*` webhooks). Outbound calls are capped per rolling hour (429 when hit).  **Idempotency:** send an `Idempotency-Key` header to make retries safe; same key + same body replays the original response instead of dialing (and billing) a second call. The body `idempotencyKey` field predates the header and keeps working; prefer the header. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_voice_call_request** | [**CreateVoiceCallRequest**](CreateVoiceCallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes dial retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::CreateVoiceCall200Response**](createVoiceCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_voice_web_session

> models::CreateVoiceWebSession200Response create_voice_web_session()
Mint a browser softphone session

Step 1 of the two-step browser softphone handshake. Mints a WebRTC session (token + credential) the browser registers with the `@telnyx/webrtc` SDK. Once registered, call `POST /v1/voice/calls/web/dial` with the returned `credentialId` to place the call. The split avoids bridging to a browser that has not finished registering. The token lives ~1 hour (it must outlive the whole call, not just the handshake). 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::CreateVoiceWebSession200Response**](createVoiceWebSession_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## dial_voice_web_call

> models::DialVoiceWebCall200Response dial_voice_web_call(dial_voice_web_call_request)
Dial from the browser softphone

Step 2 of the browser softphone handshake: places an outbound call whose answered leg is bridged to the browser registered with the credential from `POST /v1/voice/calls/web`. The call runs through the normal outbound lane, so it is logged as outbound (from = your number, to = target) and recorded per the number's settings. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dial_voice_web_call_request** | [**DialVoiceWebCallRequest**](DialVoiceWebCallRequest.md) |  | [required] |

### Return type

[**models::DialVoiceWebCall200Response**](dialVoiceWebCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_voice_on_number

> models::DisableVoiceOnNumber200Response disable_voice_on_number(id)
Disable phone calling on a number

Turns off PSTN calling for the number. The stored forward destination and settings are preserved, so re-enabling restores the prior config. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DisableVoiceOnNumber200Response**](disableVoiceOnNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_voice_on_number

> models::EnableVoiceOnNumber200Response enable_voice_on_number(id, enable_voice_on_number_request)
Enable phone calling on a number

Turns on regular phone (PSTN) calling for one of your numbers and configures how inbound calls are handled. Inbound calls route to `forwardTo`: your own AI voice agent (Vapi/Retell), a phone, or a SIP endpoint. Optional extras: voicemail, business-hours windows, an IVR menu, a caller blocklist, recording, and transcription. A number can also be voice-enabled with no forward (outbound-only).  Idempotent, and doubles as the settings update: only fields present in the body are written. Omitting `forwardTo` preserves the current destination; sending an empty string clears it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID (from GET /v1/phone-numbers). | [required] |
**enable_voice_on_number_request** | Option<[**EnableVoiceOnNumberRequest**](EnableVoiceOnNumberRequest.md)> |  |  |

### Return type

[**models::EnableVoiceOnNumber200Response**](enableVoiceOnNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## end_voice_call

> models::EndVoiceCall200Response end_voice_call(id)
Hang up a live call

Hangs up a live call on demand. Idempotent: ending a call that already ended (or never connected) returns success with the call's current status. Final duration/cost are written asynchronously when the hangup event lands, so the call doc may briefly still show its prior status. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::EndVoiceCall200Response**](endVoiceCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_voice_call

> models::GetVoiceCall200Response get_voice_call(id)
Get a phone call

Full call detail, including the transcript segments when transcription was on.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::GetVoiceCall200Response**](getVoiceCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_voice_call_estimate

> models::GetVoiceCallEstimate200Response get_voice_call_estimate(to, minutes, recording, transcription)
Estimate call cost

Pre-call cost estimate for a PSTN call: the carrier leg plus optional recording and transcription add-ons. Same billing formula as the post-call invoice, so the quote and the final charge can't disagree. The per-minute figure is deliberately conservative (the real cost comes from the settled carrier record after the call), so estimates trend slightly over the actual invoice. Parity endpoint of `GET /v1/whatsapp/calls/estimate`, minus the Meta line (PSTN calls have no separate Meta bill, so `totalCostUSD` equals `billableCostUSD`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**to** | **String** | Destination number, E.164 (leading + optional). | [required] |
**minutes** | Option<**i32**> |  |  |[default to 1]
**recording** | Option<**bool**> |  |  |
**transcription** | Option<**bool**> |  |  |

### Return type

[**models::GetVoiceCallEstimate200Response**](getVoiceCallEstimate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_voice_call_recording

> models::GetWhatsAppCallRecording200Response get_voice_call_recording(id, r#as)
Get a call recording

Resolves a fresh, playable MP3 URL for the call's recording (provider-signed URLs expire ~10 minutes after signing, so this endpoint re-signs on demand). Default responds `302 Found` redirecting to the fresh URL; pass `as=json` to receive `{ url }` instead. 

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


## list_voice_calls

> models::ListVoiceCalls200Response list_voice_calls(status, direction, number, before, limit)
List phone calls

Your PSTN voice calls (inbound + outbound), newest first. Cursor pagination: pass the returned `nextCursor` as `before` for the next page. For a history that also includes WhatsApp calls, use `GET /v1/calls`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> |  |  |
**direction** | Option<**String**> |  |  |
**number** | Option<**String**> | Exact filter: calls involving this number (typically one of your DIDs). E.164, leading + optional. |  |
**before** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListVoiceCalls200Response**](listVoiceCalls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## transfer_voice_call

> models::TransferVoiceCall200Response transfer_voice_call(id, transfer_voice_call_request)
Blind-transfer a live call

Moves the call's current leg to a new destination (a phone number or a SIP endpoint). This is a BLIND transfer: control of the leg is handed off and the call ends normally when the transferred leg hangs up. The caller ID presented on the transfer leg is always your own number. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**transfer_voice_call_request** | [**TransferVoiceCallRequest**](TransferVoiceCallRequest.md) |  | [required] |

### Return type

[**models::TransferVoiceCall200Response**](transferVoiceCall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

