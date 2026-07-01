# ListLogs200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**String**> | Log category (publishing, connections, webhooks, messaging) | [optional]
**action** | Option<**String**> | Specific action (post.published, message.sent, account.connected, etc.) | [optional]
**user_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: success, failed, pending, skipped) | [optional]
**status_code** | Option<**i32**> |  | [optional]
**error_message** | Option<**String**> |  | [optional]
**error_code** | Option<**String**> |  | [optional]
**duration_ms** | Option<**i32**> |  | [optional]
**endpoint** | Option<**String**> | The API endpoint that triggered this log | [optional]
**request_body** | Option<**String**> | Request JSON (truncated to 5KB) | [optional]
**response_body** | Option<**String**> | Response JSON (truncated to 10KB) | [optional]
**created_at** | Option<**String**> |  | [optional]
**metadata** | Option<**String**> | Additional context as JSON string | [optional]
**request_id** | Option<**String**> | Correlation ID linking every log from one API request (api_request logs) | [optional]
**api_key_id** | Option<**String**> | The API key that made the request (api_request logs) | [optional]
**method** | Option<**String**> | HTTP method (api_request logs) | [optional]
**path** | Option<**String**> | Request path (api_request logs) | [optional]
**ip_address** | Option<**String**> | Client IP address (api_request logs) | [optional]
**user_agent** | Option<**String**> | Client user-agent (api_request logs) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


