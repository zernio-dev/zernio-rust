# \ContentRetentionApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_content_retention**](ContentRetentionApi.md#get_content_retention) | **GET** /v1/content-retention | Get content retention mode
[**update_content_retention**](ContentRetentionApi.md#update_content_retention) | **PUT** /v1/content-retention | Turn zero content retention on or off



## get_content_retention

> models::ContentRetentionResponse get_content_retention()
Get content retention mode

Returns whether your team stores content. `none` is zero content retention: Zernio keeps identifiers and metadata only, and content fields come back as `null` with `contentNotRetained: true`. See the zero content retention guide for what changes. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ContentRetentionResponse**](ContentRetentionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_content_retention

> models::ContentRetentionResponse update_content_retention(update_content_retention_request)
Turn zero content retention on or off

Sets your team's content retention mode for every member. Only the team owner can change it, with a signed-in session or a full-access API key.  - `none` turns on zero content retention: from then on Zernio stores no message text, comments, lead answers, mentions, post text after publishing, call transcripts or recordings. Webhooks become the only copy, so store each event when it arrives. - `standard` stores content again for new data. Content that was not stored cannot come back. - The change applies to new data within about 5 minutes. Content stored before it stays until it is deleted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_content_retention_request** | [**UpdateContentRetentionRequest**](UpdateContentRetentionRequest.md) |  | [required] |

### Return type

[**models::ContentRetentionResponse**](ContentRetentionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

