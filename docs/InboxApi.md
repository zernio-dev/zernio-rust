# \InboxApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_whats_app_media**](InboxApi.md#get_whats_app_media) | **GET** /v1/whatsapp/media/{mediaId} | Download WhatsApp media



## get_whats_app_media

> std::path::PathBuf get_whats_app_media(media_id, account_id)
Download WhatsApp media

Streams the binary for a WhatsApp attachment. This is the endpoint the `url` on a WhatsApp `attachments[]` entry points at, in both the `message.received` webhook and the List messages response.  **This is an authenticated endpoint, not a public link.** Send `Authorization: Bearer <your API key>` exactly as you would for any other call. Passing the URL straight to a browser, an LLM vision API, or a no-code \"download file\" step without the header returns `401`. This is the most common integration mistake on this endpoint, and it differs from Instagram, Facebook and Telegram, whose `attachments[].url` is a direct CDN link that needs no header.  **Fetch on receipt, not lazily.** WhatsApp media lives in Meta's media store, not ours, and it is removed after a limited retention window (currently 7 days, and Meta has been dropping some inbound media sooner). Once Meta drops it the media is unrecoverable and this endpoint answers `400` permanently, so retrying will never succeed. Download and store the bytes when the webhook arrives. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**media_id** | **String** | The media id from `attachments[].payload.id`. | [required] |
**account_id** | **String** | The WhatsApp account that received the media. | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

