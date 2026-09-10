# \ToolsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**download_tik_tok_video**](ToolsApi.md#download_tik_tok_video) | **GET** /v1/tools/tiktok/download | Download a TikTok video



## download_tik_tok_video

> models::DownloadTikTokVideo200Response download_tik_tok_video(url, action, format_id)
Download a TikTok video

Get a download URL or list available formats for a TikTok video. Requires Tools API access and uses the Tools API rate limit. Provider gateway failures and provider-side access blocks return 503; an unavailable video returns 404.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | TikTok video URL or numeric video ID. | [required] |
**action** | Option<**String**> | Return a download URL or the available formats. |  |[default to download]
**format_id** | Option<**String**> | Format ID from the formats response. Omit to select the first available format. |  |

### Return type

[**models::DownloadTikTokVideo200Response**](downloadTikTokVideo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

