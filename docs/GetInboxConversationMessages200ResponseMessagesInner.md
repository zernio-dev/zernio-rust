# GetInboxConversationMessages200ResponseMessagesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**conversation_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**message** | Option<**String**> |  | [optional]
**sender_id** | Option<**String**> |  | [optional]
**sender_name** | Option<**String**> |  | [optional]
**sender_verified_type** | Option<**SenderVerifiedType**> | X/Twitter verified badge type. Only present for Twitter/X messages. (enum: blue, government, business, none) | [optional]
**direction** | Option<**Direction**> |  (enum: incoming, outgoing) | [optional]
**created_at** | Option<**String**> |  | [optional]
**attachments** | Option<[**Vec<models::GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner>**](GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner.md)> |  | [optional]
**subject** | Option<**String**> | Reddit message subject | [optional]
**story_reply** | Option<**bool**> | Instagram story reply | [optional]
**is_story_mention** | Option<**bool**> | Instagram story mention | [optional]
**is_edited** | Option<**bool**> | True if the sender has edited this message at least once. | [optional]
**edited_at** | Option<**String**> | When the most recent edit happened. | [optional]
**edit_count** | Option<**i32**> | Total number of edits applied. | [optional]
**edit_history** | Option<[**Vec<models::InboxMessageEditHistoryEntry>**](InboxMessageEditHistoryEntry.md)> | Every prior version of the message, oldest first. | [optional]
**is_deleted** | Option<**bool**> | True if the sender has deleted (unsent) this message. The original message and attachments fields remain populated. | [optional]
**deleted_at** | Option<**String**> |  | [optional]
**delivery_status** | Option<**DeliveryStatus**> | Lifecycle status for outgoing messages. Not all platforms emit every state (see webhook support matrix). (enum: sent, delivered, read, failed, deleted) | [optional]
**delivered_at** | Option<**String**> |  | [optional]
**read_at** | Option<**String**> |  | [optional]
**sent_at** | Option<**String**> | Original send time for outgoing messages (used for Messenger watermark queries). | [optional]
**delivery_error** | Option<[**models::GetInboxConversationMessages200ResponseMessagesInnerDeliveryError**](GetInboxConversationMessages200ResponseMessagesInnerDeliveryError.md)> |  | [optional]
**reactions** | Option<[**Vec<models::GetInboxConversationMessages200ResponseMessagesInnerReactionsInner>**](GetInboxConversationMessages200ResponseMessagesInnerReactionsInner.md)> | Emoji reactions on this message (WhatsApp / Telegram). At most one per party in a 1:1 thread. | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Platform-specific extras. Free-form, but commonly includes: `quotedMessageId` (platformMessageId this message replies to), `waInteractive` (a compact descriptor of WhatsApp interactive content sent: buttons / list / cta_url / flow / location_request), and for inbound interactive taps `interactiveType` / `interactiveId`. It can also carry `source` (`whatsapp_business_app` / `coexistence_history` on a WhatsApp Coexistence number, `bulk-api` on a POST /v1/whatsapp/bulk send), which is where the message reached us from rather than who produced it: read `sentVia` for that.  | [optional]
**sent_via** | Option<**SentVia**> | Which Zernio surface produced this outgoing message: `human` (an operator in the Zernio inbox), `api` (a call to this API), `broadcast`, `sequence`, `workflow`, `comment_automation`, or `bulk-api` (POST /v1/whatsapp/bulk). Same vocabulary as the `source` filter on the inbox analytics endpoints.  Always present, and `null` whenever the lineage is unknown: every incoming message, any outgoing message sent from the platform's own app, and every message stored before this field shipped (2026-08). Existing messages are NOT backfilled, so treat `null` as \"unknown\", never as \"sent by a human\".  (enum: human, api, broadcast, sequence, workflow, comment_automation, bulk-api, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


