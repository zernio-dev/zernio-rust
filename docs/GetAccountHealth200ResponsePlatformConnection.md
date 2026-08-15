# GetAccountHealth200ResponsePlatformConnection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | `connected` = Meta served the channel object. `disconnected` = Meta refused to serve it (Graph error 100, subcode 33), which is how a phone-side coexistence disconnect surfaces. `unknown` = the live read failed for another reason (timeout, transient Meta error), not evidence either way. (enum: connected, disconnected, unknown) | [optional]
**checked_at** | Option<**String**> | When this live probe ran (always the current request; never cached) | [optional]
**phone_status** | Option<**String**> | Meta's own `status` field from the phone-number node (for example CONNECTED), when the object was readable | [optional]
**meta_error** | Option<[**models::GetAccountHealth200ResponsePlatformConnectionMetaError**](GetAccountHealth200ResponsePlatformConnectionMetaError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


