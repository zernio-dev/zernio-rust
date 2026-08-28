# SendInboxMessage200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | Option<**String**> | Platform id of the sent message (not returned for Reddit). For WhatsApp this is the raw Meta wamid, the same id delivered as message.platformMessageId on webhooks and delivery-status updates, and the value to pass as replyTo to quote-reply. | [optional]
**conversation_id** | Option<**String**> | Zernio conversation id, echoed so the thread can be read back or replied to. It equals the id the list-conversations endpoint returns for Telegram, WhatsApp, SMS and Slack; for Facebook, Instagram, Bluesky and Reddit that endpoint returns the platform thread id instead, so do not correlate the two by equality. For X (Twitter), when the request addressed the conversation by its Twitter dm_conversation_id, that platform id is echoed back instead. Omitted when the send succeeded but the conversation could not be resolved to a stored record. | [optional]
**attachments** | Option<[**Vec<models::SendInboxMessage200ResponseDataAttachmentsInner>**](SendInboxMessage200ResponseDataAttachmentsInner.md)> | Echo of the sent attachment with its resolved public URL, when one is available (Facebook, Instagram, Telegram, WhatsApp). | [optional]
**message_ids** | Option<**Vec<String>**> | Facebook/Instagram only. Present when an attachment and text were both requested: Meta has no single body shape for both, so the send is two Meta messages under the hood. First element === messageId (the attachment); second is the follow-up text. | [optional]
**partial_failure** | Option<[**models::SendInboxMessage200ResponseDataPartialFailure**](SendInboxMessage200ResponseDataPartialFailure.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


