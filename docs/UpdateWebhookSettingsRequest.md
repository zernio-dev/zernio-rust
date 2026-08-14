# UpdateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** | Webhook ID to update (required) | 
**name** | Option<**String**> | Webhook name (1-50 characters). Must be non-empty if provided. | [optional]
**url** | Option<**String**> | Webhook endpoint URL (must be a valid URL, whitespace trimmed). Must be a valid URL if provided. | [optional]
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | Option<**Vec<Events>**> | Events to subscribe to. Must contain at least one event if provided. (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, post.platform.published, post.platform.failed, post.platform.deleted, post.tiktok.url_resolved, post.external.created, post.external.updated, post.external.deleted, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, conversation.started, call.received, call.ended, call.failed, call.permission_request, message.sent, message.edited, message.deleted, message.delivered, message.read, message.failed, reaction.received, referral.received, comment.received, review.new, review.updated, lead.received, ad.status_changed, whatsapp.template.status_updated, whatsapp.automatic_event, whatsapp.number.activated, whatsapp.number.declined, whatsapp.number.action_required, whatsapp.number.verification_required, whatsapp.number.suspended, whatsapp.number.reactivated, whatsapp.number.released, whatsapp.number.kyc_submitted, verification.approved, verification.failed) | [optional]
**is_active** | Option<**bool**> | Enable or disable webhook delivery | [optional]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers to include in webhook requests | [optional]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Replaces the subscription's denylist. Send an empty array to clear it and receive every event in `events` again. Omitting the field leaves the current denylist untouched. Applies to events emitted after the update; already-queued events can still deliver for up to five minutes after they were enqueued. When the caller is a restricted (zrk_) key, that key's own disabled groups are unioned back in either way, so a restricted key can neither clear nor widen a subscription past its own groups. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


