# SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | 
**message** | Option<**String**> | Message text | [optional]
**attachment_url** | Option<**String**> | URL of the attachment to send (image, video, audio, or file). The URL must be publicly accessible. For binary file uploads, use multipart/form-data instead. | [optional]
**attachment_type** | Option<**AttachmentType**> | Type of attachment. Defaults to file if not specified. (enum: image, video, audio, file) | [optional]
**attachment_name** | Option<**String**> | WhatsApp only. Display name for a document sent via attachmentUrl with attachmentType: file (e.g. \"Report.pdf\"). Maps to the recipient's file name; without it WhatsApp derives the name from the URL and shows \"Untitled\". Ignored for image/video/audio and for binary uploads (which use the uploaded file's name). | [optional]
**voice_note** | Option<**bool**> | WhatsApp only. When `true` on an audio attachment, the message is sent as a voice message (PTT) — the recipient sees the waveform + voice-note UI instead of a basic audio attachment. The audio file MUST be `.ogg` encoded with the OPUS codec (mono) per Meta's voice-message contract; other formats are rejected by WhatsApp. Ignored for non-audio attachments.  | [optional]
**quick_replies** | Option<[**Vec<models::SendInboxMessageRequestQuickRepliesInner>**](SendInboxMessageRequestQuickRepliesInner.md)> | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional]
**buttons** | Option<[**Vec<models::SendInboxMessageRequestButtonsInner>**](SendInboxMessageRequestButtonsInner.md)> | Action buttons. Mutually exclusive with quickReplies. Max 3 items.  WhatsApp: buttons always render as interactive reply buttons. Only `title` and `payload` are used — `type`, `url`, and `phone` are ignored (WhatsApp has no URL/phone button in this field; use the `interactive` field with `type: cta_url` for a link button). `payload` becomes the button reply ID delivered on the `message.received` webhook when the user taps. To send a simple reply-button message, provide `title` + `payload` and set `type: postback`, e.g. `{ \"type\": \"postback\", \"title\": \"Yes\", \"payload\": \"yes\" }`.  | [optional]
**template** | Option<[**models::SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md)> |  | [optional]
**interactive** | Option<[**models::SendInboxMessageRequestInteractive**](SendInboxMessageRequestInteractive.md)> |  | [optional]
**reply_markup** | Option<[**models::SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md)> |  | [optional]
**messaging_type** | Option<**MessagingType**> | Facebook messaging type. Required when using messageTag. (enum: RESPONSE, UPDATE, MESSAGE_TAG) | [optional]
**message_tag** | Option<**MessageTag**> | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. (enum: CONFIRMED_EVENT_UPDATE, POST_PURCHASE_UPDATE, ACCOUNT_UPDATE, HUMAN_AGENT) | [optional]
**reply_to** | Option<**String**> | Platform message ID to quote-reply to. For WhatsApp, pass the wamid (available in message.platformMessageId from webhooks). For Telegram, pass the Telegram message ID. | [optional]
**location** | Option<[**models::SendInboxMessageRequestLocation**](SendInboxMessageRequestLocation.md)> |  | [optional]
**contacts** | Option<[**Vec<models::SendInboxMessageRequestContactsInner>**](SendInboxMessageRequestContactsInner.md)> | WhatsApp-only. Send one or more contact cards. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


