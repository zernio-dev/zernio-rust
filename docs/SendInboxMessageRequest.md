# SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | 
**message** | Option<**String**> | Message text | [optional]
**attachment_url** | Option<**String**> | URL of the attachment to send (image, video, audio, or file). The URL must be publicly accessible. For binary file uploads, use multipart/form-data instead. | [optional]
**attachment_type** | Option<**AttachmentType**> | Type of attachment. Defaults to file if not specified. (enum: image, video, audio, file) | [optional]
**quick_replies** | Option<[**Vec<models::SendInboxMessageRequestQuickRepliesInner>**](SendInboxMessageRequestQuickRepliesInner.md)> | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional]
**buttons** | Option<[**Vec<models::SendInboxMessageRequestButtonsInner>**](SendInboxMessageRequestButtonsInner.md)> | Action buttons. Mutually exclusive with quickReplies. Max 3 items. | [optional]
**template** | Option<[**models::SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md)> |  | [optional]
**interactive** | Option<[**models::SendInboxMessageRequestInteractive**](SendInboxMessageRequestInteractive.md)> |  | [optional]
**reply_markup** | Option<[**models::SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md)> |  | [optional]
**messaging_type** | Option<**MessagingType**> | Facebook messaging type. Required when using messageTag. (enum: RESPONSE, UPDATE, MESSAGE_TAG) | [optional]
**message_tag** | Option<**MessageTag**> | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. (enum: CONFIRMED_EVENT_UPDATE, POST_PURCHASE_UPDATE, ACCOUNT_UPDATE, HUMAN_AGENT) | [optional]
**reply_to** | Option<**String**> | Platform message ID to quote-reply to. For WhatsApp, pass the wamid (available in message.platformMessageId from webhooks). For Telegram, pass the Telegram message ID. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


