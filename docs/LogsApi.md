# \LogsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_logs**](LogsApi.md#list_logs) | **GET** /v1/logs | List activity logs



## list_logs

> models::ListLogs200Response list_logs(r#type, status, platform, action, search, days, limit, skip, account_id, event, request_id, from, to, status_code, api_key_id, include_read_receipts)
List activity logs

Unified logs endpoint. Returns logs for publishing, connections, webhooks, and messaging. Filter by type, platform, status, and time range. Logs are retained for 90 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**r#type** | Option<**String**> | Log category to query. Use `all` for the unified view across every category, or `api_request` for your API request logs (method, path, status, latency).  |  |[default to publishing]
**status** | Option<**String**> | Filter by status |  |
**platform** | Option<**String**> | Filter by platform |  |
**action** | Option<**String**> | Filter by action (e.g., post.published, message.sent, account.connected, webhook.delivered) |  |
**search** | Option<**String**> | Free-text search across log fields |  |
**days** | Option<**i32**> | Number of days to look back (max 90) |  |[default to 90]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]
**account_id** | Option<**String**> | Filter by connected account ID |  |
**event** | Option<**String**> | Filter webhook logs by event (e.g. post.published, message.received) |  |
**request_id** | Option<**String**> | Correlation ID — returns every log spawned by a single API request |  |
**from** | Option<**String**> | Precise start instant (ISO 8601); narrows within the day range |  |
**to** | Option<**String**> | Precise end instant (ISO 8601) |  |
**status_code** | Option<**i32**> | Filter by exact HTTP status code (api_request logs) |  |
**api_key_id** | Option<**String**> | Filter by the API key that made the request (api_request logs) |  |
**include_read_receipts** | Option<**bool**> | Include message.read / message.delivered events (hidden by default for messaging logs) |  |[default to false]

### Return type

[**models::ListLogs200Response**](listLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

