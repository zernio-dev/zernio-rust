# SearchInboxConversations200ResponseDataInnerConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Conversation ID, usable with the conversation messages endpoints | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_username** | Option<**String**> |  | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**business_scoped_user_id** | Option<**String**> | WhatsApp only. Meta business-scoped user ID (BSUID), the stable identity anchor; present when Meta has sent it for this participant. | [optional]
**whatsapp_username** | Option<**String**> | WhatsApp only. The participant's WhatsApp username (e.g. `jane.shop`, no leading @). Not a stable identifier, because users can change it: useful for display, not recommended as an identity anchor. Captured from inbound messages, so older threads fill in on their next inbound. | [optional]
**status** | Option<**Status**> |  (enum: active, archived) | [optional]
**last_message** | Option<**String**> | The conversation's most recent message preview | [optional]
**last_message_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


