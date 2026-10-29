# WebhookPayloadMessageSentMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal message ID | 
**conversation_id** | **String** | Internal conversation ID | 
**platform** | **Platform** | Every platform whose outgoing messages Zernio observes. sms is absent on purpose: its carrier receipts update delivery status and never raise message.sent. (enum: instagram, facebook, telegram, whatsapp, twitter, reddit, bluesky, slack, tiktok, imessage) | 
**platform_message_id** | **String** | Platform's message ID | 
**direction** | **Direction** |  (enum: incoming, outgoing) | 
**text** | Option<**String**> | Message text content | 
**attachments** | [**Vec<models::WebhookPayloadMessageSentMessageAttachmentsInner>**](WebhookPayloadMessageSentMessageAttachmentsInner.md) |  | 
**sender** | [**models::WebhookPayloadMessageSentMessageSender**](WebhookPayloadMessageSentMessageSender.md) |  | 
**sent_at** | **String** | When the message was sent, as reported by the platform and passed through unmodified. Full ISO 8601 date-time: Instagram and Facebook carry millisecond precision; some platforms (for example WhatsApp and Telegram) report whole seconds.  Use it as the chronological ordering key. If two messages share the same value, fetch the conversation messages with sortOrder=desc for the deterministic order.  | 
**is_read** | **bool** |  | 
**source** | Option<**Source**> | WhatsApp send origin. Absent on non-WhatsApp platforms.  - whatsapp_business_app: sent from the WhatsApp Business phone app on a Coexistence number. - cloud_api: sent through Zernio (dashboard, API, or broadcasts). - meta_business_agent: Meta Business Agent answered on the number.  Says where WhatsApp saw the send come from, not which Zernio surface produced it: read sentVia for that.  (enum: whatsapp_business_app, cloud_api, meta_business_agent) | [optional]
**sent_via** | Option<**SentVia**> | Which Zernio surface produced this message. Same vocabulary as the `source` filter on the inbox analytics endpoints, and the same value a later GET on this message returns.  - `human`: an operator in the Zernio inbox - `api`: a call to this API - `broadcast` - `sequence` - `workflow` - `comment_automation` - `bulk-api`: POST /v1/whatsapp/bulk  Always present, and `null` whenever the lineage is unknown:  - any outgoing message not sent through Zernio (one typed in the platform's own app, a Meta automated reply such as an instant reply or away message, the echo of a click-to-message ad's greeting) - every message stored before this field shipped (2026-08)  Existing messages are NOT backfilled, so treat `null` as \"unknown\", never as \"sent by a human\".  (enum: human, api, broadcast, sequence, workflow, comment_automation, bulk-api, ) | [optional]
**automation_id** | Option<**String**> | The comment automation that sent this DM (sentVia comment_automation). Null otherwise. | [optional]
**workflow_id** | Option<**String**> | The workflow whose run sent this message (sentVia workflow). Null otherwise. | [optional]
**execution_id** | Option<**String**> | The workflow run (execution) that sent this message, as returned by the workflow executions endpoints. Null when workflowId is null. | [optional]
**broadcast_id** | Option<**String**> | The broadcast that sent this message (sentVia broadcast). Null otherwise. | [optional]
**sequence_id** | Option<**String**> | The sequence whose step sent this message (sentVia sequence). Null otherwise. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


