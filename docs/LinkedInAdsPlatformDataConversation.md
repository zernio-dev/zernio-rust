# LinkedInAdsPlatformDataConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | **String** | InMail subject shown in the inbox. | 
**sender** | Option<**String**> | Person or organization URN. Defaults to the authoring Company Page. The sender must be approved for the ad account first (Campaign Manager > Manage message ad senders) or LinkedIn rejects the create with SINMAIL_SENDER_NOT_APPROVED.  | [optional]
**body** | Option<**String**> | Optional intro body (HTML allowed). | [optional]
**footer** | Option<**String**> | Terms shown at the bottom of the message. | [optional]
**headline** | Option<**String**> | Conversation headline. Defaults to the first message's first line. | [optional]
**first_message_id** | **String** |  | 
**messages** | [**Vec<models::LinkedInAdsPlatformDataConversationMessagesInner>**](LinkedInAdsPlatformDataConversationMessagesInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


