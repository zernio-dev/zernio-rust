# \RcsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_rcs_test_device**](RcsApi.md#add_rcs_test_device) | **POST** /v1/rcs/agents/{agentId}/test-devices | Invite an RCS test phone
[**create_rcs_agent**](RcsApi.md#create_rcs_agent) | **POST** /v1/rcs/agents | Request an RCS agent
[**deactivate_rcs_agent**](RcsApi.md#deactivate_rcs_agent) | **DELETE** /v1/rcs/agents/{agentId} | Deactivate an RCS agent
[**get_rcs_agent**](RcsApi.md#get_rcs_agent) | **GET** /v1/rcs/agents/{agentId} | Get an RCS agent
[**get_rcs_capabilities**](RcsApi.md#get_rcs_capabilities) | **GET** /v1/rcs/capabilities | Check RCS capability
[**list_rcs_agents**](RcsApi.md#list_rcs_agents) | **GET** /v1/rcs/agents | List RCS agents
[**list_rcs_brands**](RcsApi.md#list_rcs_brands) | **GET** /v1/rcs/brands | List RCS brands
[**list_rcs_test_devices**](RcsApi.md#list_rcs_test_devices) | **GET** /v1/rcs/agents/{agentId}/test-devices | List RCS test phones
[**remove_rcs_test_device**](RcsApi.md#remove_rcs_test_device) | **DELETE** /v1/rcs/agents/{agentId}/test-devices/{testDeviceId} | Remove an RCS test phone
[**request_rcs_agent_launch**](RcsApi.md#request_rcs_agent_launch) | **POST** /v1/rcs/agents/{agentId}/launch-request | Send the launch filing
[**send_rcs_message**](RcsApi.md#send_rcs_message) | **POST** /v1/rcs/messages | Send an RCS message
[**update_rcs_agent**](RcsApi.md#update_rcs_agent) | **PATCH** /v1/rcs/agents/{agentId} | Update an RCS agent
[**upload_rcs_asset**](RcsApi.md#upload_rcs_asset) | **POST** /v1/rcs/assets | Upload an RCS logo or banner



## add_rcs_test_device

> models::AddRcsTestDevice201Response add_rcs_test_device(agent_id, add_rcs_test_device_request)
Invite an RCS test phone

Invites a phone to try the agent before launch. It must accept the invite in its messaging app. Available once the agent exists with the carriers (after brand vetting). T-Mobile and AT&T numbers cannot be test phones. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |
**add_rcs_test_device_request** | [**AddRcsTestDeviceRequest**](AddRcsTestDeviceRequest.md) |  | [required] |

### Return type

[**models::AddRcsTestDevice201Response**](addRcsTestDevice_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_rcs_agent

> models::CreateRcsAgent201Response create_rcs_agent(create_rcs_agent_request, idempotency_key)
Request an RCS agent

Requests a new agent for a profile, with a new company (`brand`) or an existing one (`brandId`, skips vetting when it is already verified). The request lands in our review: nothing is filed with the carriers or billed until we submit it. A profile can hold several agents. Requires usage-based billing and a card on file. Send an `Idempotency-Key` header to make retries safe. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_rcs_agent_request** | [**CreateRcsAgentRequest**](CreateRcsAgentRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::CreateRcsAgent201Response**](createRcsAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deactivate_rcs_agent

> models::CreateRcsAgent201Response deactivate_rcs_agent(agent_id)
Deactivate an RCS agent

Stops sending, disconnects its inbox account and stops monthly billing. Fees already charged are not refunded.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |

### Return type

[**models::CreateRcsAgent201Response**](createRcsAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_rcs_agent

> models::CreateRcsAgent201Response get_rcs_agent(agent_id)
Get an RCS agent

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |

### Return type

[**models::CreateRcsAgent201Response**](createRcsAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_rcs_capabilities

> models::GetRcsCapabilities200Response get_rcs_capabilities(agent_id, numbers)
Check RCS capability

Which recipients can receive RCS from the agent and which rich features their phones support. Up to 100 numbers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |
**numbers** | **String** | Comma-separated E.164 numbers, max 100. | [required] |

### Return type

[**models::GetRcsCapabilities200Response**](getRcsCapabilities_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_rcs_agents

> models::ListRcsAgents200Response list_rcs_agents(include_closed)
List RCS agents

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include_closed** | Option<**bool**> | Include rejected and deactivated agents. |  |

### Return type

[**models::ListRcsAgents200Response**](listRcsAgents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_rcs_brands

> models::ListRcsBrands200Response list_rcs_brands()
List RCS brands

The team's RCS brands (vetted companies), to reuse one for another agent with `brandId`.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListRcsBrands200Response**](listRcsBrands_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_rcs_test_devices

> models::ListRcsTestDevices200Response list_rcs_test_devices(agent_id)
List RCS test phones

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |

### Return type

[**models::ListRcsTestDevices200Response**](listRcsTestDevices_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_rcs_test_device

> models::UpdateYoutubeDefaultPlaylist200Response remove_rcs_test_device(agent_id, test_device_id)
Remove an RCS test phone

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |
**test_device_id** | **uuid::Uuid** |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## request_rcs_agent_launch

> models::CreateRcsAgent201Response request_rcs_agent_launch(agent_id, rcs_launch_request)
Send the launch filing

Sends the launch details the carriers review (campaign, consent and a public test video). US agents send them once they are in `testing`; we review them before they reach the carriers. Agents in other markets send them while still in review (`requested`, `changes_requested` or `brand_vetting`), because we file everything with the carriers at once; this saves the details without changing the status. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |
**rcs_launch_request** | [**RcsLaunchRequest**](RcsLaunchRequest.md) |  | [required] |

### Return type

[**models::CreateRcsAgent201Response**](createRcsAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_rcs_message

> models::SendRcsMessage200Response send_rcs_message(send_rcs_message_request, idempotency_key)
Send an RCS message

Sends from one of your agents. Use `text` for a plain message or `content` for rich content (card, carousel, media, suggestion chips). Before launch an agent only reaches test phones that accepted the invite. With the agent's `smsFallbackFrom` set, phones without RCS get `fallbackText` (default: the message's readable text) as SMS.  Replies and status arrive as webhooks with `platform: \"rcs\"`: `message.received` (a tapped chip carries its postback in `metadata.postbackPayload`), `message.delivered`, `message.read` and `message.failed`. Send an `Idempotency-Key` header to make retries safe. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_rcs_message_request** | [**SendRcsMessageRequest**](SendRcsMessageRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::SendRcsMessage200Response**](sendRcsMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_rcs_agent

> models::CreateRcsAgent201Response update_rcs_agent(agent_id, update_rcs_agent_request)
Update an RCS agent

Edits the filing while the agent is `requested` or `changes_requested`; answering a change request puts it back in our review. The company can only change until it is filed. `smsFallbackFrom` stays editable in any status (null removes it). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agent_id** | **String** |  | [required] |
**update_rcs_agent_request** | [**UpdateRcsAgentRequest**](UpdateRcsAgentRequest.md) |  | [required] |

### Return type

[**models::CreateRcsAgent201Response**](createRcsAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_rcs_asset

> models::ListInboxReviews200ResponseDataInnerPhotosInner upload_rcs_asset(file, kind)
Upload an RCS logo or banner

Uploads an image and returns a public URL for `profile.logoUrl` or `profile.heroUrl`. The image is cropped and compressed to the carriers' exact rules (logo 224x224 under 50 KB, banner 1440x448 under 200 KB). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file** | **std::path::PathBuf** | PNG, JPEG or WebP. | [required] |
**kind** | **String** |  | [required] |

### Return type

[**models::ListInboxReviews200ResponseDataInnerPhotosInner**](listInboxReviews_200_response_data_inner_photos_inner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

