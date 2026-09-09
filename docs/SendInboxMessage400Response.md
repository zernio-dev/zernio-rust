# SendInboxMessage400Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> | Present on Meta pass-through rejections: platform_error when Meta rejected the send (see platform/platformError below), invalid_request_error for validation failures. (enum: platform_error, invalid_request_error) | [optional]
**code** | Option<**Code**> | Stable machine-readable reason. PLATFORM_LIMITATION covers a capability the platform does not offer (e.g. Bluesky and Reddit DMs reject media); MISSING_PARTICIPANT means the stored conversation has no recipient to send to; DIRECT_SEND_NOT_ELIGIBLE and DIRECT_SEND_BLOCKED mean the WhatsApp Business Account needs Meta to grant or restore Direct Send access; DIRECT_SEND_LIMITED is temporary, Meta lifts it on its own; platform_api_error means Meta itself rejected the send (see platformError). (enum: PLATFORM_LIMITATION, MISSING_PARTICIPANT, DIRECT_SEND_NOT_ELIGIBLE, DIRECT_SEND_LIMITED, DIRECT_SEND_BLOCKED, platform_api_error) | [optional]
**platform** | Option<**String**> | Present alongside code platform_api_error. The platform that rejected the send (e.g. instagram, facebook). | [optional]
**platform_error** | Option<[**models::SendInboxMessage400ResponsePlatformError**](SendInboxMessage400ResponsePlatformError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


