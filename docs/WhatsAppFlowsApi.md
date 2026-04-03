# \WhatsAppFlowsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_whats_app_flow**](WhatsAppFlowsApi.md#create_whats_app_flow) | **POST** /v1/whatsapp/flows | Create flow
[**delete_whats_app_flow**](WhatsAppFlowsApi.md#delete_whats_app_flow) | **DELETE** /v1/whatsapp/flows/{flowId} | Delete flow
[**deprecate_whats_app_flow**](WhatsAppFlowsApi.md#deprecate_whats_app_flow) | **POST** /v1/whatsapp/flows/{flowId}/deprecate | Deprecate flow
[**get_whats_app_flow**](WhatsAppFlowsApi.md#get_whats_app_flow) | **GET** /v1/whatsapp/flows/{flowId} | Get flow
[**get_whats_app_flow_json**](WhatsAppFlowsApi.md#get_whats_app_flow_json) | **GET** /v1/whatsapp/flows/{flowId}/json | Get flow JSON asset
[**list_whats_app_flows**](WhatsAppFlowsApi.md#list_whats_app_flows) | **GET** /v1/whatsapp/flows | List flows
[**publish_whats_app_flow**](WhatsAppFlowsApi.md#publish_whats_app_flow) | **POST** /v1/whatsapp/flows/{flowId}/publish | Publish flow
[**send_whats_app_flow_message**](WhatsAppFlowsApi.md#send_whats_app_flow_message) | **POST** /v1/whatsapp/flows/send | Send flow message
[**update_whats_app_flow**](WhatsAppFlowsApi.md#update_whats_app_flow) | **PATCH** /v1/whatsapp/flows/{flowId} | Update flow
[**upload_whats_app_flow_json**](WhatsAppFlowsApi.md#upload_whats_app_flow_json) | **PUT** /v1/whatsapp/flows/{flowId}/json | Upload flow JSON



## create_whats_app_flow

> models::CreateWhatsAppFlow200Response create_whats_app_flow(create_whats_app_flow_request)
Create flow

Create a new WhatsApp Flow in DRAFT status. Optionally clone an existing flow. After creating, upload a Flow JSON definition, then publish to make it sendable. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_flow_request** | [**CreateWhatsAppFlowRequest**](CreateWhatsAppFlowRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppFlow200Response**](createWhatsAppFlow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_flow

> models::UpdateYoutubeDefaultPlaylist200Response delete_whats_app_flow(flow_id, account_id)
Delete flow

Delete a DRAFT flow. This is irreversible. Only flows in DRAFT status can be deleted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deprecate_whats_app_flow

> models::UpdateYoutubeDefaultPlaylist200Response deprecate_whats_app_flow(flow_id, publish_whats_app_flow_request)
Deprecate flow

Deprecate a PUBLISHED flow. **This is irreversible.** Deprecated flows cannot be sent or opened, but existing active sessions may continue until they complete. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**publish_whats_app_flow_request** | [**PublishWhatsAppFlowRequest**](PublishWhatsAppFlowRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_flow

> models::GetWhatsAppFlow200Response get_whats_app_flow(flow_id, account_id, fields)
Get flow

Get details for a specific flow, including status, categories, validation errors, and preview URL. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**fields** | Option<**String**> | Comma-separated fields to return (default: id,name,status,categories,validation_errors,json_version,preview,data_api_version,endpoint_uri) |  |

### Return type

[**models::GetWhatsAppFlow200Response**](getWhatsAppFlow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_flow_json

> models::GetWhatsAppFlowJson200Response get_whats_app_flow_json(flow_id, account_id)
Get flow JSON asset

Get the flow JSON asset metadata, including a temporary download URL for the Flow JSON file. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppFlowJson200Response**](getWhatsAppFlowJson_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_flows

> models::ListWhatsAppFlows200Response list_whats_app_flows(account_id)
List flows

List all WhatsApp Flows for the Business Account (WABA) associated with the given account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::ListWhatsAppFlows200Response**](listWhatsAppFlows_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## publish_whats_app_flow

> models::UpdateYoutubeDefaultPlaylist200Response publish_whats_app_flow(flow_id, publish_whats_app_flow_request)
Publish flow

Publish a DRAFT flow. **This is irreversible.** Once published, the flow and its JSON become immutable and the flow can be sent to users. To update a published flow, create a new flow (optionally cloning this one via `cloneFlowId`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**publish_whats_app_flow_request** | [**PublishWhatsAppFlowRequest**](PublishWhatsAppFlowRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_whats_app_flow_message

> models::SendWhatsAppFlowMessage200Response send_whats_app_flow_message(send_whats_app_flow_message_request)
Send flow message

Send a published flow as an interactive message with a CTA button. When the recipient taps the button, the flow opens natively in WhatsApp. Flow responses are received via webhooks. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_whats_app_flow_message_request** | [**SendWhatsAppFlowMessageRequest**](SendWhatsAppFlowMessageRequest.md) |  | [required] |

### Return type

[**models::SendWhatsAppFlowMessage200Response**](sendWhatsAppFlowMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_flow

> models::UpdateYoutubeDefaultPlaylist200Response update_whats_app_flow(flow_id, update_whats_app_flow_request)
Update flow

Update metadata (name, categories) of a DRAFT flow. Published flows are immutable. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**update_whats_app_flow_request** | [**UpdateWhatsAppFlowRequest**](UpdateWhatsAppFlowRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_whats_app_flow_json

> models::UploadWhatsAppFlowJson200Response upload_whats_app_flow_json(flow_id, upload_whats_app_flow_json_request)
Upload flow JSON

Upload or update the Flow JSON for a DRAFT flow. The Flow JSON defines all screens, components (text inputs, dropdowns, date pickers, etc.), and navigation.  Meta validates the JSON on upload and returns any validation errors. See: https://developers.facebook.com/docs/whatsapp/flows/reference/flowjson 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**flow_id** | **String** | Flow ID | [required] |
**upload_whats_app_flow_json_request** | [**UploadWhatsAppFlowJsonRequest**](UploadWhatsAppFlowJsonRequest.md) |  | [required] |

### Return type

[**models::UploadWhatsAppFlowJson200Response**](uploadWhatsAppFlowJson_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

