# \LogsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_post_logs**](LogsApi.md#get_post_logs) | **GET** /v1/posts/{postId}/logs | Get post logs
[**list_connection_logs**](LogsApi.md#list_connection_logs) | **GET** /v1/connections/logs | List connection logs
[**list_logs**](LogsApi.md#list_logs) | **GET** /v1/logs | List activity logs
[**list_posts_logs**](LogsApi.md#list_posts_logs) | **GET** /v1/posts/logs | List publishing logs



## get_post_logs

> models::GetPostLogs200Response get_post_logs(post_id, limit)
Get post logs

Retrieve all publishing logs for a specific post. Shows the complete history of publishing attempts for that post across all platforms. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post ID | [required] |
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]

### Return type

[**models::GetPostLogs200Response**](getPostLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_connection_logs

> models::ListConnectionLogs200Response list_connection_logs(platform, event_type, status, days, limit, skip)
List connection logs

**Deprecated.** Use `GET /v1/logs?type=connections` instead. Retrieve connection event logs. Logs are retained for 90 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform |  |
**event_type** | Option<**String**> | Filter by event type |  |
**status** | Option<**String**> | Filter by status (shorthand for event types) |  |
**days** | Option<**i32**> | Number of days to look back (max 7) |  |[default to 7]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]

### Return type

[**models::ListConnectionLogs200Response**](listConnectionLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_logs

> models::ListLogs200Response list_logs(r#type, status, platform, action, search, days, limit, skip)
List activity logs

Unified logs endpoint. Returns logs for publishing, connections, webhooks, and messaging. Filter by type, platform, status, and time range. Logs are retained for 90 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**r#type** | Option<**String**> | Log category to query |  |[default to publishing]
**status** | Option<**String**> | Filter by status |  |
**platform** | Option<**String**> | Filter by platform |  |
**action** | Option<**String**> | Filter by action (e.g., post.published, message.sent, account.connected, webhook.delivered) |  |
**search** | Option<**String**> | Free-text search across log fields |  |
**days** | Option<**i32**> | Number of days to look back (max 90) |  |[default to 90]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]

### Return type

[**models::ListLogs200Response**](listLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_posts_logs

> models::ListPostsLogs200Response list_posts_logs(status, platform, action, days, limit, skip, search)
List publishing logs

**Deprecated.** Use `GET /v1/logs?type=publishing` instead. Retrieve publishing logs for all posts. Logs are retained for 90 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> | Filter by log status |  |
**platform** | Option<**String**> | Filter by platform |  |
**action** | Option<**String**> | Filter by action type |  |
**days** | Option<**i32**> | Number of days to look back (max 7) |  |[default to 7]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]
**search** | Option<**String**> | Search through log entries by text content. |  |

### Return type

[**models::ListPostsLogs200Response**](listPostsLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

