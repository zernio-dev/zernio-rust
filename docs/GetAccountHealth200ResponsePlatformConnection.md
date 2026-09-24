# GetAccountHealth200ResponsePlatformConnection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | `connected` = Meta served the channel object. `disconnected` = Meta refused to serve it (Graph error 100, subcode 33), which is how a phone-side coexistence disconnect surfaces. `unknown` = the live read failed for another reason (timeout, transient Meta error), not evidence either way. (enum: connected, disconnected, unknown) | [optional]
**checked_at** | Option<**String**> | When this live probe ran (always the current request; never cached) | [optional]
**phone_status** | Option<**String**> | Meta's own `status` field from the phone-number node (for example CONNECTED), when the object was readable | [optional]
**meta_error** | Option<[**models::GetAccountHealth200ResponsePlatformConnectionMetaError**](GetAccountHealth200ResponsePlatformConnectionMetaError.md)> |  | [optional]
**inbound_webhook_subscribed** | Option<**bool**> | From the phone number's Meta health_status. `false` = Meta says Zernio is not subscribed to the message webhook for this number, so inbound messages are not delivered even though the number is CONNECTED and can still send. Fix by re-subscribing (reconnect the number); if it stays `false`, the number is routed to a different WhatsApp Business Account (typically after linking it to a Facebook Page). `true` = Meta reports no such problem. `null` = Meta did not report it (read failed or no health_status), not evidence either way. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


