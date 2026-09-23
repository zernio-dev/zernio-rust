# WebhookPayloadMessageSentMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_interactive** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Instagram/Facebook only. The buttons, quickReplies and/or template this outgoing message carried, as sent (tracked urls included when link tracking wrapped a button). Absent when the send carried none. | [optional]
**location** | Option<[**models::WebhookPayloadMessageSentMetadataLocation**](WebhookPayloadMessageSentMetadataLocation.md)> |  | [optional]
**contacts** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | WhatsApp only. The contact cards this message carries. On API sends this is the `contacts` array exactly as given to the inbox send API (`name`, `phones[].phone` / `type`, `emails[]`); on Coexistence echoes of a card shared from the WhatsApp Business app it is Meta's shape (`phones[].wa_id`, `vcard`). The message `text` is only the emoji preview (`👤 <name>`); the cards live here.  | [optional]
**quoted_message_id** | Option<**String**> | `platformMessageId` of the message this send is a quote-reply to.  Present when the reply was sent through Zernio with `replyTo` on the inbox send API (WhatsApp and Telegram). A WhatsApp API send fires its `message.sent` off the delivery status, and the quote reference is forwarded from the stored send there, so it arrives on the same `message.sent` as any other WhatsApp send.  Not delivered on Instagram echoes. Zernio forwards `reply_to.mid` whenever Meta puts it on an echo, but on Instagram Meta does not send it, so a reply the operator quoted in the Instagram app arrives with no `quotedMessageId`. Facebook Messenger rides a separate subscription (`message_echoes`) and has not been measured, so treat it as unverified rather than supported.  Absent on WhatsApp Coexistence echoes. Meta omits the quote context from `smb_message_echoes`, so a reply the operator sent from the WhatsApp Business app arrives with no `quotedMessageId` even though WhatsApp shows it as a quote-reply. Do not read the absence of this field as \"not a reply\".  | [optional]
**thread_ts** | Option<**String**> | Slack only. Parent thread ts of the sent message. Pass it back as `replyTo` on the inbox send API to keep replying inside the thread.  | [optional]
**tiktok_message_type** | Option<**String**> | TikTok only. The message type as TikTok reports it, forwarded verbatim (for example image, video, sticker, share_post, emoji, reaction, template). Present on every TikTok DM that is not plain text; those arrive with text empty and, for image, video, share_post, sticker and emoji, an attachment (share_post as type share with the embed url and payload.videoId; sticker/emoji as type sticker, url signed and expiring). Absent on image sends made through the Zernio API, which carry the image in attachments. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


