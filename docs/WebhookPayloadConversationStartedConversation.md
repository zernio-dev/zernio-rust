# WebhookPayloadConversationStartedConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Internal conversation ID | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, whatsapp, twitter, reddit, bluesky) | 
**platform_conversation_id** | **String** |  | 
**participant_id** | Option<**String**> | Contact's platform identifier (IGSID, PSID, wa_id, etc.) | [optional]
**participant_name** | **String** |  | 
**participant_username** | Option<**String**> | Contact's handle when the platform exposes one | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**status** | **Status** |  (enum: active, archived) | 
**contact_id** | Option<**String**> | Zernio CRM Contact ID for the participant, when one exists. Resolved by joining `participantId` to the ContactChannel collection (same join used by message.*, reaction.received, and call.* webhooks). Best-effort: omitted when no channel matches or `participantId` is absent. Lets integrators seed the CRM straight from `conversation.started` without waiting for the first `message.*` event.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


