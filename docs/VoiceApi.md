# \VoiceApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attach_number_to_sip_trunk**](VoiceApi.md#attach_number_to_sip_trunk) | **POST** /v1/phone-numbers/{id}/sip-trunk | Attach a number to a SIP trunk
[**create_sip_trunk**](VoiceApi.md#create_sip_trunk) | **POST** /v1/phone-numbers/sip-trunks | Create a SIP trunk
[**create_voice_call**](VoiceApi.md#create_voice_call) | **POST** /v1/voice/calls | Place an outbound phone call
[**create_voice_web_session**](VoiceApi.md#create_voice_web_session) | **POST** /v1/voice/calls/web | Mint a browser softphone session
[**delete_sip_trunk**](VoiceApi.md#delete_sip_trunk) | **DELETE** /v1/phone-numbers/sip-trunks/{id} | Delete a SIP trunk
[**detach_number_from_sip_trunk**](VoiceApi.md#detach_number_from_sip_trunk) | **DELETE** /v1/phone-numbers/{id}/sip-trunk | Detach a number from its SIP trunk
[**dial_voice_web_call**](VoiceApi.md#dial_voice_web_call) | **POST** /v1/voice/calls/web/dial | Dial from the browser softphone
[**disable_voice_on_number**](VoiceApi.md#disable_voice_on_number) | **DELETE** /v1/phone-numbers/{id}/voice | Disable phone calling on a number
[**enable_voice_on_number**](VoiceApi.md#enable_voice_on_number) | **POST** /v1/phone-numbers/{id}/voice | Enable phone calling on a number
[**end_voice_call**](VoiceApi.md#end_voice_call) | **POST** /v1/voice/calls/{id}/end | Hang up a live call
[**get_sip_trunk**](VoiceApi.md#get_sip_trunk) | **GET** /v1/phone-numbers/sip-trunks/{id} | Get a SIP trunk
[**get_voice_call**](VoiceApi.md#get_voice_call) | **GET** /v1/voice/calls/{id} | Get a phone call
[**get_voice_call_estimate**](VoiceApi.md#get_voice_call_estimate) | **GET** /v1/voice/calls/estimate | Estimate call cost
[**get_voice_call_recording**](VoiceApi.md#get_voice_call_recording) | **GET** /v1/voice/calls/{id}/recording | Get a call recording
[**list_sip_trunks**](VoiceApi.md#list_sip_trunks) | **GET** /v1/phone-numbers/sip-trunks | List SIP trunks
[**list_voice_calls**](VoiceApi.md#list_voice_calls) | **GET** /v1/voice/calls | List phone calls
[**rotate_sip_trunk_credentials**](VoiceApi.md#rotate_sip_trunk_credentials) | **POST** /v1/phone-numbers/sip-trunks/{id}/rotate-credentials | Rotate a SIP trunk's password
[**transfer_voice_call**](VoiceApi.md#transfer_voice_call) | **POST** /v1/voice/calls/{id}/transfer | Blind-transfer a live call



## attach_number_to_sip_trunk

> models::AttachNumberToSipTrunk200Response attach_number_to_sip_trunk(id, attach_number_to_sip_trunk_request)
Attach a number to a SIP trunk

Routes the number's calls to the trunk: the external platform receives its inbound directly and can present it as outbound caller ID. While attached, Zernio-side voice features are off for this number (call forwarding, IVR, voicemail, recording, the softphone, and WhatsApp calling), so the number must have Calls and WhatsApp calling disabled before attaching. SMS and WhatsApp messaging are unaffected. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID (from GET /v1/phone-numbers). | [required] |
**attach_number_to_sip_trunk_request** | [**AttachNumberToSipTrunkRequest**](AttachNumberToSipTrunkRequest.md) |  | [required] |

### Return type

[**models::AttachNumberToSipTrunk200Response**](attachNumberToSipTrunk_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_sip_trunk

> models::CreateSipTrunk201Response create_sip_trunk(create_sip_trunk_request)
Create a SIP trunk

Creates a SIP trunk an external voice platform (Retell, ElevenLabs, Vapi, or any SIP endpoint) can import your Zernio numbers into. The trunk carries both directions: inbound calls on attached numbers are delivered to `sipHost`, and the platform originates outbound calls through `termination.uri` with the digest credentials.  The `digestPassword` is returned only by this call (and by rotate-credentials); store it immediately. Attach any number of numbers to a trunk. Several trunks may point at the same host — each carries its own credentials and spend cap, so separate destination workspaces (e.g. an agency's clients) stay isolated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_sip_trunk_request** | [**CreateSipTrunkRequest**](CreateSipTrunkRequest.md) |  | [required] |

### Return type

[**models::CreateSipTrunk201Response**](createSipTrunk_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_voice_call

> models::CreateVoiceCall200Response create_voice_call(create_voice_call_request, idempotency_key)
Place an outbound phone call

Dials `to` FROM one of your voice-enabled numbers and, on answer, bridges the callee to the number's stored forward destination, or to the per-call `forwardTo` override. Destinations can be your own AI voice agent (Vapi/Retell), a phone, or a SIP endpoint. An optional `greeting` is spoken to the callee before the bridge.  The 200 response means the call is dialing; the lifecycle continues asynchronously (track it via `GET /v1/voice/calls/{id}` or the `call.*` webhooks). Outbound calls are capped per rolling hour (429 when hit).  **Idempotency:** send an `Idempotency-Key` header to make retries safe; same key + same body replays the original response instead of dialing (and billing) a second call. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_voice_call_request** | [**CreateVoiceCallRequest**](CreateVoiceCallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

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


## delete_sip_trunk

> models::DeleteSmsSenderId200Response delete_sip_trunk(id)
Delete a SIP trunk

Tears down the trunk and its carrier-side objects. Refused while any number is still attached: detach them first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DeleteSmsSenderId200Response**](deleteSmsSenderId_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## detach_number_from_sip_trunk

> models::DetachNumberFromSipTrunk200Response detach_number_from_sip_trunk(id)
Detach a number from its SIP trunk

Returns the number's calls to Zernio routing. Idempotent when the number is not attached to any trunk. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DetachNumberFromSipTrunk200Response**](detachNumberFromSipTrunk_200_response.md)

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


## get_sip_trunk

> models::GetSipTrunk200Response get_sip_trunk(id)
Get a SIP trunk

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::GetSipTrunk200Response**](getSipTrunk_200_response.md)

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


## list_sip_trunks

> models::ListSipTrunks200Response list_sip_trunks()
List SIP trunks

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListSipTrunks200Response**](listSipTrunks_200_response.md)

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


## rotate_sip_trunk_credentials

> models::RotateSipTrunkCredentials200Response rotate_sip_trunk_credentials(id)
Rotate a SIP trunk's password

Mints a new digest password on the trunk. The old password stops working immediately, so update the destination platform right away. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::RotateSipTrunkCredentials200Response**](rotateSipTrunkCredentials_200_response.md)

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

