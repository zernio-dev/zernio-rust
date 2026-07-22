# Webhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> | Unique webhook identifier | [optional]
**name** | Option<**String**> | Webhook name (for identification) | [optional]
**url** | Option<**String**> | Webhook endpoint URL | [optional]
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification. | [optional]
**events** | Option<**Vec<Events>**> | Events subscribed to (enum: post.scheduled, post.published, post.failed, post.partial, post.cancelled, post.recycled, post.platform.published, post.platform.failed, post.tiktok.url_resolved, post.external.created, post.external.updated, post.external.deleted, account.connected, account.disconnected, account.ads.initial_sync_completed, message.received, conversation.started, call.received, call.ended, call.failed, call.permission_request, message.sent, message.edited, message.deleted, message.delivered, message.read, message.failed, reaction.received, comment.received, review.new, review.updated, lead.received, ad.status_changed, whatsapp.template.status_updated, whatsapp.automatic_event, whatsapp.number.activated, whatsapp.number.declined, whatsapp.number.action_required, whatsapp.number.verification_required, whatsapp.number.suspended, whatsapp.number.reactivated, whatsapp.number.released, whatsapp.number.kyc_submitted, verification.approved, verification.failed) | [optional]
**is_active** | Option<**bool**> | Whether webhook delivery is enabled | [optional]
**last_fired_at** | Option<**String**> | Timestamp of last successful webhook delivery | [optional]
**failure_count** | Option<**i32**> | Consecutive delivery failures (resets on success, webhook disabled at 10) | [optional]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers included in webhook requests | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


