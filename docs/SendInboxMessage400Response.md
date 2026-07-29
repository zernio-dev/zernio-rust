# SendInboxMessage400Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | Option<**String**> |  | [optional]
**code** | Option<**Code**> | Stable machine-readable reason. PLATFORM_LIMITATION covers a capability the platform does not offer (e.g. Bluesky and Reddit DMs reject media); MISSING_PARTICIPANT means the stored conversation has no recipient to send to. (enum: PLATFORM_LIMITATION, MISSING_PARTICIPANT) | [optional]
**platform_error** | Option<[**models::SendInboxMessage400ResponsePlatformError**](SendInboxMessage400ResponsePlatformError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


