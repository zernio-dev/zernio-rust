# UpdateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** | Webhook ID to update (required) | 
**name** | Option<**String**> | Webhook name (1-50 characters). Must be non-empty if provided. | [optional]
**url** | Option<**String**> | Webhook endpoint URL (must be a valid URL, whitespace trimmed). Must be a valid URL if provided. | [optional]
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | Option<**Vec<Events>**> | Events to subscribe to. Must contain at least one event if provided. (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, post.platform.published, post.platform.failed, post.external.created, post.external.updated, post.external.deleted, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, message.sent, message.edited, message.deleted, message.delivered, message.read, message.failed, reaction.received, comment.received, review.new, review.updated, ad.status_changed, whatsapp.template.status_updated, whatsapp.number.activated, whatsapp.number.declined, whatsapp.number.verification_required, whatsapp.number.suspended, whatsapp.number.reactivated, whatsapp.number.released) | [optional]
**is_active** | Option<**bool**> | Enable or disable webhook delivery | [optional]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers to include in webhook requests | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


