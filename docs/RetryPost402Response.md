# RetryPost402Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | Option<**String**> | Human-readable error message. | [optional]
**r#type** | Option<**Type**> | Error class for programmatic handling. (enum: invalid_request_error, authentication_error, permission_error, not_found, rate_limit_error, platform_error, api_error) | [optional]
**code** | Option<**String**> | Stable machine-readable error code. | [optional]
**param** | Option<**String**> | The request field that caused the error, when applicable. | [optional]
**doc_url** | Option<**String**> | Documentation page for resolving the error, when one applies. | [optional]
**platform** | Option<**String**> | Upstream platform (e.g. meta, google, tiktok), present when type is platform_error. | [optional]
**platform_error** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Raw error payload from the upstream platform, passed through verbatim so integrators can read provider-specific codes. For Meta this includes error_subcode, error_user_title, and error_user_msg.  | [optional]
**provider** | Option<**String**> | Email API: the mailbox provider the error came from (`google`, `microsoft`). | [optional]
**provider_error** | Option<[**models::ErrorResponseProviderError**](ErrorResponseProviderError.md)> |  | [optional]
**retryable** | Option<**bool**> | Email API: whether the same request can succeed if retried (with the same `Idempotency-Key` for sends). | [optional]
**request_id** | Option<**String**> | Email API: the request id, also in the `X-Request-Id` header. Quote it when you contact support. | [optional]
**docs_url** | Option<**String**> | Email API: where this `code` is documented. | [optional]
**details** | Option<[**models::ErrorResponseDetails**](ErrorResponseDetails.md)> |  | [optional]
**funding_url** | **String** | Dashboard link to Billing that opens the Add funds drawer (the add-card drawer first when there is no card). Send the user there, then retry. | 
**required_cents** | Option<**i32**> | Only when an item debited later (a phone number's first month, all numbers of the order) is refused: what the balance must hold, in cents. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


