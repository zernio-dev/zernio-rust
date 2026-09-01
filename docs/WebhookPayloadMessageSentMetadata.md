# WebhookPayloadMessageSentMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**quoted_message_id** | Option<**String**> | `platformMessageId` of the message this send is a quote-reply to.  Present when the reply was sent through Zernio with `replyTo` on the inbox send API (WhatsApp and Telegram). A WhatsApp API send fires its `message.sent` off the delivery status, and the quote reference is forwarded from the stored send there, so it arrives on the same `message.sent` as any other WhatsApp send.  Not delivered on Instagram echoes. Zernio forwards `reply_to.mid` whenever Meta puts it on an echo, but on Instagram Meta does not send it, so a reply the operator quoted in the Instagram app arrives with no `quotedMessageId`. Facebook Messenger rides a separate subscription (`message_echoes`) and has not been measured, so treat it as unverified rather than supported.  Absent on WhatsApp Coexistence echoes. Meta omits the quote context from `smb_message_echoes`, so a reply the operator sent from the WhatsApp Business app arrives with no `quotedMessageId` even though WhatsApp shows it as a quote-reply. Do not read the absence of this field as \"not a reply\".  | [optional]
**thread_ts** | Option<**String**> | Slack only. Parent thread ts of the sent message. Pass it back as `replyTo` on the inbox send API to keep replying inside the thread.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


