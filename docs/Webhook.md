# Webhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> | Unique webhook identifier | [optional]
**name** | Option<**String**> | Webhook name (for identification) | [optional]
**url** | Option<**String**> | Webhook endpoint URL | [optional]
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification. | [optional]
**events** | Option<**Vec<Events>**> | Events subscribed to (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, post.platform.published, post.platform.failed, post.platform.deleted, post.tiktok.url_resolved, post.external.created, post.external.updated, post.external.deleted, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, conversation.started, call.received, call.ended, call.failed, call.permission_request, message.sent, message.edited, message.deleted, message.delivered, message.read, message.failed, reaction.received, referral.received, comment.received, review.new, review.updated, lead.received, ad.status_changed, whatsapp.template.status_updated, whatsapp.template.category_updated, whatsapp.account.name_status_updated, whatsapp.automatic_event, whatsapp.number.activated, whatsapp.number.declined, whatsapp.number.action_required, whatsapp.number.verification_required, whatsapp.number.suspended, whatsapp.number.reactivated, whatsapp.number.released, whatsapp.number.kyc_submitted, phone_number.stock_available, verification.approved, verification.failed) | [optional]
**is_active** | Option<**bool**> | Whether webhook delivery is enabled | [optional]
**last_fired_at** | Option<**String**> | Timestamp of last successful webhook delivery | [optional]
**failure_count** | Option<**i32**> | Consecutive delivery failures (resets on success, webhook disabled at 10) | [optional]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers included in webhook requests | [optional]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Resource groups this subscription does not receive (opt-out denylist, same vocabulary and same semantics as the field on API keys). Absent or empty means the subscription receives every event listed in `events`, which is how every subscription created before this field existed behaves. An event whose group is listed here is dropped before delivery even when it is still present in `events`, and the same check runs on every replay path (test fire, redelivery, dead-letter requeue). Editing the denylist applies to every event emitted afterwards; events already queued when the edit landed can still be delivered for up to five minutes after they were enqueued. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


