# WebhookPayloadMessageSentMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**quoted_message_id** | Option<**String**> | platformMessageId of the message this send is a quote-reply to. Set when the reply was sent through Zernio with `replyTo` on the inbox send API (WhatsApp and Telegram), and when the operator replied from the native WhatsApp Business, Instagram or Messenger app. WhatsApp API sends carry it on the event fired from the delivery status, so it arrives on the same `message.sent` as any other WhatsApp send.  | [optional]
**thread_ts** | Option<**String**> | Slack only. Parent thread ts of the sent message. Pass it back as `replyTo` on the inbox send API to keep replying inside the thread.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


