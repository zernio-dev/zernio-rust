# WebhookPayloadConversationStartedConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal conversation ID | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, whatsapp, twitter, reddit, bluesky) | 
**platform_conversation_id** | **String** |  | 
**participant_id** | Option<**String**> | Contact's platform identifier (IGSID | [optional]
**participant_name** | **String** |  | 
**participant_username** | Option<**String**> | Contact's handle when the platform exposes one | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**status** | **Status** |  (enum: active, archived) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


