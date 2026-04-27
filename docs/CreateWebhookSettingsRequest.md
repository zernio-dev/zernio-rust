# CreateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Webhook name (1-50 characters) | 
**url** | **String** | Webhook endpoint URL (must be a valid URL, whitespace trimmed) | 
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | **Vec<Events>** | Events to subscribe to (at least one required) (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, comment.received, review.new, review.updated) | 
**is_active** | Option<**bool**> | Enable or disable webhook delivery. Defaults to `true` when omitted. | [optional][default to true]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers to include in webhook requests | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


