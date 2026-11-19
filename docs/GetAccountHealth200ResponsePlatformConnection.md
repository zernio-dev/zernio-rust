# GetAccountHealth200ResponsePlatformConnection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | `connected` = Meta served the channel object. `disconnected` = Meta refused to serve it (Graph error 100, subcode 33), which is how a phone-side coexistence disconnect surfaces. `unknown` = the live read failed for another reason (timeout, transient Meta error), not evidence either way. (enum: connected, disconnected, unknown) | [optional]
**checked_at** | Option<**String**> | When this live probe ran (always the current request; never cached) | [optional]
**phone_status** | Option<**String**> | Meta's own `status` field from the phone-number node (for example CONNECTED), when the object was readable. Anything other than CONNECTED adds an issue and raises `status` (BANNED: error, others: warning). | [optional]
**meta_error** | Option<[**models::GetAccountHealth200ResponsePlatformConnectionMetaError**](GetAccountHealth200ResponsePlatformConnectionMetaError.md)> |  | [optional]
**inbound_webhook_subscribed** | Option<**bool**> | From the phone number's Meta health_status, overridden to `false` when subscribing the number's WhatsApp Business Account to Zernio's webhooks failed at connect.  - `false`: Meta says Zernio is not subscribed to the message webhook for this number, or the subscribe failed when the number was connected, so inbound messages are not delivered, though the number is CONNECTED and can still send. - `false`, fix: re-subscribe (reconnect the number). If it stays `false`, the number is routed to a different WhatsApp Business Account (typically after linking it to a Facebook Page). - `true`: Meta reports no such problem. - `null`: Meta did not report it (read failed or no health_status); not evidence either way.  | [optional]
**can_send_message** | Option<**String**> | Top-level `can_send_message` from the phone number's Meta health_status: `AVAILABLE`, `LIMITED` or `BLOCKED`. `BLOCKED` adds an issue and raises `status` to at least `warning`. `null` when Meta did not report it. | [optional]
**messaging_blockers** | Option<[**Vec<models::GetAccountHealth200ResponsePlatformConnectionMessagingBlockersInner>**](GetAccountHealth200ResponsePlatformConnectionMessagingBlockersInner.md)> | The health_status entities that are not `AVAILABLE`, one item per Meta error, with calling-only signals (138024, 138025) removed. `null` when the read failed. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


