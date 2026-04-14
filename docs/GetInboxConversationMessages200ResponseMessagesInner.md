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
**edit_history** | Option<[**Vec<models::GetInboxConversationMessages200ResponseMessagesInnerEditHistoryInner>**](GetInboxConversationMessages200ResponseMessagesInnerEditHistoryInner.md)> | Every prior version of the message, oldest first. | [optional]
**is_deleted** | Option<**bool**> | True if the sender has deleted (unsent) this message. The original message and attachments fields remain populated. | [optional]
**deleted_at** | Option<**String**> |  | [optional]
**delivery_status** | Option<**DeliveryStatus**> | Lifecycle status for outgoing messages. Not all platforms emit every state (see webhook support matrix). (enum: sent, delivered, read, failed, deleted) | [optional]
**delivered_at** | Option<**String**> |  | [optional]
**read_at** | Option<**String**> |  | [optional]
**sent_at** | Option<**String**> | Original send time for outgoing messages (used for Messenger watermark queries). | [optional]
**delivery_error** | Option<[**models::GetInboxConversationMessages200ResponseMessagesInnerDeliveryError**](GetInboxConversationMessages200ResponseMessagesInnerDeliveryError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


