# ErrorResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | Option<**String**> | Human-readable error message. | [optional]
**r#type** | Option<**Type**> | Error class for programmatic handling. (enum: invalid_request_error, authentication_error, permission_error, not_found, rate_limit_error, platform_error, api_error) | [optional]
**code** | Option<**String**> | Stable machine-readable error code. | [optional]
**param** | Option<**String**> | The request field that caused the error, when applicable. | [optional]
**platform** | Option<**String**> | Upstream platform (e.g. meta, google, tiktok) — present when type is platform_error. | [optional]
**platform_error** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Raw error payload from the upstream platform, passed through verbatim so integrators can read provider-specific codes. For Meta this includes error_subcode, error_user_title, and error_user_msg.  | [optional]
**details** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Additional structured context (e.g. field-level validation errors). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


