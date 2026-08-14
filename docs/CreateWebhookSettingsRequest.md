# CreateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Webhook name (1-50 characters) | 
**url** | **String** | Webhook endpoint URL (must be a valid URL, whitespace trimmed) | 
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | **Vec<Events>** | Events to subscribe to (at least one required) (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, post.platform.published, post.platform.failed, post.platform.deleted, post.tiktok.url_resolved, post.external.created, post.external.updated, post.external.deleted, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, conversation.started, call.received, call.ended, call.failed, call.permission_request, message.sent, message.edited, message.deleted, message.delivered, message.read, message.failed, reaction.received, referral.received, comment.received, review.new, review.updated, lead.received, ad.status_changed, whatsapp.template.status_updated, whatsapp.template.category_updated, whatsapp.automatic_event, whatsapp.number.activated, whatsapp.number.declined, whatsapp.number.action_required, whatsapp.number.verification_required, whatsapp.number.suspended, whatsapp.number.reactivated, whatsapp.number.released, whatsapp.number.kyc_submitted, verification.approved, verification.failed) | 
**is_active** | Option<**bool**> | Enable or disable webhook delivery. Defaults to `true` when omitted. | [optional][default to true]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers to include in webhook requests | [optional]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Resource groups this subscription does not receive (opt-out denylist). Omit or send an empty array to receive every event in `events`. Listing a group here drops its events before delivery and on every replay path. Set at creation it applies to everything this subscription ever receives; changed later via PUT it applies to events emitted after the change, with a five-minute tail for events already queued (see that operation). When the caller is a restricted (zrk_) key, that key's own disabled groups are unioned into whatever you send here, so a restricted key can never create a subscription wider than itself. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


