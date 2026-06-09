# WebhookLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | Option<**String**> | ID of the account owner the webhook belongs to | [optional]
**webhook_id** | Option<**String**> | ID of the webhook configuration that produced this delivery | [optional]
**webhook_name** | Option<**String**> | Name of the webhook configuration at delivery time | [optional]
**event_id** | Option<**String**> | Stable webhook event ID (correlates to the delivered payload) | [optional]
**event** | Option<**String**> | Event type that triggered the delivery (e.g. post.published) | [optional]
**url** | Option<**String**> | Destination URL the webhook was delivered to | [optional]
**status** | Option<**Status**> | Delivery outcome (enum: success, failed) | [optional]
**status_code** | Option<**i32**> | HTTP status code returned by the destination endpoint | [optional]
**request_payload** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The JSON payload sent to the destination endpoint | [optional]
**response_body** | Option<**String**> | Response body returned by the destination endpoint | [optional]
**error_message** | Option<**String**> | Error message when delivery failed | [optional]
**attempt_number** | Option<**i32**> | Delivery attempt number (increments on retries) | [optional]
**response_time** | Option<**i32**> | Time taken by the destination endpoint to respond, in milliseconds | [optional]
**created_at** | Option<**String**> | Timestamp the delivery was attempted | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


