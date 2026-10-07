# ListInboxConversationAnalytics200ResponseItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversation_id** | Option<**String**> | The platformConversationId. A thread whose events were logged under both its ids comes back as one row. | [optional]
**mongo_id** | Option<**String**> | The Zernio conversation id, when a matching conversation exists | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_username** | Option<**String**> |  | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**last_message** | Option<**String**> | Cached preview from the Conversation doc | [optional]
**total_messages** | Option<**i32**> |  | [optional]
**received** | Option<**i32**> |  | [optional]
**sent** | Option<**i32**> |  | [optional]
**read** | Option<**i32**> |  | [optional]
**failed** | Option<**i32**> |  | [optional]
**first_message_at** | Option<**String**> |  | [optional]
**last_message_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


