# CreateInboxConversation201ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | Option<**String**> | Platform message ID (dm_event_id) | [optional]
**conversation_id** | Option<**String**> | Platform conversation ID (dm_conversation_id). For WhatsApp, this is Zernio's internal conversation id (24-character hex) which matches the id returned by the list-conversations endpoint and the conversationId in the message.received and conversation.started webhooks; use it to correlate the created thread with inbound events. | [optional]
**participant_id** | Option<**String**> | Twitter numeric user ID of the recipient | [optional]
**participant_name** | Option<**String**> | Display name of the recipient | [optional]
**participant_username** | Option<**String**> | Twitter username of the recipient | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


